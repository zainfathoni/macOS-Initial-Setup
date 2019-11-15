# Go Setup

~~Download Go [macOS binary release](https://golang.org/dl/) and follow the [installation instructions](https://golang.org/doc/install)~~

<details><summary>Install Go using Homebrew</summary>

<!-- markdownlint-disable MD014 -->

```bash
$ brew install go
==> Downloading https://homebrew.bintray.com/bottles/go-1.13.4.catalina.bottle.tar.gz
==> Downloading from https://akamai.bintray.com/77/77af3e8081a002c86b4b87ec97dc5dc28cab49704913a4db22ebc7ce838dc6ad?__gda__=exp=1573853061~hmac=4f8bdec8b39750ab62edab55f63d702da3913ec5fc4fa004099021f382b97f69&response-content-disposition=at
######################################################################## 100.0%
==> Pouring go-1.13.4.catalina.bottle.tar.gz
🍺  /usr/local/Cellar/go/1.13.4: 9,271 files, 414MB

# verify installation
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
