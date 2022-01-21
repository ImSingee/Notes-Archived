---
title: 浅谈缓存 | 青空之蓝 (highlights)
---

- Author:: [[blog.ixk.me]]

- Full Title:: 浅谈缓存 | 青空之蓝

- Category:: #articles

- URL:: https://blog.ixk.me/post/talking-about-cache?cmdid=S3YFTK729UQOK2

- Highlights first synced by #Readwise [[May 28th, 2021]]
	 - LRU (最近最少使用)：通过一个缓存队列，按每项的最后被访问时间排序。当缓存满了的时候删除队尾，即最后一次被访问时间距现在最久的项。当某个项被使用的时候，则将该项移至队首。

	 - LFU (最近最少使用)：通过一个缓存队列，按每个缓存块的被访问频率将缓存中的各块排序，当缓存满了替换掉缓存队列中访问频率最低的一项。

	 - LRU-K：是一种 LRU 算法的增强版，LRU 队列的基础上，再添加一个队列维护数据访问的次数，由原来访问 1 次会被添加到缓存中，改为访问 K 次才会被加入到缓存中。
