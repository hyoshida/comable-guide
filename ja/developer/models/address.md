# Address

住所情報を保持しています。

`Address` は次のカラムを持ちます。

- `user_id`: `User` に関連付く ID です。ユーザーが複数住所を保持するのに利用されます。利用中の請求先住所や配送先住所は `User` の `bill_address_id` と `ship_address_id` にそれぞれの ID が保持されます。
- `family_name`: この住所に属する人物の苗字です。
- `first_name`: この住所に属する人物の名前です。
- `zip_code`: この住所の郵便番号です。ハイフンの有無は問いません。
- `state_name`: この住所の都道府県名です。
- `city`: この住所の市町村名です。
- `phone_number`: 電話番号です。ハイフンの有無は問いません。
