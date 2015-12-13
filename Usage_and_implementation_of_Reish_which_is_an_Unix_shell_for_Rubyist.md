# Usage and implementation of Reish which is an Unix shell for Rubyist

Speaker: Keiju Ishitsuka
* irbの作者

## Reish

* 昔のRuby: Shellぽかった-> Shellそのものでもいいんじゃない?
* イテレータを使える
* 引数は全てObject扱い
* 上の部分はShellぽいが，細かいところに行くとrubyに近い

* ExEnv
  * 実行環境を担う

## コード生成

* SimpleCommand
  * そのままRubyに変換
    * ``` / ```がある場合は，sendを使う
* Pipeline
  * メッセージセンドに変換する
  　``` ls ; pw -> ls().pw()```

## methodmissing

* コマンドが存在しない場合は，環境変数のPATHをたどってSystemCommandを返す
* SystemCommandがつながったが場合，Reishを通さず，しすてむコマンド側で完結させる

## コマンドの出力

* 端末
  * .reish_termをつける(内部的に)
* stdout
* 次のコマンドへ
* 実行結果ではなくステータスが欲しい場合もある
  * ```.reish_status```をつけている(内部的に)

## reish_eval

* ローカル変数を参照したいため
