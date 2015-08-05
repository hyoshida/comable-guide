# Image

商品画像を保持しています。画像ファイルは [CarrierWave](https://github.com/carrierwaveuploader/carrierwave) によって、サーバー上のファイルシステムに保存されます。

`Image` は次のカラムを持ちます。

- `product_id`: `Product` に関連付く ID です。
- `file`: CarrierWave が使用します。
