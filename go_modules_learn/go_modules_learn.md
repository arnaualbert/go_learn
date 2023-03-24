### GO modules learn

First we create the folder greetings and we create the go mod file

to track the dependencies

```shell
mkdir greetings
cd greetings
go mod init example.com/greetings
```

Thats the code of the greetings.go

```go
package greetings

import "fmt"

// Hello returns a greeting for the named person.
func Hello(name string) string {
    // Return a greeting that embeds the name in a message.
    message := fmt.Sprintf("Hi, %v. Welcome!", name)
    return message
}
```

