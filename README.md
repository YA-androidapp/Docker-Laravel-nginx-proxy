# Docker-Laravel-MultiApp

---

## .env の作成

```sh
$ mv .env.sample .env
$ nano ./.env
```

## docker-compose.yml の編集

```sh
$ nano ./docker-compose.yml
```

## コンテナの起動

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
