# Ruby meets Go

Speaker: Masaki Matsushita

* C shared from Go 1.5
* rubyからGoの関数を呼び出す(FFI/Fiddle)
* RubyのライブラリをGoでかく

## C Shared

* Cからよびだせるライブラリを生成する処理
* ```cgo```

## GoからC

```
import "C"
```

で読み込めるようになる．
.soも生成できる

## rubyでsoを使う方法

* FFI
* Fiddle
+ 数字は簡単だが，文字列だと若干めんどくさいかも
  * GoStringを使う必要がある
  * ```C.String``` Go -> c
    * ユーザが責任持ってメモリ管理してあげる必要がある
　* ```C.GoString``` c -> Go

## Goでライブラリを作る方法

* CgoではMacroは使えない
* gemにGoファイルに必要がある

### cgoではMacroを使えない

対策

* Cの関数で実装する
  * 同等の関数がない場合は，Goのファイル内に用意してあげる

### 文字列のコピー処理

* Go String->(copy)C.String->(copy) Ruby string
  * Cの文字列についてはユーザーがメモリ管理しないといけない
```
defer C.free(unsafe.Pointer(cs)) <- メモリを解放してあげる
```
* GOSTRING_PTRを用意してあげれば，コピー処理を走らなくすることもできる

### gem

* extension patternにgoを追加する
* 決定版と言えるような(Helper)関数群は存在しない．
