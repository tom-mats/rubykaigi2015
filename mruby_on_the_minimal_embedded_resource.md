# mruby on the minimal embedded resource

* Prototyping platformの作成(enzi)
  * mruby + センサー
* 組み込みLinuxの対応
  * Linux on MIPS
  * 通信/制御
* mrdbの作者
* mruby-polarsslをapache licenceに変更

* mrubyでは使うメモリの先を変更できる
  * CPUも改良されている

## Physical computing

* Cのコードはコンパイルの中継が必要なので，開発に時間がかかる
* アルディーノなどは豊富のライブラリが整っている

## mrubyの良い点

* サイズが小さい
* オブジェクト指向
* Fiber(軽量なスレッドシステム)
* ライブラリが整って

## 他の環境

* Python
* Javascript

  最近流行っている

* Lua

  ライブラリが少ない

# mrubyが動くスペック

* デフォルトのgemだけで150KB
* libを使うのにが50-100KBは必要

# FROM

* stringを使うことでメモリの書き換え回数が大幅に増加する
