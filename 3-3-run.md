# Docker のセットアップとデバッグについてのノート

## セットアップ

セットアップされているイメージは、基本的にデフォルト命令で起動します。環境変数の指定が必要な場合は稀にあります。DockerHubの該当イメージのトップページに行くと解説があることが多いです。起動する際は、ベースイメージの機能か、Docker の機能か、特定のイメージの機能かを意識すると活用できます。

特定のサービスにアクセスする場合、EXECでBASHを起動し、次にサービスにセットアップします。また、ホストマシンから直接サービスに接続する場合もあります。この場合は、最短で繋がるというメリットがありますが、デバッグのためのポート解放が必要で、ホストマシンのセットアップも必要になります。

## デバッグ

コンテナが起動しない場合は、大きく分けて理由が2つあります。どこかの状態操作に不備があるか、イメージや命令に不備があるかです。デバッグ時には、デタッチオプションを外して出力を隠さないようにすると良いでしょう。設定ファイルが間違っている場合もありますが、これはドッカーとはあまり関係ないことがあります。

イメージが悪い場合でも、必ずしも失敗しないことに留意します。問題の発覚タイミングと設定ファイルの内容を関連付けるためにも、図を描いて相関を把握する練習を行いましょう。

## ポイント

- 何らかの機能がなにに提供されているかを整理すると使いこなしやすい
- コンテナが起動しないときは、起動コマンドが悪いのかイメージが悪いのかをまず考える
    - 前者であれば、出力をよくみて文法や状態を確認する
    - 後者であれば、出力をよく見てイメージを確認する