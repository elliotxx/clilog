![clilog](https://socialify.git.ci/elliotxx/clilog/image?font=Raleway&language=1&name=1&owner=1&pattern=Plus&theme=Light)

# clilog

[![Go Report Card](https://goreportcard.com/badge/github.com/elliotxx/clilog)](https://goreportcard.com/report/github.com/elliotxx/clilog)
[![GoDoc](https://godoc.org/github.com/elliotxx/clilog?status.svg)](https://godoc.org/github.com/elliotxx/clilog)
[![License](https://img.shields.io/github/license/elliotxx/clilog.svg)](https://github.com/elliotxx/clilog/blob/main/LICENSE)

A Go library for simple and pretty command-line logging

![image](https://github.com/user-attachments/assets/14380dbf-8a99-4eac-ba39-9d58239f4fc5)

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
	log.L(1).P("→").C(log.ColorCyan).Log("Item 1")
}
```

## Examples

### Basic Logging
```go
log.Info("Application started")
log.Warn("High memory usage detected")
log.Success("User login successful")
log.Error("Database connection failed")
```

### Hierarchical Logging
```go
log.Info("Processing order %d", 1234).
    L(1).P("→").C(log.ColorCyan).Log("Validating items").
    L(2).Info("Checking inventory").
    L(2).Success("Stock available").
    L(1).P("✓").C(log.ColorGreen).Log("Payment processing").
    L(1).Error("Shipping address invalid")
```

### Progress Indicator
```go
// Initialize progress bar
progress := log.New().L(1).P("▰").C(log.ColorBlue)

for i := 0; i <= 10; i++ {
    progress.Log("Loading: %s", strings.Repeat("▰", i))
    time.Sleep(300 * time.Millisecond)
}
```

### Formatted Data Display
```go
log.Info("User Profile:").
    L(1).Log("Name:    %s", log.Bold("Alice")).
    L(1).Log("Email:   %s", log.Bold("alice@example.com")).
    L(1).Log("Balance: %s", log.Bold("$1,234.56"))
```

### Disable Color Output
```go
log.SetNoColor(true)
log.Info("Running in CI environment")
```

## 👥 Who's using it

- [osp](https://github.com/elliotxx/osp)

## 🤝 Contributing

We welcome all forms of contributions! Whether it's new features, documentation improvements, or bug fixes. See our [Contributing Guide](CONTRIBUTING.md) for details.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

