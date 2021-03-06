## [beanstalkd-go](https://github.com/sjatsh/beanstalkd-go)

English | [简体中文](readme.md)

[![Build Status](https://travis-ci.org/sjatsh/beanstalkd-go.svg?branch=main)](https://travis-ci.org/sjatsh/beanstalkd-go.svg?branch=main)
[![codecov](https://codecov.io/gh/sjatsh/beanstalkd-go/branch/main/graph/badge.svg)](https://codecov.io/gh/sjatsh/beanstalkd-go)
[![Release](https://img.shields.io/github/release/sjatsh/beanstalkd-go.svg?label=Release)](https://github.com/sjatsh/beanstalkd-go/releases)
[![License](https://img.shields.io/github/license/sjatsh/beanstalkd-go)](https://github.com/sjatsh/beanstalkd-go)

## Description

- Simple and fast general purpose work queue.
- Fully [Beanstalk](https://github.com/beanstalkd/beanstalkd) compatible task queue implemented by golang
  purpose
- [ProtocolDescription](doc/protocol.zh-CN.md)

## Milepost

- *2020-11-14* : all dispatch cmd complete but memory only.
- *2020-11-15* : binlog persistence support

## Quick Start

using go get install

```bash
GO111MODULE=on GOPROXY=https://goproxy.cn/,direct go get -u -v github.com/sjatsh/beanstalkd-go
```

using make you self

```bash
make
make run    # run program
make test   # run go test
make clean  # del program and log dir
```

view support commands

```bash
./beanstalkd-go -h
```

```bash
Usage of ./beanstalkd-go:
  -F    never fsync
  -L string
        set the log level, switch one in (panic, fatal, error, warn, waring, info, debug, trace) (default "warn")
  -V    increase verbosity
  -b string
        write-ahead log directory
  -f int
        fsync at most once every MS milliseconds (default is 50ms);use -f0 for "always fsync" (default 50)
  -l string
        listen on address (default is 0.0.0.0) (default "0.0.0.0")
  -p int
        listen on port (default is 11400) (default 11400)
  -s int
        set the size of each write-ahead log file (default is 10485760);will be rounded up to a multiple of 4096 bytes (default 10485760)
  -u string
        become user and group
  -v    show version information
  -z int
        set the maximum job size in bytes (default is 65535);max allowed is 1073741824 bytes (default 65535)
```

## Third Party

- [Beanstalkd queue server console](https://github.com/xuri/aurora)
- [High available beanstalkd go client](https://github.com/tal-tech/go-queue) 