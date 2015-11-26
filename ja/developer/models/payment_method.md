# PaymentMethod

決済方法を保持しています。

`PaymentMethod` は次のカラムを持ちます。

- `name`: 決済方法名です。
- `fee`: 手数料です。
- `payment_provider_type`: 決済プロバイダのクラス名を文字列で保持します。
- `payment_provider_kind`: 決済プロバイダ内の種別をインデックスで保持します。
- `enable_price_from`: 利用可能な価格範囲の開始値です。
- `enable_price_to`: 利用可能な価格範囲の終了値です。
