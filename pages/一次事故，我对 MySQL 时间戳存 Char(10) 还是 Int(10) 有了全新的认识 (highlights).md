---
title: 一次事故，我对 MySQL 时间戳存 Char(10) 还是 Int(10) 有了全新的认识 (highlights)
---

- Author:: [[华为云开发者社区]]

- Full Title:: 一次事故，我对 MySQL 时间戳存 Char(10) 还是 Int(10) 有了全新的认识

- Category:: #articles

- URL:: https://www.inoreader.com/article/3a9c6e7b036530ff-mysql-char10-int10

- Highlights first synced by #Readwise [[May 29th, 2021]]
	 - char 类型字段想走索引的话，必须用引号括起来。如果是时间戳等类型的纯数字，建议还是存为 int 型吧
