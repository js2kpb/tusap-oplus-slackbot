# oplus-SlackBot
このリポジトリは、[oplus](https://opluswork.com/)のシフト情報をSlackに通知するBOTです。

## 技術スタック
| 技術           | 説明                                      |
|----------------|-------------------------------------------|
| 言語           | TypeScript                                |
| ランタイム     | Bun                                       |
| フレームワーク | Hono                                       |
| データベース   | PostgreSQL                                 |
| コンテナ化     | Docker                                     |
| メッセージング | Slack API                                  |

## Docker

### ビルドと開始

以下のコマンドでDockerコンテナをビルドして開始します:

```sh
docker-compose up --build
```
##### オプション

以下のオプションを使用してDockerコンテナをカスタマイズできます:

- `-d`: バックグラウンドでコンテナを実行します。
- `--watch`:
### ビルドと開始

以下のコマンドでDockerコンテナをビルドして開始します:

```sh
docker-compose up --build
```
##### オプション

以下のオプションを使用してDockerコンテナをカスタマイズできます:

- `-d`: バックグラウンドでコンテナを実行します。
- `--watch`: ファイルの変更を監視し、自動的に再ビルドします。

### 停止

以下のコマンドでDockerコンテナを停止します:

```sh
docker-compose down
```

#### オプション
以下のオプションを使用してDockerコンテナをカスタマイズできます:

- `--rmi all`: すべてのイメージを削除します。
- `-v`: ボリュームを削除します。

  >[!CAUTION]
  >DBのデータが全て消えるので注意

### 環境変数
下記の値を各自`.env`に設定してください

```
POSTGRES_USER=admin
POSTGRES_PASSWORD=password
DB_PORT=5433
```
