# spring_boot

javaとspring_boot環境構築用のDockerfile

元にするイメージは[ubuntu_japanese](https://github.com/geshi-prog/dockerfiles/tree/main/ubuntu_japanese)で作成したイメージを元にしています。

ですのでまずは、ubuntu_japaneseのイメージを作成してもらえればと思います。

```shell
// イメージを作成
docker image build --tag spring_boot .
// コンテナを作成
docker container run -p 8080:8080 --name spring_boot_app -it spring_boot
```
