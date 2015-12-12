# Data Analytics Service Company and its Ruby Usage

Speaker: Tagamori Satoshi

* Data service関連のツール
  * C++/JVMが多い(頻繁に変えないため)
  * 保存先はHadoopが主
  * Collect->store->process->visualize(->reporting, monitoring)

## Data Analytics Platform

* Data collection
* API endpoint
* Schema management.
* Processing(batch, query)(Hadoop)
* Queuing，スケジューリング
* Data connector/export

## Treasure Data internal

* Java/(J)Ruby が多い
* OSSツールが主
  * クローズドで管理するのが大変，色々な人がパッチを送ってくれたりする．
* Worker request 200k/day 50k/day 12M/day(138/sec)

## PerfectSched(schedulare)

* cronみたいなもの
* CRuby
* At least once semantics(リクエストに応じて1回だけ実行する)
* キューを作成する機能

## PerfectQueue

+ Queueにはプライオリティーをもたせている
* Queueは一つのテーブルに対応
  * 将来的には別のDBになるかもしれない

### testing

* RSpecで実施
* わかりやすくするためにMetaprogramingを利用している
  * Indented here documentsは便利そう

## Done is better than Perfect

* 互換性を確認しながら，できるだけ改善していく
* どこに問題あるかを常に意識しながら改善していく
