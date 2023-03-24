# go_learn

# Index

## - [Download GO](#download-go)

## - [GO modules learn](#go-modules-learn)

## - [Return and handle an error](#return-and-handle-an-error)

# Download GO

How to download GO version 1.20.2

```shell

sudo apt-get update
wget https://golang.org/dl/go1.20.2.linux-amd64.tar.gz
sha256sum go1.20.2.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.20.2.linux-amd64.tar.gz
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc
echo 'export GOPATH=$HOME/go' >> ~/.bashrc
echo 'export PATH=$PATH:$GOPATH/bin' >> ~/.bashrc
source ~/.bashrc
go version

```

## - [Index](#index)

# GO modules learn

Learn how to call your code from another module

Structure:

```shell
go_modules_learn/
|-- greetings/
|-- hello/
```

Expected output:

```shell
Hi, Gladys. Welcome!
```

#### [GO MODULES LEARN PAGE](go_modules_learn/go_modules_learn.md)

## - [Index](#index)

# Return and handle an error

Learn how to return and handle and error

Structure:

```shell
go_modules_learn/
|-- greetings/
|-- hello/
```

Expected output:

```shell
greetings: empty name
exit status 1
```

#### [GO RETURN AND HANDLE AN ERROR PAGE](return_and_handle_an_error/return_and_handle_an_error.md)

## - [Index](#index)