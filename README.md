# getparty [![Build Status](https://travis-ci.org/vbauerster/getparty.svg?branch=master)](https://travis-ci.org/vbauerster/getparty)

Console download manager

![showcase](showcase.gif)

## Installation
`getparty` requires Go 1.7 or later.
```
$ go install github.com/vbauerster/getparty/cmd/getparty
```
Or download [binary](https://github.com/vbauerster/getparty/releases/latest).

## Usage

```
Usage:
  getparty [OPTIONS] url

Application Options:
  -p, --parts=              number of parts (default: 2)
  -t, --timeout=            download timeout in seconds
  -o, --output-file=NAME    force output file name
  -c, --continue=JSON       resume download from the last saved json file
  -m, --best-mirror         pickup the fastest mirror. Will read from stdin
      --version             show version

Help Options:
  -h, --help                Show this help message
```

#### Best mirror example:

`cat` [mirrors.txt](https://github.com/vbauerster/getparty/blob/master/cmd/getparty/mirrors.txt) `| getparty -p 8 -m`

## License

[BSD 3-Clause](https://opensource.org/licenses/BSD-3-Clause)
