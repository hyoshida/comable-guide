# ライブラリ構成

Comable は複数のライブラリ (gem) で構成されています。これによって必要な機能を取捨選択して利用することができるようになっています。これらの gem は、すべて Comable のリポジトリ内に含まれています。

以下に各種 gem を紹介します。

<!---
#+ORGTBL: SEND gems orgtbl-to-gfm
| gem              | ディレクトリ | 説明                                               |
|------------------+--------------+----------------------------------------------------|
| comable          | -            | これ以下のすべての gem を読み込むための gem です。 |
| comable-core     | core         | コア機能となるモデルやヘルパーを扱います。         |
| comable-frontend | frontend     | フロント画面のビューやコントローラを扱います。     |
| comable-backend  | backend      | 管理画面のビューやコントローラを扱います。         |
| comable-sample   | sample       | サンプルデータの作成機能を提供します。             |
-->

<!--- BEGIN RECEIVE ORGTBL gems -->
| gem | ディレクトリ | 説明 |
|---|---|---|
| comable | - | これ以下のすべての gem を読み込むための gem です。 |
| comable-core | core | コア機能となるモデルやヘルパーを扱います。 |
| comable-frontend | frontend | フロント画面のビューやコントローラを扱います。 |
| comable-backend | backend | 管理画面のビューやコントローラを扱います。 |
| comable-sample | sample | サンプルデータの作成機能を提供します。 |
<!--- END RECEIVE ORGTBL gems -->
