FROM ubuntu_japanese

# 選択を自動化させるためにexpectをインストール
RUN apt install -y expect

# rustをインストール
COPY install_rust.sh /root/
RUN sh /root/install_rust.sh
RUN /root/.cargo/bin/rustup default stable

# pathを通す
RUN echo "PATH=/root/.cargo/bin/:$PATH" >> /root/.bashrc
