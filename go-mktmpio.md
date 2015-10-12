---
title: go-mktmpio
---
# go-mktmpio

A simple Go library for accessing the mktmpio service. This is what powers our
official CLI, which also serves as our primary usage example.

<dl>
  <dt>GitHub</dt>
  <dd><a href="https://github.com/mktmpio/go-mktmpio">mktmpio/go-mktmpio</a></dd>
  <dt>GoDoc</dt>
  <dd><a href="https://godoc.org/github.com/mktmpio/go-mktmpio">github.com/mktmpio/go-mktmpio</a></dd>
</dl>

```go
package main

import (
  "fmt"
  "github.com/mktmpio/go-mktmpio"
)

func main() {
  client, err := mktmpio.NewClient()
  if err != nil {
    fmt.Printf("Error initializing client: %s\n", err)
    return
  }
  instance, err := client.Create("redis")
  if err != nil {
    fmt.Printf("Error creating instance: %s\n", err)
    return
  }
  defer func() {
    if err := instance.Destroy(); err != nil {
      fmt.Printf("Error terminating instance: %v\n", err)
    } else {
      fmt.Printf("Instance %s terminated.\n", instance.ID)
    }
  }()

  // Do stuff here
}
```
