- #CruelCoding #[[2022-01-23]] [讨论](https://github.com/Monsooooon/CruelFundamental/tree/main/homework/202201/23)
-
- [[binlog]] 为 [[mysql]] 的 Server 层实现的，而 [[redolog]] 为 [[InnoDB]] 引擎所特有的
-
- binlog 的写入逻辑比较简单：事务执行过程中，先把日志写到 binlog cache，事务提交的时候，再把 binlog cache 写到 binlog 文件中。
  
  使用 cache 的原因：一个事务的 binlog 是不能被拆开的，因此不论这个事务多大，也要确保一次性写入。如果 cache 不够那么会暂存到磁盘。
  
  每个线程有自己 binlog cache，但是共用同一份 binlog 文件。
  
  cache 到 file 调用 write 和 fsync 的时机，是由参数 sync_binlog 控制的：
- sync_binlog=0 的时候，表示每次提交事务都只 write，不 fsync；
- sync_binlog=1 的时候，表示每次提交事务都会执行 fsync；
- sync_binlog=N (N>1) 的时候，表示每次提交事务都 write，但累积 N 个事务后才 fsync。