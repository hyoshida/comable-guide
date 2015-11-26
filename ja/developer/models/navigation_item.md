# NavigationItem

ナビゲーション項目を保持しています。

`NavigationItem` は次のカラムを持ちます。

- `navigation_id`: `Navigation` に関連付く ID です。
- `linkable_id`: `linkable_type` が示すクラスに関連付く ID です。外部リンクなど、ID を持たない項目の場合は `NULL` になります。
- `linkable_type`: リンク対象となるモデル名の文字列を保持します。外部リンクなど、モデルを持たない項目の場合は `NULL` になります。
- `url`: URL です。外部リンクのときのみ使用します。
- `position`: 項目の順番です。[ActsAsList] が使用します。

[ActsAsList]: https://github.com/swanandp/acts_as_list
