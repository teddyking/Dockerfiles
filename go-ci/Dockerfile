FROM alpine

RUN apk add --update git
RUN apk add --update go
RUN rm -rf /var/cache/apk/*

RUN mkdir -p go/bin go/pkg go/src

ENV GOPATH /go

RUN go get -u github.com/onsi/ginkgo/ginkgo
RUN go get -u github.com/onsi/gomega
RUN go get -u github.com/tools/godep
RUN go get -u github.com/golang/lint/golint

