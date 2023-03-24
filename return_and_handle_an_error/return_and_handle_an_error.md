### Return and handle an error

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

import (
	"errors"
	"fmt"
)

// Hello returns a greeting for the named person.
func Hello(name string) (string, error) {
	// If no name was given, return an error with a message.
	if name == "" {
		return "", errors.New("empty name")
	}

	// If a name was received, return a value that embeds the name
	// in a greeting message.
	message := fmt.Sprintf("Hi, %v. Welcome!", name)
	return message, nil
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
	"log"

	"example.com/greetings"
)

func main() {
	// Set properties of the predefined Logger, including
	// the log entry prefix and a flag to disable printing
	// the time, source file, and line number.
	log.SetPrefix("greetings: ")
	log.SetFlags(0)

	// Request a greeting message.
	message, err := greetings.Hello("")

	// If an error was returned, print it to the console and
	// exit the program.
	if err != nil {
		log.Fatal(err)
	}

	// If no error was returned, print the returned message
	// to the console.
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