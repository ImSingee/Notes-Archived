---
title: Go 1.13 中值得关注的几个变化 (highlights)
---

- Author:: [[简悦]]

- Full Title:: Go 1.13 中值得关注的几个变化

- Category:: #articles

- URL:: https://mp.weixin.qq.com/s/Txqvanb17LYQYgohNiUHig

- Highlights first synced by #Readwise [[May 31st, 2021]]
	 - go 会在 go module 启用时在本地建立一个 go.sum 文件，用来存储依赖包特定版本的加密校验和

- New highlights added [[May 31st, 2021]] at 11:46 AM
	 - 在 Go 1.12 版本中，GO111MODULE 默认值为 auto，在 auto 模式下，GOPATH/src 下面的 repo 以及在 GOPATH 之外的 repo 依旧使用 GOPATH mode，不使用 go.mod 来管理依赖；在 Go 1.13 中，module mode 优先级提升，GO111MODULE 的默认值依然为 auto，但在这个 auto 下，无论是在 GOPATH/src 下还是 GOPATH 之外的 repo 中，只要目录下有 go.mod，go 编译器都会使用 go module 来管理依赖。

	 - GOPROXY 支持设置为多个 proxy 的列表 (多个 proxy 之间采用逗号分隔)，Go 编译器会按顺序尝试列表中的 proxy 以获取依赖包数据，但是当有 proxy server 服务不可达或者是返回的 http 状态码不是 404 也不是 410 时，go 会终止数据获取
