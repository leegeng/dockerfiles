FROM ubuntu:16.04

LABEL maintainer="kyoungwon.lee86@gmail.com"

RUN apt-get update

RUN apt-get upgrade -y

RUN apt-get install -y \
    curl \
    software-properties-common \
    git \
    make \
    build-essential \
    libssl-dev \
    zlib1g-dev \
    libbz2-dev \
    libreadline-dev \
    libsqlite3-dev \
    wget \
    llvm \
    libncurses5-dev \
    libncursesw5-dev \
    xz-utils \
    tk-dev

RUN git clone https://github.com/pyenv/pyenv.git ~/.pyenv

ENV HOME /root

ENV PYENV_ROOT $HOME/.pyenv

ENV PATH $PYENV_ROOT/shims:$PYENV_ROOT/bin:$PATH

RUN pyenv install 3.6.3
RUN pyenv global 3.6.3
RUN pyenv rehash

RUN pip install pip --upgrade

RUN pip install django==2.0