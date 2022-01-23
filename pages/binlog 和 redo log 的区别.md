- #CruelCoding #[[2022-01-23]] #MySQL [讨论](https://github.com/Monsooooon/CruelFundamental/tree/main/homework/202201/23)
-
- [[binlog]] 为 [[mysql]] 的 Server 层实现的，而 [[redo log]] 为 [[InnoDB]] 引擎所特有的
	- > MySQL 整体来看，其实就有两块：一块是 Server 层，它主要做的是 MySQL 功能层面的事情；还有一块是引擎层，负责存储相关的具体事宜。redo log 是 InnoDB 引擎特有的日志，而 Server 层也有自己的日志，称为 binlog（归档日志）。
- [[redo log]]为物理日志，记录在某个数据页上面做什么修改；[[binlog]]为逻辑语句日志，记录的是这个语句的原始逻辑，例如id=x的这一行的某个字段+1
- [[redo log]]循环写，空间固定会用完。[[binlog]]可以追加写，binlog写完一定大小，可以切换到下一个内容当中写，不会覆盖。
- [[redo log]] 用于实现 [[crash-safe]] 能力（有了 redo log，InnoDB 就可以保证即使数据库发生异常重启，之前提交的记录都不会丢失，这个能力称为 crash-safe）
-
- [[binlog]] 的写入逻辑比较简单：事务执行过程中，先把日志写到 binlog cache，[[事务]]提交的时候，再把 binlog cache 写到 binlog 文件中。
  
  使用 cache 的原因：一个事务的 [[binlog]] 是不能被拆开的，因此不论这个事务多大，也要确保一次性写入。如果 cache 不够那么会暂存到磁盘。
  
  每个线程有自己 binlog cache，但是共用同一份 binlog 文件。
  
  cache 到 file 调用 write 和 fsync 的时机，是由参数 sync_binlog 控制的：
- sync_binlog=0 的时候，表示每次提交事务都只 write，不 fsync；
- sync_binlog=1 的时候，表示每次提交事务都会执行 fsync；
- sync_binlog=N (N>1) 的时候，表示每次提交事务都 write，但累积 N 个事务后才 fsync。
-
- 事务在执行过程中，生成的 [[redo log]] 是要先写到 redo log buffer 的，而 redo log buffer 的内容并不需要实时持久化。
- 如果事务执行期间 MySQL 发生异常重启，那这部分日志就丢了。由于事务并没有提交，所以这时日志丢了也不会有损失。
- redo log 持久化三种机制，以 innodb_flush_log_at_trx_commit 参数控制（可以参考上述 ACID 特性中的持久性里面的内容）。
- 需要注意的是，如果把 innodb_flush_log_at_trx_commit 设置成 1，那么 redo log 在 prepare 阶段持久化一次而在 commit 阶段就不用 fsync 了而只是写到了文件系统 OS Page Cache（因为崩溃恢复逻辑是要依赖于 prepare 的 redo log 再加上 binlog 来恢复的，如果事务执行成功 binlog 已经写完了，就算这时崩溃 redo log 还是 prepare 状态也没问题）。
-
- **为什么会有两份日志呢？**
	- 因为最开始 MySQL 里并没有 InnoDB 引擎。MySQL 自带的引擎是 [[MyISAM]]，但是 MyISAM 没有 crash-safe 的能力，**binlog 日志只能用于归档**。而 InnoDB 是另一个公司以插件形式引入 MySQL 的，既然只依靠 binlog 是没有 crash-safe 能力的，所以 InnoDB 使用另外一套日志系统——也就是 redo log 来实现 crash-safe 能力。
-
- # 参考
- [gaolijiemathcs 的答案](https://github.com/Monsooooon/CruelFundamental/blob/main/homework/202201/23/gaolijiemathcs.md)
- [02 | 日志系统：一条SQL更新语句是如何执行的？](https://time.geekbang.org/column/article/68633)