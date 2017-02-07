FROM golang:1.7.5

RUN apt-get -y update
RUN apt-get -y install libseccomp-dev libseccomp2
RUN go get -d github.com/opencontainers/runc
RUN go get -u github.com/golang/dep/...
RUN go get -u github.com/onsi/ginkgo/ginkgo
RUN cd src/github.com/opencontainers/runc && \
  make && \
  mv runc /usr/local/bin/
