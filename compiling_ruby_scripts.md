# Compling Ruby Scripts

+ pycみたいなもの
* Experimental Tool at V.2.3

* JIT
  * 関数の頻度に応じて処理速度を変える
* Ahead-of-time
  * 実行前にコンパイル
  * 別言語のコードに変換
#### JavaVMがclassファイルをロードする部分を改良したい

* Fast Bootとメモリ削減が主
* 他のマシンに持って行っても動くとは限らない

rb->complie->binary data->load->isq

* ISeqは20&のメモリを使用しているので削減したい
* マルチプロセス時にプロセスごとにデータが用意されてしまうので，共有データをつけるようにし，メモリの使用量を削減したい．

* 構造が切れるごとにISeqは切れる.
rubyスクリプトは複数のISeqにより構成される．

## Lazy Loading

* 必要な時に必要なISeqをロードする

## Interface

* ```RubyVM::InstructionSequence.load_iseq```

  必要なもの(ロードできるデータがあれば)をロードしてIseqを生成する．

* ```RubyVM::InstructionSequence.to_binary```

  シリアライズ

* ```RubyVM::InstructionSequence.load_from_binary```

  デシリアライズ

* ライブラリをインストールする時にバイナリ化するのが一番可能性が高い
