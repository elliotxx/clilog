# clilog

A Go library for clear and pretty command-line logging

## Features

- Hierarchical logging with indentation
- Built-in log levels (Debug/Info/Warn/Success/Error)
- Customizable prefixes and colors
- Bold text formatting
- Verbose mode control
- Color output toggle

## Installation

```bash
go get github.com/elliotxx/clilog
```

## Usage
```go
package main

import (
	"github.com/elliotxx/clilog"
)

func main() {
	log.SetVerbose(true)
	log.Info("Processing items")
	log.L(1).P("→").C(log.ColorCyan).Log("Item 1")
	log.L(1).Success("Done")
}
```
