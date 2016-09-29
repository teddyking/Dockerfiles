# Dockerfiles

A collection of Dockerfiles that I use sometimes.

* c-dev - A largeish image used for developing C code.
  * FROM ubuntu.
  * Includes build-essential, curl, git and vimfiles.
* go-ci - A smallish image used for running CI of Go programs.
  * FROM alpine.
  * Includes go, ginkgo, gomega, godep and golint.
* go-ci-ubuntu - A largeish image used for running CI of Go programs.
  * FROM ubuntu.
  * Includes build-essential, iptables and wget.
  * Includes go, ginkgo, gomega, godep and golint.

