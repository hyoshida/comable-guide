# Payment

注文に紐づく決済情報を保持しています。

`Payment` は次のカラムを持ちます。

- `order_id`: `Order` に関連付く ID です。
- `payment_method_id`: `PaymentMethod` に関連付く ID です。
- `fee`: 手数料です。
- `state`: 決済ステータスです。詳細は [ステートマシン](../state_machine.md) をご覧ください。
- `completed_at`: 決済確定日時です。
