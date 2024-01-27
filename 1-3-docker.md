# Dockerと関連サービスについての詳細まとめ

## Dockerの基本要素

### 1. Docker Engine
- コンテナを載せるソフトウェア。
  
### 2. Docker CLI
- コンテナなどを操作するためのコマンドラインツール。

### 3. Docker Desktop
- LinuxカーネルやDockerが組み込まれたGUIアプリケーション。
- WindowsやMacでDockerを簡単に利用するための便利な統合環境。

### 4. Docker Compose
- 複数のコンテナやネットワークの構築を一括で管理するツール。
- YAMLファイルを使用して複雑な構成を簡単に再現可能。

### 5. DockerHub
- Dockerのイメージレジストリで、SaaSサービス。
- 公開されたイメージを共有したり、プル・プッシュしたりするための場所。

## コンテナ管理サービス

### 1. ECS-GKE
- Amazon Elastic Container Service (ECS) と Google Kubernetes Engine (GKE)。
- Docker Engineに入ったコンテナを管理するサービス。
- オーケストレーションにより、ロードバランスやスケーリングが容易に実現。

## 非公開のImage Registry

### 1. ECR-GCR
- Amazon Elastic Container Registry (ECR) と Google Container Registry (GCR)。
- 商用サービスのイメージを非公開にして保存・管理するためのレジストリ。
- プライベートなDockerHubのような利用が可能。

## Kubernetes

### 1. Kubernetes
- オーケストレーションソフトウェアで、コンテナの管理を担当。
- `kubectl`で始まるコマンドを提供。
- ロードバランスの作成やスケーリングなどが簡単に実現可能。

## その他

- Docker ComposeやKubernetesは、通常のローカル環境の開発において必要ないこともある。
