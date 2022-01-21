---
title: 监听风云 | Inotify 实现原理 (highlights)
---

- Author:: [[juejin.cn]]

- Full Title:: 监听风云 | Inotify 实现原理

- Category:: #articles

- URL:: https://juejin.cn/post/6966910863101919269?cmdid=DJ0R2NSLES06QS

- Highlights first synced by #Readwise [[May 29th, 2021]]
	 - 当用户调用 read 或者 write 等系统调用对文件进行读写操作时，内核会把事件保存到 inotify_device 对象的事件队列中，然后唤醒等待 inotify 事件的进程
