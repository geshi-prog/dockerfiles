FROM ubuntu_japanese

# インストールに必要な物をインストール
RUN apt install -y \
    git \
    gcc \
    make \
    libssl-dev \
    zlib1g-dev

# rubyのバージョン
ARG ruby_version="3.1.2"
# railsのバージョン
ARG rails_version="7.0.4"
# bundlerのバージョン
ARG bundler_version="2.3.14"

# 作業ディレクトリを作成する
WORKDIR /root/work

# rbenvをクローンする
RUN git clone --depth 1 https://github.com/rbenv/rbenv.git /root/.rbenv
RUN git clone https://github.com/rbenv/ruby-build.git /root/.rbenv/plugins/ruby-build

# 環境変数にrbenvを追加する
RUN echo 'PATH="/root/.rbenv/bin:$PATH"' >> /root/.bashrc
RUN echo 'eval "$(rbenv init - bash)"' >> /root/.bashrc

# rubyをインストールする
# ビルド時には~/.bashrcが読み込まれないので直接pathを指定する
RUN /root/.rbenv/bin/rbenv install ${ruby_version}
RUN /root/.rbenv/bin/rbenv global ${ruby_version}

# railsをインストールする
RUN /root/.rbenv/shims/gem install rails -v ${rails_version}

# gemの依存関係を管理するためにbundlerをインストール
RUN /root/.rbenv/shims/gem install bundler -v ${bundler_version}
