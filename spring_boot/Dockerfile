FROM ubuntu_japanese

# バージョンを設定する
ARG gradle_version="7.5.1"
ARG maven_version="3.8.7"

# javaをインストール
RUN apt install -y \
    default-jre \
    default-jdk \
    git \
    unzip

# 作業ディレクトリを作成する
WORKDIR /root/work

# gradleをインストールする
RUN wget https://services.gradle.org/distributions/gradle-${gradle_version}-bin.zip
RUN unzip -d /opt/gradle ./gradle-${gradle_version}-bin.zip

# mavenをインストールする
RUN wget https://dlcdn.apache.org/maven/maven-3/${maven_version}/binaries/apache-maven-${maven_version}-bin.zip
RUN unzip -d /opt/maven ./apache-maven-${maven_version}-bin.zip

# PATHを通す
ARG path="PATH=/opt/gradle/gradle-${gradle_version}/bin/:/opt/maven/apache-maven-${maven_version}/bin/:$PATH"
RUN echo ${path} >> /root/.bashrc
