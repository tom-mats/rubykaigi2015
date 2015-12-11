# High Performance Template Engine:Guide to optimize your Ruby code

* erb
* haml(htmlに特化)
* slim(hamlに近い，軽量)

## Templateの中身

* templateをrubyコードに変換
* rubyコードからhtmlを生成

## Performance

* Hamlはパフォーマンスに劣る
　* Templateからrubyに変換する際に関数呼び出しなどがあるため遅くなる．
* Slimは早い(erbレベル)
  * Template gemを使うことで，一般的な最適化を行ってくる

## Rubyを早くする方法

### ベンチマーク

* ベンチマークを書いておけば，後から遅くなったかどうかをチェックできる
* benchmark-ips

### どこを図るか

* templateエンジンからrubyを作るプロセスと
  rubyからhtmlを生成する部分の処理速度は相反する
* 今回は後者

rblineprofは短いスクリプトに向いている

###　ベンチマークは常に行う

* ベンチマークの結果があることで，ちゃんと早くなったかどうかをチェックできる

## Faml

* Slimの機能をHamlに移植したい
* Hamlの書き方には自由度が高い
  * Parser gemを使ってparseするようにした．
+ Runtime attribute
  + keyとvalが変数
  + 一番時間がかかる
* Templateエンジンにおいて，行番号を一致させるのは重要

### Runtime attributeを早くしたい

* C/C++で書けばだいぶ早くなる
* 遅いところだけC/C++のは有効．全部を書くのは無謀

## Hamlit

* String allocation
  * Templeを使うことで勝手にfreezeがつく
* stcat
  + string interpolationが早い
* Ripperを使って構文解析. stringだったらそのまま書いてしまう．
