FROM ubuntu_japanese

# インストールに必要なパッケージをインストール
RUN apt install -y \
    build-essential \
    libffi-dev \
    libffi7 \
    libgmp-dev \
    libgmp10 \
    libncurses-dev \
    libncurses5 \
    libtinfo5

# 作業ディレクトリを作成する
WORKDIR /root/work

# haskellをインストールする
RUN curl --proto '=https' --tlsv1.2 -sSf https://get-ghcup.haskell.org | sh

# PATHを通す
RUN echo "PATH=/root/.ghcup/bin/:$PATH" >> /root/.bashrc
