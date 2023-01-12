# rails

ruby on rails環境構築用のDockerfile

元にするイメージは[ubuntu_japanese](https://github.com/geshi-prog/dockerfiles/tree/main/ubuntu_japanese)で作成したイメージを元にしています。
ですのでまずは、ubuntu_japaneseのイメージを変更してもらえればと思います。

```shell
// イメージを作成
docker image build --tag rails .
// コンテナを作成する
docker container run -p 3000:3000 --name rails_app -it rails 
```

## railsを起動(helloアプリの場合)

```shell
root@6c4ee3be843d:~/work# rails new hello
root@6c4ee3be843d:~/work# cd hello
root@6c4ee3be843d:~/work/hello# bundle
root@6c4ee3be843d:~/work/hello# rails server -b 0.0.0.0
```

以上のコマンドを実行した後に http://127.0.0.1:3000/ に移動すると下記の様にrailsアプリが立ち上がっているかと思います。
![image](https://user-images.githubusercontent.com/66429160/212195676-7de2f507-5368-45f0-8f79-a6af2c5e1569.png)

## 参照ページ
https://qiita.com/kerupani129/items/77dd1e3390b53f4e97b2
