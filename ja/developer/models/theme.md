# Theme

テーマのメタデータを保持しています。各種テーマファイルはサーバー上のファイルシステムに保存されます。

テーマとは、フロントエンドの外観 (Views) をカスタマイズできる機能です。[liquid](https://github.com/Shopify/liquid) の構文でカスタマイズした HTML 内に動的なコンテンツを埋め込むことが可能です。

`Theme` は次のカラムを持ちます。

- `name`: テーマ名です。
- `display`: テーマの表示名です。
- `version`: バージョン情報です。
- `description`: 説明文です。
- `homepage`: 作成者のホームページです。
- `author`: 作成者名です。
