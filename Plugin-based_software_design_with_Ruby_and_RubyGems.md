# plugin-based software design with ruby and rubygems

## Plugin architecture

* keep core SimpleCommand
* many features
* easy to test
* active developer community

## plugin design pattern

## plugin-based architecture

* Application = Plugins network
* More flex != More complex

### DI

* Interface = Plugin
* Unittestするときに便利

### Dynamic Plugin Loader

###  Combination of those

## example at fluentd

### fluentd

* Data collector
* JSONベース
* C&Rubyで実装

* Plugin marketplaceにはrubygems.orgを利用
  * なかったらrubygems.orgから取ってくる
* fluentd coreはplugin間のメッセージ管理のみを行う
* 実際の処理はpluginで行う

## example at embulk

* CSVはデータベースといったバルクデータをhadoopなどに出力
* Java&JRubyで実装

### Usecase mysql->(kuromoji->)elasticsearch

### S3->Analystic(BigQuery, Redshift)

## architecture

* Coreにはexecutor pluginが刺さっている
* Input自体はFileInputとDecorder,Parserで基本的には構成される
  * Outputも同様
