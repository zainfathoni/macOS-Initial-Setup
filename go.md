# Go Setup

Download Go [macOS binary release](https://golang.org/dl/) and follow the [installation instructions](https://golang.org/doc/install)

<details><summary>Test Go installation</summary>

<!-- markdownlint-disable MD014 -->

```bash
$ go version
go version go1.13.4 darwin/amd64

$ echo $GOPATH
/Users/zain/Code/go

$ mkdir $GOPATH

$ cd $GOPATH

$ mkdir src

$ mkdir src/hello

$ cd src/hello

$ echo "package main

import \"fmt\"

func main() {
        fmt.Printf(\"hello, world\\\n\")
}" >> hello.go

$ go build

$ ./hello
hello, world
```

<!-- markdownlint-enable MD014 -->

</details>
