# インストール

アプリケーションに Comable をインストールする手順は以下の通りです。

1. `Gemfile` に Comable を追加します:

    ```ruby
    gem 'comable'
    ```

2. [Bundler] を利用して gem をインストールします:

    ```bash
    bundle install
    ```

3. Comable のジェネレータで必要なファイルをインストールします:

    ```bash
    bundle exec rails generate comable:install
    ```

4. アプリケーションサーバーを起動します:

    ```bash
    bundle exec rails server
    ```

最後に任意のブラウザで `http://localhost:3000` にアクセスしてください。

[Bundler]: http://bundler.io/

## 管理画面

アプリケーションのバックエンドにアクセスするには管理者権限を持つユーザーが必要になります。

以下のコマンドで管理ユーザーを生成できます。

```bash
bunlde exec rake db:seed
```

この後に `http://localhost:3000/admin` にアクセスし、指定したユーザー情報を入力することでバックエンドにアクセスできます。

## 開発準備

アプリケーションではなく Comable そのものを開発する場合は以下の手順でインストールできます。

1. Comable のソースをダウンロードします:

    ```bash
    git clone https://github.com/appirits/comable.git
    ```

2. ダウンロードしたディレクトリに移動します:

    ```bash
    cd comable
    ```

3. 依存するライブラリをインストールします:

    ```bash
    bundle install
    ```

4. データベースを初期化します:

    ```bash
    bundle exec rake db:create
    bundle exec rake db:migrate
    ```

通常のアプリケーションと同じようにサーバーを起動する方法については [ダミーアプリケーション](dummy_application.md) をご覧ください。
