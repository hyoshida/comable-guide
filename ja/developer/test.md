# テスト

Comable の自動テストにはさまざまな項目が含まれています。自動テストで測定される項目は次の通りです:

* [Rspec]: コードの動作に対するテストです。これにはユニットテストや結合 (Feature) テストが含まれます。
* [Jasmine]: JavaScript に対するテストです。
* [RuboCop]: コーディングスタイルを検証します。
* [Brakeman]: 脆弱線診断を行います。

すべての自動テストを実行するには以下のコマンドを実行します。

```bash
rake
```

ただしいずれかのテスト項目で失敗があると、それ以降のテスト項目が実施されないので注意が必要です。

[Rspec]: https://github.com/rspec/rspec-rails
[Jasmine]: https://github.com/searls/jasmine-rails
[RuboCop]: https://github.com/bbatsov/rubocop
[Brakeman]: https://github.com/presidentbeef/brakeman

## 継続的インテグレーション

自動テストは git-push をトリガーにして [Travis CI] でも実行されます。

[Travis CI] ではローカルでのテストの他に、複数の Ruby のバージョンや複数のデータベースサーバーを組み合わせてのテストが実施されます。これには ruby-head や rails-edge といった次期バージョンでのテストも含まれるため、次期バージョンに向けた開発の補助としても有用です。

テストの対象や実行スクリプトなどは `.travis.yml` から変更することができます。詳しくは公式ドキュメントをご覧ください: [Building a Ruby Project]

[Travis CI]: https://travis-ci.org/appirits/comable
[Building a Ruby Project]: https://docs.travis-ci.com/user/languages/ruby

## カバレッジ

テストカバレッジは [Coveralls] で測定しています。この測定は git-push をトリガーにして行われます。

また、GitHub で Pull-Request を作成すると自動で計測値が通知されます。このときのカバレッジがマージ対象のブランチより低いものだと警告が表示されます。カバレッジが 100% に近づくのは悪いことではありませんが、一般的にカバレッジが高くなるのに比例して作業コストも高くなるので、このトレードオフを十分理解した上で利用するのが理想的です。場合によっては警告を無視してマージせざるを得ないでしょう。

[Coveralls]: https://coveralls.io/github/appirits/comable

## メトリクス

メトリクスは [CodeClimate] で測定しています。この測定は git-push をトリガーにして行われます。

メトリクスの測定値はそのままコードの品質を示しているということができます。リファクタリングの目安として利用することをおすすめします。

[CodeClimate]: https://codeclimate.com/github/appirits/comable
