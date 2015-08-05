# Category

商品カテゴリを保持しています。ツリー構造の実現には [Ancestry](https://github.com/stefankroes/ancestry) を利用しています。また、リスト構造の実現には [ActsAsList](https://github.com/swanandp/acts_as_list) を利用しています。

`Category` は次のカラムを持ちます。

- `name`: カテゴリ名です。
- `ancestry`: Ancestry が使用します。
- `position`: ActsAsList が使用します。
