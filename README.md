# ansible-docker

## build方法

``` shell
cd app
docker build -t hidepin/ansible .
```

## 実行方法

``` shell
cd (playbookディレクトリ)
docker run --rm -it -v (ホスト上のplaybookディレクトリ):/playbook hidepin/ansible ansible-playbook site.yml
```
