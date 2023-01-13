FROM ubuntu_japanese

# GOのパッケージの一部ではgitを使用するのでインストール
RUN apt install -y \
    git

# goのバージョン(https://go.dev/dl/ からバージョンは確認する)
ARG go_version="1.19.5"

# 作業ディレクトリを作成する
WORKDIR /root/work

# goをビルドする
RUN wget https://go.dev/dl/go${go_version}.linux-amd64.tar.gz
RUN tar -C /usr/local -xzf go${go_version}.linux-amd64.tar.gz

# pathを通す
RUN echo 'export PATH=/usr/local/go/bin:$PATH' >> /root/.bashrc
