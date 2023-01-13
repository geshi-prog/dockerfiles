# Django

django環境構築用のDockerfile

元にするイメージは[ubuntu_japanese](https://github.com/geshi-prog/dockerfiles/tree/main/ubuntu_japanese)で作成したイメージを元にしています。

ですのでまずは、ubuntu_japaneseのイメージを作成してもらえればと思います。

```shell
// イメージを作成
docker image build --tag django .
// コンテナを作成する
docker container run -p 8000:8000 --name django_app -it django 
```

## djangoを起動(helloアプリの場合)

```shell
root@6c4ee3be843d:~/work# django-admin startproject hello
root@6c4ee3be843d:~/work# cd hello
root@6c4ee3be843d:~/work/hello# python manage.py migrate
root@6c4ee3be843d:~/work/hello# python manage.py runserver 0.0.0.0:8000 --settings=hello.settings
```

以上のコマンドを実行した後に http://127.0.0.1:8000/ に移動すると下記の様にdjangoアプリが立ち上がっているかと思います。
