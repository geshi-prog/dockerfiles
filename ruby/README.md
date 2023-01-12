# ruby

ruby環境構築用のDockerfile

元にするイメージは[ubuntu_japanese](https://github.com/geshi-prog/dockerfiles/tree/main/ubuntu_japanese)で作成したイメージを元にしています。

ですのでまずは、ubuntu_japaneseのイメージを作成してもらえればと思います。

```shell
// イメージを作成
docker image build --tag ruby . 
```

## 参照ページ
https://qiita.com/kerupani129/items/77dd1e3390b53f4e97b2
