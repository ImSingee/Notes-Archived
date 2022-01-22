- Go 的源码存放在 [官方 Repo](https://go.googlesource.com/go) 和 [Github Mirror](https://github.com/golang/go)，为了简化开始的流程，我们直接从 Github 克隆，同时，为了避免出问题，我们不从 master 分支开始，而是在克隆后切换到最新的稳定 tag（写这篇文章时是 `go1.17.6`）
- ```shell
  cd /opt
  sudo mkdir go
  sudo chown `whoami`:staff go
  git clone git@github.com:golang/go.git
  cd /opt/go
  git checkout go1.17.6
  ```
- 首先第一步永远是进行测试保证你下载的代码没有问题，Go 已经实现了 [[自举]]，因此必须已经[安装](https://go.dev/doc/install)好了 Go
- ```shell
  cd /opt/go/src
  ./all.bash # 编译并测试 Go 命令
  ```
- 看到 ALL TESTS PASSED 即为成功
- ![2022_01_23_image.png](https://cdn.logseq.com/%2Fa738fab4-25bd-41b0-bb53-62a3b83356f2e53e27f4-77ff-479d-86b8-99898dd25a7a2022_01_23_image.png?Expires=4796492069&Signature=NwGei1solzhSzx49snivfHP9fztWpD3~TQxbirr6Pq8chTZzSvycL~KZ9tADVSDMSgjLvUvSY1Y-1gqgh4R2qlEflcNt0TDY2~8FDe838tklTeRAipInXrofUDqQMvz723B7fOcLGqQglr8UhYjWszPF-5ESINCe0pDjijDtFML4BgOricwJRjfMtwxwBWC1qLdXKN5jC3EWajMsYNMKr5G9qutm67s7ox03aPUhokHe9YZiUhfXr8TtG-1SsguxnWJF8ICF~VKCHOt37OsbF4u82ucFPxxShCBc6-QlaK9ZbJPMvTnD4QUj7CGGin5iHssmYmSKyYUbe0L5daSF3g__&Key-Pair-Id=APKAJE5CCD6X7MP6PTEA)
-
- 简单看下 [all.bash](https://github.com/golang/go/blob/go1.17.6/src/all.bash) 做了什么
- ```bash
  ```