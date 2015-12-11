# Experiments in sharing Java VM technology with CRuby

## なぜRubyのJITを作っているか

* IBMはクラウド関係に力を入れている
* Rubyが早くなれば，CloudでのRubyの処理環境を改善できる

## OMR

* IBMがオープンソースで提供している仮想マシン環境
+ Testarossa
  * コードをそれぞれ(x86/powerpc)などに合わせて実行する
  * c++
  * 100以上の最適化ツールが含まれている

* YARV
 * 現状のRubyのVM
 * 実行コードはかなり複雑
 
