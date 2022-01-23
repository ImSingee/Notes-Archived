- #CruelCoding #[[2022-01-23]] [讨论](https://github.com/Monsooooon/CruelFundamental/tree/main/homework/202201/23)
-
- [[binlog]] 为 [[mysql]] 的 Server 层实现的，而 [[redolog]] 为 [[InnoDB]] 引擎所特有的
-
- [[binlog]] 的写入逻辑比较简单：事务执行过程中，先把日志写到 binlog cache，[[事务]]提交的时候，再把 binlog cache 写到 binlog 文件中。
  
  使用 cache 的原因：一个事务的 [[binlog]] 是不能被拆开的，因此不论这个事务多大，也要确保一次性写入。如果 cache 不够那么会暂存到磁盘。
  
  每个线程有自己 binlog cache，但是共用同一份 binlog 文件。
  
  cache 到 file 调用 write 和 fsync 的时机，是由参数 sync_binlog 控制的：
- sync_binlog=0 的时候，表示每次提交事务都只 write，不 fsync；
- sync_binlog=1 的时候，表示每次提交事务都会执行 fsync；
- sync_binlog=N (N>1) 的时候，表示每次提交事务都 write，但累积 N 个事务后才 fsync。
-
- 事务在执行过程中，生成的 redo log 是要先写到 redo log buffer 的，而 redo log buffer 的内容并不需要实时持久化。
- 如果事务执行期间 MySQL 发生异常重启，那这部分日志就丢了。由于事务并没有提交，所以这时日志丢了也不会有损失。
- redo log 持久化三种机制，以 innodb_flush_log_at_trx_commit 参数控制（可以参考上述 ACID 特性中的持久性里面的内容）。
- 需要注意的是，如果把 innodb_flush_log_at_trx_commit 设置成 1，那么 redo log 在 prepare 阶段持久化一次而在 commit 阶段就不用 fsync 了而只是写到了文件系统 OS Page Cache（因为崩溃恢复逻辑是要依赖于 prepare 的 redo log 再加上 binlog 来恢复的，如果事务执行成功 binlog 已经写完了，就算这时崩溃 redo log 还是 prepare 状态也没问题）。