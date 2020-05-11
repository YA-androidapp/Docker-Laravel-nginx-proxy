# Docker-Laravel-MultiApp

---

## プロキシ側の設定

## .env の作成

```sh
$ mv .env.sample .env
$ nano ./.env
```

### docker-compose.yml の編集

```sh
$ nano ./docker-compose.yml
```

### コンテナの起動

```sh
$ ./start.sh
```

```sh
$ docker ps
```

| IMAGE                                  | PORTS                                    | NAMES             |
| -------------------------------------- | ---------------------------------------- | ----------------- |
| nginx                                  | 0.0.0.0:80->80/tcp, 0.0.0.0:443->443/tcp | nginx-web         |
| jwilder/docker-gen                     |                                          | nginx-gen         |
| jrcs/letsencrypt-nginx-proxy-companion |                                          | nginx-letsencrypt |

## Web アプリを追加

### ホスト名の修正

`./app1/` （app1 はサブドメインと揃える）配下のファイルに含まれる `EXAMPLE.NET` を、設置するホストのドメインに変更

### コンテナの起動

```sh
$ docker-compose up -d
```
