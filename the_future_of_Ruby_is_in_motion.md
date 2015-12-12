# The future of Ruby is in motion

Speaker: Laurent Sansonetti

* 元Apple

## Rubymotion

* iOS/Androidで動くフレームワーク
  * iOS は Objective-Cに刺さっている
  * Androidの場合は，JNIを経由してJVMに刺さっている

## Static compilation

* rb -> AST -> LLVM IR -> asm で変換している
* バイナリ(Native Code0)として使うので速度は早そうだ
* サイズはMB程度になる

* rubymotion
