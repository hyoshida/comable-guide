# User

ユーザー情報を保持しています。管理者と顧客はどちらともこのモデルで管理されます。

`User` は次のカラムを持ちます。

- `email`: メールアドレスです。
- `role`: ユーザーの権限です。
- `bill_address_id`: `Address` に関連付く請求先住所の ID です。
- `ship_address_id`: `Address` に関連付く請求先住所の ID です。
- `TODO`: ...
