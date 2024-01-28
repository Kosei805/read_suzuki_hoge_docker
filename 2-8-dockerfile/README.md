# Dockerfileの基本とコマンド

## Dockerfileの紹介:
- Dockerfileは、Dockerイメージを構築するための一連の命令です。
- ベースイメージ、実行するコマンド、コピーするファイル、デフォルトのコマンドを指定します。

## 基本的なDockerfileの命令:

### FROM:
- ベースイメージを指定します。
- 例: `FROM ubuntu:latest`.

### RUN:
- Linuxコマンドを実行してレイヤーを作成します。
- 例: `RUN apt-get update && apt-get install -y nginx`.

### COPY:
- ホストマシンからファイルをイメージに追加します。
- 例: `COPY index.html /var/www/html/`.

### CMD:
- イメージのデフォルトのコマンドを設定します。
- 例: `CMD ["nginx", "-g", "daemon off;"]`.

## Dockerfileの作成:
- カレントディレクトリにDockerfileを作成します。
- 任意のテキストエディタを使用して作成します。

### サンプルDockerfile:
```Dockerfile
FROM ubuntu:latest
RUN apt-get update && apt-get install -y nginx
COPY index.html /var/www/html/
CMD ["nginx", "-g", "daemon off;"]
```

## イメージのビルド:
- `docker image build`コマンドを使用してイメージをビルドします。
- 必要に応じてパスとCOPYを調整します。
- タグオプションを指定して識別しやすくします。
- 例: `docker image build --tag MyUbuntu:Tag .`

## イメージのレイヤーを確認:
- `docker image history`コマンドを使用してイメージのレイヤーを確認します。
- レイヤーは下から上に構築され、最終的なレイヤーにはイメージIDが含まれます。
- 例: `docker image history MyUbuntu:Tag`

## RUNコマンドの考慮事項:
- RUNで確定するレイヤーの粒度を決定します。
- イメージのサイズやキャッシュなどの利点、デバッグの難しさなどを考慮します。
- レイヤーを適切に確定することで、イメージの最適化が可能です。

## DockerHubのレイヤー情報の違い:
- DockerHubはイメージのレイヤー情報を表示しますが、実際のDockerfileの内容とは異なる場合があります。
- DockerHubはFROMで指定したベースイメージに追加されるレイヤーを表示します。
- この違いを理解することは、イメージの最適化やデバッグに重要です。
