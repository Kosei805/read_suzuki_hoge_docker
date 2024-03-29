# コンテナの状態保存について

- コンテナの状態保存は重要な概念であり、永続的なデータや設定を保持する方法が必要です。
- コンテナ内での操作やデータの永続性を確保するためには、ファイルシステム、データベース、外部ストレージなどが使用されます。

# コンテナの独立性について

- コンテナは互いに独立しており、同じイメージから起動しても別々のコンテナとして扱われます。
- コンテナ間での操作や変更は互いに影響を与えません。

# コンテナの状態変更を他のコンテナに反映する方法

- イメージの更新: 新しいイメージを作成して変更を全てのコンテナに反映させる。
- ホストマシンとの共有: ホストマシンと共有することで、コンテナの状態変更を他のコンテナに反映させる。

# 構成変更の継続性とファイル共有

- 構成変更の継続性を保つためには、イメージを更新する方法があります。
- ファイルを残したい場合は、ホストマシンとのファイル共有が重要です。
- DockerfileやVolume、BindMountなどを使用して、コンテナ間での構成変更を管理します。
