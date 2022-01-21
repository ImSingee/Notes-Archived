---
title: Dnspeep - V2EX (highlights)
---

- Author:: [[v2ex.com]]

- Full Title:: Dnspeep - V2EX

- Category:: #articles

- URL:: https://www.v2ex.com/t/778485

- Highlights first synced by #Readwise [[May 27th, 2021]]
	 - https://jvns.ca/blog/2021/03/31/dnspeep-tool/一个简单的小工具，用来监控本地系统上发出的所有 DNS 请求。

	 - system32 目录下创建 echo aa > dnsrslvr.log
设置权限 cacls dnsrslvr.log /g everyone:f
重启动 dns client，net stop "dns client" ,net start "dns client" .
		 - **Note**: Windows 检查本地所有 DNS 请求
