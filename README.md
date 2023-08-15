# 開発者向け情報
開発に関わる仕様を以下にまとめます。

## 開発環境
本プロジェクトの環境は以下になります。
| App名 | バージョン | インストール条件 |
|:-- |:--:|:--:|
| Ruby | [.ruby-version](https://github.com/futaro0405/rails-docker/blob/docker/.ruby-version) | 必須 |
| postgres | 12 | 必須 |
| docker-compose | 3.9 | 必須 |
| Ruby on Rails | 7.0.6 | 必須 |
| Docker |  | 必須 |
| [Visual Studio Code](https://code.visualstudio.com/) |  | 推奨 |
| [Docker Desctop](https://www.docker.com/products/docker-desktop/) |  | 推奨 |

## 開発環境構築
環境構築には次のコマンドを実行します。
### 1 本リポジトリをcloneする
```
git clone https://github.com/futaro0405/rails-docker.git
```

### 2 docker imageをbuildする
```
docker-compose build
```

### 3 docker containerを作成・起動する
```
docker-compose up -d
```

### 4 起動したdocker containerでbashシェルを開始する
```
docker-compose exec web bash
```

#### 4.1 bashシェル内でDBを作成する
```
rails db:create
```

#### 4.2 bashシェル内でDBを更新する
```
rails db:migrate
```

### 5 プラウザでlocalhost:3000にアクセスする

## コマンド一覧
開発時は以下コマンドを適切に実行してください。

| コマンド | 用途 |
|:--|:--|
| docker-compose build | docker imageの作成 |
| docker-compose up | docker containerを作成して起動<br>`-d`オプション : デタッチモード<br>`--build`オプション : docker imageのビルドから作成 |
| docker-compose stop | docker containerを停止 |
| docker-compose down | docker containerを停止＆削除 |
