---
title: "golang.org/x/sys/unix error on Go 1.18 - MacOS"
tags: [golang, 1.18]
layout: post
excerpt_separator: <!--more-->
published: true
---

I just reset my dev env. Then when I tried to run my old go code using `go run .`, it failed with errors:

```bash
# golang.org/x/sys/unix
../../go/pkg/mod/golang.org/x/sys@v0.0.0-20201119102817-f84b799fce68/unix/syscall_darwin.1_13.go:29:3: //go:linkname must refer to declared function or variable
../../go/pkg/mod/golang.org/x/sys@v0.0.0-20201119102817-f84b799fce68/unix/zsyscall_darwin_amd64.1_13.go:27:3: //go:linkname must refer to declared function or variable
../../go/pkg/mod/golang.org/x/sys@v0.0.0-20201119102817-f84b799fce68/unix/zsyscall_darwin_amd64.1_13.go:40:3: //go:linkname must refer to declared function or variable
../../go/pkg/mod/golang.org/x/sys@v0.0.0-20201119102817-f84b799fce68/unix/zsyscall_darwin_amd64.go:28:3: //go:linkname must refer to declared function or variable
../../go/pkg/mod/golang.org/x/sys@v0.0.0-20201119102817-f84b799fce68/unix/zsyscall_darwin_amd64.go:43:3: //go:linkname must refer to declared function or variable
../../go/pkg/mod/golang.org/x/sys@v0.0.0-20201119102817-f84b799fce68/unix/zsyscall_darwin_amd64.go:59:3: //go:linkname must refer to declared function or variable
../../go/pkg/mod/golang.org/x/sys@v0.0.0-20201119102817-f84b799fce68/unix/zsyscall_darwin_amd64.go:75:3: //go:linkname must refer to declared function or variable
../../go/pkg/mod/golang.org/x/sys@v0.0.0-20201119102817-f84b799fce68/unix/zsyscall_darwin_amd64.go:90:3: //go:linkname must refer to declared function or variable
../../go/pkg/mod/golang.org/x/sys@v0.0.0-20201119102817-f84b799fce68/unix/zsyscall_darwin_amd64.go:105:3: //go:linkname must refer to declared function or variable
../../go/pkg/mod/golang.org/x/sys@v0.0.0-20201119102817-f84b799fce68/unix/zsyscall_darwin_amd64.go:121:3: //go:linkname must refer to declared function or variable
../../go/pkg/mod/golang.org/x/sys@v0.0.0-20201119102817-f84b799fce68/unix/zsyscall_darwin_amd64.go:121:3: too many errors
```

The problem is solved by running this command:

```bash
go get -u golang.org/x/sys
```
