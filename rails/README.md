# rails

ruby on rails環境構築用のDockerfile

元にするイメージはubuntu_japaneseで作成したイメージを元にしています。

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

