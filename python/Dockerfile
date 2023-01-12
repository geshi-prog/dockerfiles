FROM ubuntu_japanese

# インストールに必要な物をインストール
RUN apt install -y \
    build-essential \
    libbz2-dev \
    libdb-dev \
    libreadline-dev \
    libffi-dev \
    libgdbm-dev \
    liblzma-dev \
    libncursesw5-dev \
    libsqlite3-dev \
    libssl-dev \
    zlib1g-dev \
    uuid-dev \
    tk-dev

# pythonのバージョン
ARG python_version="3.11.1"

# 作業ディレクトリを作成する
WORKDIR /root/work

# pythonをビルドする
RUN wget https://www.python.org/ftp/python/${python_version}/Python-${python_version}.tar.xz
RUN tar xJf Python-${python_version}.tar.xz
RUN cd Python-${python_version}
RUN /root/work/Python-${python_version}/configure
RUN make
RUN make install

# pipのアップグレード
RUN python3 -m pip install --upgrade pip

# jupyter notebookのインストール
RUN python3 -m pip install notebook

# エイリアスを変更する。
RUN echo 'alias python=python3' >> /root/.bashrc
RUN echo "alias pip='python3 -m pip'" >> /root/.bashrc
