# go_learn

### Download GO

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
