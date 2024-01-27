# コンテナ基本操作に関する会話のまとめ

## コンテナの起動
新コマンド: `docker run <イメージ名>`
旧コマンド: `docker <イメージ名>`

## コンテナの一覧確認
新コマンド: `docker container ls`
旧コマンド: `docker ps`
オプション: `--all` - すべてのコンテナを表示

## コンテナの停止
新コマンド: `docker container stop <コンテナ名>`
旧コマンド: `docker stop <コンテナ名>`
オプション: `-f`または`--force` - 強制停止

## 起動中のコンテナの一覧確認
正しいコマンド: `docker container ls`または`docker container ls -a`

## 起動中のコンテナの停止および削除
- containerは軽量なのでいちいち停止せず、こちらで削除し、改めて起動するという方が多い

コマンド: `docker container rm -f <コンテナ名またはコンテナID>`
