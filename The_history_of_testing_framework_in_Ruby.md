# The history of testing framework in Ruby

Speaker: Kouhei Sutou

## Ruby1.3

* testsupp
  * Perlのテストモジュール

## Ruby1.4

* RubyUnit
  * xUnit系
    * XP(1999年出版)を元に生まれた
  * Testを生成するコマンドが付いている

## Ruby1.6

   * Lapidary
    * GUIのテストランナーあり

## Test::Unit
  * RubyUnit+Lapidary
    * APIはRubyUnitがベース
    * ベースはLapidary

## Ruby1.8
  * テストユニットがバンドルされた
  * ```require "test/unit"```

### Rspec

  * 英語っぽい
  * Mockや未実装などもある
  * Test::Unitはあまり進歩しなかった

## Ruby1.9

  * Test::Unit -> test-unitに成った．(バンドルされなくなった)
    * 開発は継続中
  * minitest
    * 同じ頃開発
    * Ruby1.9にバンドル
  * test/unit
    * Test::Unit<->minitestのラッパー
    * 実際にテストするのはminitest

## Ruby2,1

  * minitestに非互換の修正が入った
    * 新しいのはバンドルするが，
      Ruby-coreのテストには古いminitestとtest/unitを使うようにした．

## Ruby2.2

  * test-unitがバンドルされるようになった
  * test/unitは

    Core開発者にとっては test/lib/test/Unit

    普通の人には lib/test/unit

## testunitとは

* Test::Unitと互換性があるもの
* Rubyっぽい
　* 普通のrubyスクリプトのように欠ける

### グループ化

* テストケースはclassにする
* サブテストケースは子class化する
  * selfの継承が必要
* テストを共有する場合はmodule化する

### Assertion

* RSpec, test-unitは色とスニペットできる
　* test-unitは前景色も設定
* power-assert
```
assert do
条件
end
```
  * 縦で並べられないので，やりにくい時があるかも

## Fixture

  * テストの実行結果を同じにするための仕組み
