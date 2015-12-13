# Upcoming Improvements to JRuby 9000

## JRuby

* GC
* Native JIT
* Cross Platform
* Javaライブラリを使える

## JRuby 9000

* Ruby2.2向け
* Semantic analysis や最適化処理を追加
* 9.0.4ではMRIより早くなった

csv.rbはJrubyではとても遅いらしい
* Backtrace関連の問題
* rescueの処理がよくない

## JRubyの問題点

### 起動速度

* CRubyよりStartupが遅い
* ```jruby --dev```とすると速いけど，最適化とか抜けているので注意

## AOT

* PrecompilerとしてJITの前に走らせると起動が早くなる
* ```jruby --dev```と同等程度
* 最適化の有無にはあまり依存しない


## 9.1.0.0

* Ruby2.3サポート
