FROM ubuntu:16.04

RUN apt-get update
RUN apt-get install -y build-essential curl git vim-nox
RUN sh -c "useradd teddyking -d /home/teddyking -s /bin/bash -m"

USER teddyking
RUN curl vimfiles.luan.sh/install | bash
RUN vim +slient +VimEnter +PlugInstall +qall
RUN mkdir -p /home/teddyking/workspace
