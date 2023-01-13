# julia

julia環境構築用のDockerfile

元にするイメージは[ubuntu_japanese](https://github.com/geshi-prog/dockerfiles/tree/main/ubuntu_japanese)で作成したイメージを元にしています。

ですのでまずは、ubuntu_japaneseのイメージを作成してもらえればと思います。

```shell
// イメージを作成
docker image build --tag julia .
```

