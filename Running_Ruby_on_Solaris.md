# Running Ruby on Solaris

## BioRuby

* 生物化学用のライブラリ集

## Solarisでつまづくところ

* タイプミス
```
#if
#endif
```
* 名前の競合
* Endian
* Word alignment

## 名前の競合

solarisがatomic.hを持っていたため，include時の名前が競合した

## エンディアン

* 32 - 64ビットの際にオフセットすると問題になるかと
 
