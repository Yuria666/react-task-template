# react-task-template

フロントエンドフレームワーク課題のボイラーテンプレートです。
このファイルを手元の PC に取り込んで、課題を実施するようにしてください。

## 全体構成

- フロントエンド
  - React.js
- バックエンド
  - Laravel API
- DB
  - MySQL

全てコンテナ環境で稼働できるように構成しています。
今回の課題ではこの構成のフロントエンド開発を担当してもらいます。

![課題の全体構成](./task_architecture.png)

## 環境構築

- `node.js`のインストール
- `docker`のインストール
- `src/laravel/.env`に下記リンクの環境変数を上書きする
  - https://www.notion.so/plantsprogramming/bd282fcbc78045d8a4488dde4c8cb312#98ffd52be53947b090346637bb32dde1
- `docker-compose.yml`のあるディレクトリで下記コマンド実施
  - `docker-compose up -d`
- Laravel コンテナ内でマイグレーションの実行し、テーブル作成
  - `docker exec -it laravel bash`
  - `php artisan migrate`

※Laravel に関するライブラリのインストールは不要です。

## フロントエンド

React.js\* TypeScript を利用した Web アプリケーションです
`src/client`配下がフロントエンドのディレクトリになります。

### ディレクトリ構成

```
- src
  - pages
    - ページコンポーネント置き場
  - components/{コンポーネント単位}
    - 各種コンポーネント置き場
  - tests/{page区分}
   - テスト用ファイル置き場
```

### コンポーネント管理について

コンポーネント管理に Atomic Design を採用しています。
コンポーネントの粒度に合わせて、適切なディレクトリに格納していく形にしてください。

※Atomic Design については[こちら](https://blog.spacemarket.com/code/atomic-design%E3%82%92%E4%BD%BF%E3%81%A3%E3%81%A6react%E3%82%B3%E3%83%B3%E3%83%9D%E3%83%BC%E3%83%8D%E3%83%B3%E3%83%88%E3%82%92%E5%86%8D%E8%A8%AD%E8%A8%88%E3%81%97%E3%81%9F%E8%A9%B1/)を参照

### テストについて

テストコードは全て tests ディレクトリに格納します。

## バックエンド

Laravel を用いた API です。
`src/laravel`配下がバックエンドのディレクトリになります。

本課題では触ることはありませんが、最初の環境構築時に何点かセットアップが必要です。
[環境構築](#環境構築)セクションを参考にセットアップしてください。
