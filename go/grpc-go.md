1.  Install the protocol compiler plugins for Go
```
go get -u google.golang.org/protobuf/cmd/protoc-gen-go@v1.26
go get -u google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.1
```

3.  Export path golang
```
export GOROOT=/usr/local/go
export GOPATH=$HOME/go
export GOBIN=$GOPATH/bin
export PATH=$PATH:$GOROOT:$GOPATH:$GOBIN
```
