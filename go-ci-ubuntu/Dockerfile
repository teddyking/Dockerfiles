FROM ubuntu

RUN apt-get update
RUN apt-get -y install git wget build-essential iptables
RUN cd /usr/local && \
  wget https://storage.googleapis.com/golang/go1.7.linux-amd64.tar.gz && \
  tar -zxf go1.7.linux-amd64.tar.gz

RUN mkdir -p go/bin go/pkg go/src

ENV GOPATH /go
ENV PATH $PATH:/usr/local/go/bin

RUN go get -u github.com/onsi/ginkgo/ginkgo
RUN go get -u github.com/onsi/gomega
RUN go get -u github.com/tools/godep
RUN go get -u github.com/golang/lint/golint

