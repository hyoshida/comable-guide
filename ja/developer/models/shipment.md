# Shipment

注文に紐づく配送情報を保持しています。

`Shipment` は次のカラムを持ちます。

- `order_id`: `Order` に関連付く ID です。
- `shipment_method_id`: `ShipmentMethod` に関連付く ID です。
- `fee`: 手数料です。
- `tracking_number`: トラッキング番号です。
- `state`: 配送ステータスです。詳細は [ステートマシン](../state_machine.md) をご覧ください。
- `completed_at`: 発送完了日時です。
