# Order

注文情報を保持しています。注文が完了していないカート情報を含みます。

`Order` は次のカラムを持ちます。

- `user_id`: `User` に関連付く ID です。ログインユーザーの場合に利用されます。
- `guest_token`: ユーザーを識別するためのトークンです。ゲストユーザー（非ログインユーザー）の場合に利用されます。
- `code`: 注文番号です。
- `email`: 注文者のメールアドレスです。
- `payment_fee`: 決済手数料です。
- `shipment_fee`: 送料です。
- `total_price`: 商品合計と各種手数料を含んだ合計価格です。
- `bill_address_id`: `Address` に関連付く請求先住所の ID です。
- `ship_address_id`: `Address` に関連付く配送先住所の ID です。
- `state`: 注文ステータスです。詳細は [ステートマシン](../state_machine.md) をご覧ください。
- `completed_at`: 注文確定日時です。

## 価格

`Order` には各種価格を得るためのメソッドがいくつか用意されています。`current_` から始まるメソッドは対象の時価を示します。注文確定当時の価格を知りたい場合は `current_` の付かないメソッドから売価を取得できます。

`Order` に用意されている価格用のメソッドは次の通りです。

- `current_item_total_price`, `item_total_price`: 商品の合計価格です。
- `current_shipment_fee`, `shipment_fee`: 送料です。
- `current_payment_fee`, `payment_fee`: 決済手数料です。
- `current_total_price`, `total_price`: 商品合計と各種手数料を含んだ合計価格です。
