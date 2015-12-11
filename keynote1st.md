# Keynote初日(Ruby3.0 Challange)

* Speaker Yukihiro "Matz" Matsumo

money forward CEO(スポンサー)
* Rubyの開発を行う人を採用(会社の業務には携わらない)

MINASWAN
* マーチンファウラー提案
* Rubyコミュニティの良い点

## Ruby2.3

* 12/25 にリリース
* rubykaigiに合わせてコミット

* レコメンド機能を追加
  * 関数名を間違えたら提案してくれる

Ruby3.0にはstringがすべてfreeze(変更不可)になる予定?

### Safe navigation operator

* objectがnilかどうかをチェックし，nilじゃなかったら.以降の関数を呼ぶ
* ```&.``` lonely operator

### 高速化

* 年5-10%で速度が向上

## mruby 1.2

* バグの修正
* ビルドプロセスを改良
* あまり変更はない

## Streem

# OCaaS

* OSS community as Shark
* OSSには変化が必要

* 人が「欲しい」機能ではなく「必要」な機能を作るべきだ
* 「欲しい」機能を作ると大抵失敗する
* 未来にこんな機能が欲しいというつもりで作った(ruby開発開始時)
* 新しい当たり前を作る
* 変化させることをやめるとシステムは死んでいく
* 1.8-1.9に移行するのに5年かかった(開発には3年ぐらい)
  * テストとコード変更を繰り返した

## 移行に伴う撒き餌

* 1.8 -> 1.9への移行により
  * Performanceの向上

## 変化において重要なこと

* 理由なく互換性を切ってはいけない
* メリットを提供しないといけない

# 今後(Ruby3)

* MultiCoresの対応向上
* Code scalability
* Data scalability

## MultiCores

* Concurrencyが重要
  * Actor Model
  * Ownership model(スレットが権限を持っていると読み書きできる)
  * STM(Rubyにはきつい)

## Code scalability

* Man-machine インターフェース
  * コンパイラをより賢く
  * Dialyzer(緩い型チェック)
* Performance
  * Ruby3 はRuby2に比べて3倍速くしたい
    * 2010年代にはリリースしたい
  * JIT
  * Ahead-of-time compiler
  * Memoryの使用量はRuby2.3レベルにまで抑えられる処理を入れる予定
  
