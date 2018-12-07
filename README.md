# glci-demo
Demo of bad interaction between golangci-lint and quicktemplate

Usage:

    go get -u github.com/valyala/quicktemplate
    go get -u github.com/valyala/quicktemplate/qtc
    go get -u golang.org/x/lint/golint
    go get -u github.com/golangci/golangci-lint/...
    export PATH="$PATH:$GOPATH/bin"

    go get -u -d github.com/aaron42net/glci-demo
    cd $GOPATH/src/github.com/aaron42net/glci-demo
    go generate ./...

    golint ./...
    go vet ./...
    golangci-lint run --no-config --disable-all -E golint -E govet
