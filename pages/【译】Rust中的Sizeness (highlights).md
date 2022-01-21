---
title: 【译】Rust中的Sizeness (highlights)
---

- Author:: [[mp.weixin.qq.com]]

- Full Title:: 【译】Rust中的Sizeness

- Category:: #articles

- URL:: https://mp.weixin.qq.com/s/5eRaXMewRqdyrnwhYU3HIg

- Highlights first synced by #Readwise [[May 25th, 2021]]
	 - 我们可以通过给结构体添加一个不确定大小(unsized)的字段来定义一个不确定大小结构体。不确定大小结构体只能有1个不确定大小字段并且该字段必须是这个结构体里的最后一个字段。
