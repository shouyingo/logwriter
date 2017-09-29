# logwriter
支持文件滚动的 Writer

## install
```
go get github.com/shouyingo/logwriter
```

## usage
```go
package main

import (
	"github.com/shouyingo/logwriter"
)

func main() {
	// create roll.log at log directory.
	// each log file limits 50MB.
	// max 10 files.
	w := logwriter.New("log/roll.log", 50*1024*1024, 10)
	w.Write([]byte("hello world\n"))
	w.Sync()
}
```
