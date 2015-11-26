# StockLocation

倉庫情報を保持しています。商品には複数の倉庫の在庫を紐づけることができます。注文時に対象在庫を保持する倉庫が複数存在した場合は、その中から適当な１つが選択され、在庫の割り当てが行われます。もしも倉庫の在庫が尽きてしまったときは、他に同じ在庫を持つ倉庫があればそこからの割り当てを試みます。

`StockLocation` は次のカラムを持ちます。

- `name`: 倉庫名です。
- `default`: デフォルト倉庫かどうかを示すフラグです。すべての在庫は初期化時にデフォルト倉庫に関連付きます。
- `active`: 有効/無効を示すフラグです。このフラグが有効な倉庫の在庫が注文時に利用されます。
- `address_id`: `Address` に関連づく ID です。