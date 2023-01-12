FROM ubuntu:latest

RUN apt update && apt install -y \
    sudo \
    wget \
    curl \
    vim \
    tzdata \
    locales && \
    locale-gen ja_JP.UTF-8

# vim setting
RUN echo '\n\
    set fenc=utf-8\n\
    set encoding=utf-8\n\
    set fileencodings=iso-2022-jp,euc-jp,sjis,utf-8\n\
    set fileformats=unix,dos,mac\n\
    syntax on' >> /root/.vimrc

ENV TZ Asia/Tokyo
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
