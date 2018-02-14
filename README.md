# 共立出版『Rで楽しむ統計』サポートページ

とりあえず，code，data，figにコード例，データ，図のRソースとMakefileを置いておきます。

[本文中の全コード](code.md)を公開しました。

## リンク

* 共立出版の[『Rで楽しむ統計』のページ](http://www.kyoritsu-pub.co.jp/bookdetail/9784320112414)
* 共立出版の[「Wonderful R」シリーズのページ](http://www.kyoritsu-pub.co.jp/series/205/)

## Errata

* p.28 最初の4行がまったく違いますorz。正しくは
```
> qnorm(0.975)
[1] 1.959964
> qnorm(0.995)
[1] 2.575829
```
です。また，その少し下に `y$生徒数` が突然出てきますが，その前に何かが抜けていますねorz。

* p.54 「密度関数 dpois(x,λ)」は，いろいろ考えましたが，とりあえず「確率 dpois(x,λ)」でどうでしょうか。Rのヘルプでは「density」functionと呼んでおり，そもそもdpoisのdはdensityから来ているのですが，離散分布ですので，密度関数と呼ぶのは少々ためらいがあります。離散分布の確率には「質量関数」（mass function）という用語があるので，そちらを（どこかで定義して）使うべきだったかもしれません。

* p.152 間違いではないですが，下から10行・9行のコードがやや不自然でした。次のようにするほうが素直かもしれません。
```
m = outer(40:90, 40:90, Vectorize(function(x,y) f(c(x,y))))
```
* p.155 下から4行目：都道府県iの「点数」→都道府県iの科目jの「点数」
