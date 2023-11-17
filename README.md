# wp-env-template

wp-env のテンプレートリポジトリです。

## テンプレートの構成

| Node.js | PHP    | WordPress |
| :------ | :----- | :-------- |
| 20.9.0  | 8.1 系 | 6.3.1     |

## 開発環境の構築

### Node.js

`.nvmrc` に記載されている Node.js のバージョンが動くようにしてください。

### Docker

Docker がインストール済みで、起動した状態であること。

### 構築手順

```
# 1. 依存関係のインストール
yarn
# 2. WordPressのセットアップ ※初回は少し時間がかかります。 Done! と表示されれば完了です。
yarn wp-env start
```

## URL 一覧

| 項目     | URL                            | その他                                        |
| -------- | ------------------------------ | --------------------------------------------- |
| サイト   | http://localhost:8000          | -                                             |
| 管理画面 | http://localhost:8000/wp-admin | ユーザー名: `admin`<br>パスワード: `password` |

## コマンド一覧

- WordPress を起動する

```
yarn wp-env start
```

- WordPress を停止する

```
yarn wp-env stop
```

- WordPress を再起動する(`.wp-env.json` ファイルを更新した場合)

```
yarn wp-env start --update
```

- WordPress を削除する(初期化したい場合)

```
yarn wp-env destroy
```

## その他

- WordPress のプラグインを追加する場合は、`.wp-env.json` の plugins に 追加したいプラグインの DL のリンクを追加する。<br>
  なお WordPress の起動中に `.wp-env.json` を更新した場合は反映されないので、WordPress の再起動(`yarn wp-env start --update`) のコマンドを叩く。
