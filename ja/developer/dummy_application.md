# ダミーアプリケーション

Comable には開発用にダミーアプリケーションが存在します。開発に際していちいちアプリケーションを作成する必要はありません。このダミーアプリケーションは `spec/dummy` ディレクトリ以下に存在します。ファイル構成は通常の Rails アプリケーションとほとんど同じです。このディレクトリから `rails` や `rake` などのコマンドを利用することが可能です。

ダミーアプリケーションが使用するデフォルトのデータベースサーバーは PostgreSQL です。環境に合わせて `dummy_development` や `dummy_test` といったデータベースにアクセスします。これらの設定は `spec/dummy/config/database.yml` から変更することができます。

## シードデータ

ダミーアプリケーションのバックエンドを利用するには管理者権限を持つユーザーが必要になります。

`comable-core` には管理ユーザーを作成するための機能が用意されています。これを利用するには `spec/dummy` ディレクトリで以下のコマンドを実行します。

```bash
bin/rails runner Comable::Core::Engine.load_seed
```

## サンプルデータ

ダミーアプリケーションを利用するときにある程度のデータが入っていないと不便です。そこでサンプルデータをあらかじめ用意しておくことをおすすめします。

`comable-sample` にはサンプルデータを生成するための Rake タスクが含まれています。これを実行するには `spec/dummy` ディレクトリで以下のコマンドを実行します。

```bash
bin/rake comable:sample
```