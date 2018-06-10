FROM golang:1.10.3-alpine3.7

RUN apk add --update git curl make gcc

RUN go get -u github.com/onsi/ginkgo/ginkgo
RUN go get -u github.com/onsi/ginkgo/
RUN go get -u github.com/onsi/gomega

RUN curl https://raw.githubusercontent.com/golang/dep/master/install.sh | sh
