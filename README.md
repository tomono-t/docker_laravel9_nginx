# docker_laravel9_nginx
個人用のlaravel9のSandbox用環境

以下の記事にかかれている内容を使用

https://qiita.com/ucan-lab/items/56c9dc3cf2e6762672f4

## 環境構築手順

```sh

git clone git@github.com:tomono-t/docker_laravel9_nginx.git

cd docker_laravel9_nginx

docker compose up -d

docker compose exec app bash

```

```sh
chmod -R 777 storage bootstrap/cache

composer install

cp .env.example .env

php artisan key:generate

php artisan storage:link

php artisan migrate

```
