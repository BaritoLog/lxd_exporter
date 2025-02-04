# lxd_exporter

[![Build Status](https://travis-ci.org/BaritoLog/lxd_exporter.svg?branch=master)](https://travis-ci.org/BaritoLog/lxd_exporter)

LXD metrics exporter for Prometheus. Improved version of [viveksing/lxdexporter_golang](https://github.com/viveksing/lxdexporter_golang).

## Usage

Download latest precompiled binary of this exporter from [the release page](https://github.com/BaritoLog/lxd_exporter/releases).

Extract archive, then run the exporter:
```
./lxd_exporter
```

The exporter must have access to LXD socket which can be guided by:
- Specifying `LXD_SOCKET` environment variable to LXD socket path, or
- Specifying `LXD_DIR` environment variable to LXD socket's parent directory.

For more information, you can see the documentation from [Go LXD client library](https://godoc.org/github.com/lxc/lxd/client#ConnectLXDUnix).

## Hacking

Install [Go](https://golang.org/dl) before hacking this library.

To run all tests:
```
go test ./...
```

To build exporter binary:
```
mkdir build
go build -o build ./...
```

Binary will be available on `build/` directory.

## License

[MIT](LICENSE).
