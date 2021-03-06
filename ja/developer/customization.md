# カスタマイズ

Comable を利用したアプリケーションを構築すると、Comable の内部処理をカスタマイズする必要に迫られることが少なからずあります。ここではカスタマイズ対象ごとに、その方法を紹介します。

## モデル

Comable のモデルのカスタマイズには Rails の公式ドキュメントで紹介されている [Overriding Models and Controllers] の手法が利用できます。Comable にはこの手法を利用するための処理が組み込まれています。そのためアプリケーション側は事前準備なしに `app/decorators` 以下にファイルを設置するだけでオーバーライドが可能になります。

例えば `User` に「ユーザー名を取得する」というメソッドを追加するには、以下の内容のファイルを `user_decorator.rb` という名前で設置することになります:

```ruby
Comable::User.class_eval do
  def full_name
    bill_full_name || email
  end
end
```

[Overriding Models and Controllers]: http://edgeguides.rubyonrails.org/engines.html#overriding-models-and-controllers


## コントローラ

コントローラもモデルと同じ手法でカスタマイズが可能です。

## ビュー

ビューのカスタマイズはモデルやコントローラと違って、少し特殊なやり方が必要です。

カスタマイズの方法は主に２つあります。１つは Comable のビューファイルをコピーしてきて上書きする方法、もう１つファイルを上書きせずにオーバーライドする方法です。前者はもっとも手取り早い方法です。ただしアプリケーションを長期的に保守する場合は、Comable がアップデートするたびに互換性を保つための努力が必要になるため、あまりおすすめできません。

後者の方法、つまりビューのオーバーライドは [Cosme] を使って実現することができます。このライブラリは、HTML セレクタを使ってオーバーライド対象の選択を行うので、ビューファイルを上書きする方法よりも互換性を保ちやすいのが利点です。またカスタマイズ部分のみを記述することになるので、どこからどこまでがカスタマイズかということに迷うことがなくなります。詳しい使用方法はライブラリのドキュメントをご覧ください。

[Cosme]: https://github.com/appirits/cosme
