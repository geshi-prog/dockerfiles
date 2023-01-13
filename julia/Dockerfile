FROM ubuntu_japanese

# juliaのバージョン(https://julialang.org/downloads/ からバージョンは確認する)
ARG julia_parent_version="1.8"
ARG julia_version="1.8.5"

# 作業ディレクトリを作成する
WORKDIR /root/work

# juliaをビルドする
RUN wget https://julialang-s3.julialang.org/bin/linux/x64/${julia_parent_version}/julia-${julia_version}-linux-x86_64.tar.gz
RUN tar -C /usr/local -xzf julia-${julia_version}-linux-x86_64.tar.gz

# pathを通すjuliaのバージョンを渡すために一度.bashrcに書きたい内容を変数に格納して渡す
ARG julia_path="export PATH=/usr/local/julia-${julia_version}/bin/:$PATH"
RUN echo ${julia_path} >> /root/.bashrc
