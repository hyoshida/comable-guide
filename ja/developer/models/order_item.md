# OrderItem

注文明細を保持しています。

`OrderItem` は次のカラムを持ちます。

- `order_id`: `Order` に関連付く ID です。
- `variant_id`: `Variant` に関連付く ID です。注文対象の商品を示します。
- `name`: 注文当時の商品名です。
- `sku`: 注文当時のSKUです。
- `price`: 注文当時の商品価格です。
- `quantity`: 商品の個数です。
