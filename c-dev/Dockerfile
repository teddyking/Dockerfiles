FROM ubuntu:16.04

RUN apt-get update
RUN apt-get install -y build-essential curl git tmux vim-nox
RUN sh -c "useradd teddyking -d /home/teddyking -s /bin/bash -m"

USER teddyking
RUN curl vimfiles.luan.sh/install | bash
RUN curl "https://raw.githubusercontent.com/luan/dotfiles/master/tmux.conf" > /home/teddyking/.tmux.conf
RUN git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
RUN vim +slient +VimEnter +PlugInstall +qall
RUN mkdir -p /home/teddyking/workspace
RUN echo "export TERM=xterm-256color" >> /home/teddyking/.bashrc
