FROM golang:1.7.5

RUN apt-get -y update
RUN apt-get -y install libseccomp-dev libseccomp2
RUN go get -d github.com/opencontainers/runc
RUN go get -d github.com/opencontainers/runtime-tools/cmd/oci-runtime-tool
RUN curl https://glide.sh/get | sh
RUN go get -u github.com/golang/dep/...
RUN go get -u github.com/onsi/ginkgo/ginkgo
RUN cd /go/src/github.com/opencontainers/runc && \
  make && \
  mv runc /usr/local/bin/
RUN cd /go/src/github.com/opencontainers/runtime-tools && \
  make && \
  mv oci-runtime-tool /usr/local/bin/
