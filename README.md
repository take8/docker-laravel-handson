# docker-laravel-handson

[こちらの記事](https://qiita.com/ucan-lab/items/56c9dc3cf2e6762672f4)を見ながら写経しました。

## 環境構築

```sh
docker compose up -d --build

docker compose exec app bash
composer install
```

```sh
cp .env.example .env
```

`DB_PASSWORD` を記載する。
`infra/mysql/Dockerfile` を参照。

```sh
php artisan key:generate
php artisan storage:link
chmod -R 777 storage bootstrap/cache
```

## 接続確認

http://127.0.0.1:8080/
