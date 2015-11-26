# User

ユーザー情報を保持しています。管理者と顧客はどちらともこのモデルで管理されます。

`User` は次のカラムを持ちます。

- `email`: メールアドレスです。
- `role`: ユーザーの権限です。次のうちのいずれかの値を取ります: `customer`, `reporter`, `admin`
- `bill_address_id`: `Address` に関連付く請求先住所の ID です。
- `ship_address_id`: `Address` に関連付く請求先住所の ID です。
- `encrypted_password`: 暗号化したパスワードを保持します。[devise] が使用します。
- `reset_password_token`: パスワードリセット時のトークンを保持します。[devise] が使用します。
- `reset_password_sent_at`: パスワードリセット送信日時を保持します。[devise] が使用します。
- `remember_created_at`: ログイン状態の記憶開始日時を保持します。[devise] が使用します。
- `sign_in_count`: サインイン回数を保持します。[devise] が使用します。
- `current_sign_in_at`: サインイン日時を保持します。[devise] が使用します。
- `current_sign_in_ip`: IP アドレスを保持します。[devise] が使用します。
- `last_sign_in_at`: 最終サインイン日時を保持します。[devise] が使用します。
- `last_sign_in_ip`: 最終サインイン時の IP アドレスを保持します。[devise] が使用します。

[devise]: https://github.com/plataformatec/devise

## カートの継承

ログインしていないユーザーがカートに商品を追加すると、`guest_token` を発行してカート情報を `Order` に保存します。このあとでユーザーがログインすると、ログイン前のカート情報をログイン後のカートに継承する処理が実行されます。この処理は [warden] の `after_set_user` メソッドを利用することで実現しています。

ログインユーザーとしてのカートがすでに存在する場合は、ゲストユーザーとしてのカートとのマージが行われます。例えばログインユーザーとしてのカートには商品 A が１つ存在していたとします。ユーザーがログアウトした状態でカートに商品 A を２つ追加し、このあとにログインすると、ユーザーのカートには３つの商品 A が存在することになります。

[warden]: https://github.com/hassox/warden
