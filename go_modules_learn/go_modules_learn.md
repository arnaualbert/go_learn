### GO modules learn

First we create the folder greetings and we create the go mod file

to track the dependencies

```shell
mkdir greetings
cd greetings
go mod init example.com/greetings
```

That's the code of the greetings.go

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

Now we create the folder hello and all the necessary files

```shell
cd ..
mkdir hello
cd hello
go mod init example.com/hello
```

That's the code of the hello.go

```go
package main

import (
    "fmt"

    "example.com/greetings"
)

func main() {
    // Get a greeting message and print it.
    message := greetings.Hello("Gladys")
    fmt.Println(message)
}
```

Go to the shell again

```shell
go mod edit -replace example.com/greetings=../greetings
go mod tidy
```

Now you can run the code like this:

```shell
go run .
```
#### [HOME PAGE](../README.md)

