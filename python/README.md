# python

python環境構築用のDockerfile

元にするイメージは[ubuntu_japanese](https://github.com/geshi-prog/dockerfiles/tree/main/ubuntu_japanese)で作成したイメージを元にしています。

ですのでまずは、ubuntu_japaneseのイメージを作成してもらえればと思います。

```shell
// イメージを作成
docker image build --tag python .
// コンテナを作成する(jupyter用に8888ポートを開放しています。)
docker container run -p 8888:8888 --name python_container -it python 
```

## jupyter notebookの起動

```shell
jupyter notebook --allow-root --ip=0.0.0.0
```
このコマンドで?token=<token>の箇所があるので<token>をメモします。
http://127.0.0.1:8888/ に移動すると下記の画面が表示されるのでtokenと設定したいパスワードを入力するとログインが可能です。
![image](https://user-images.githubusercontent.com/66429160/212205383-66a30146-42d3-4fab-833f-d9186b0ce000.png)

## 参照ページ
https://www.python.jp/install/ubuntu/index.html
