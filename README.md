# Timer

[![Go Reference](https://pkg.go.dev/badge/github.com/gmodx/timer.svg)](https://pkg.go.dev/github.com/gmodx/timer)

The `timer` package provides a simple way to schedule and execute functions at specified intervals.

## Installation

To use this package in your Go project, you can install it using `go get`:

```sh
go get github.com/gmodx/timer
```

## Usage
Here's a basic example of how to use the timer package to schedule and execute functions at specified intervals:

``` go
package main

import (
	"fmt"
	"github.com/gmodx/timer"
	"time"
)

func main() {
	// Define a function to be executed.
	jobFunc := func(message string) {
		fmt.Println("Job executed:", message)
	}

	// Schedule the function to be executed every 2 seconds with a 1-second delay.
	err := timer.Tick(time.Second, 2*time.Second, jobFunc, "Hello, World!")
	if err != nil {
		fmt.Println("Error:", err)
	}

	// Keep the program running for demonstration purposes.
	select {}
}
```

## Documentation
For more information and usage examples, please refer to the GoDoc documentation.

