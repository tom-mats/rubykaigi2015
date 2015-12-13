# Request and Response

* Manage IQ
  * 仮想OSを管理するソフト
* Ruby/Rails/Rack core team

## HTTP2

### 利点

* Binaryプロトコル
  * データ量が減る
* 多重化
　* 複数の情報をまとめてから送信
* サーバープッシュ
* headerはいつも小文字
  * 特別な headerは:で始まる

## Rack

* Adapter Pattern
  * 依存関係の爆発を防ぐ

###
1. Web server がrequestを解析し，env
2. Rail::Application
3. Rack::SendFile
4. ActionDispaher::Static
5. AD::LoaderI
6. xx
7. Rackアプリケーションが要した時間を書きコム
8. xxx
9. RequestID
10. Loggingの処理
11. ShowException
...
99. Router

### 問題点

* 長い
* 複雑
* ハッシュキーを代えられない
* 配列の順番も代えられない

### node.jsを参照してみる

## Rails


## Rack/Rails + HTTP2
