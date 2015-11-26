# リリース

新しいバージョンの gem を [RubyGems.org] にリリースする手順は次の通りです:

1. 各ライブラリの `CHANGELOG.md` を更新します。
2. `CHANGELOG.md` に記述しておいた `(unreleased)` を `rake changelog:release_date` コマンドで実際の日時に置換します。
3. コミットします。
4. `COMABLE_VERSION` のバージョンを更新します。
5. `rake all:release` コマンドでリリースします。

[RubyGems.org]: https://rubygems.org/

## バージョニング

Comable は [セマンティック バージョニング] を採用しています。リリースの際にはこれに基づいてバージョニングすることになります。

[セマンティック バージョニング]: http://semver.org/lang/ja/
