# Building CLI Application For Everyone

* rubyをパッケージでとして提供したいという話

## Packaging in Ruby

* heroku toolbelt
* hk (heroku cli at golang)はrubyに比べて圧倒的に速い

### Shoes.rb

* Traveling Ruby

## Why mruby

* いろいろないけど一応Ruby
* mrbgems
  * 特別なrakeファイルが存在する
　* Nativeに出力するのでCrosscompile環境が必要
* いろいろめんどくさい

## mruby-cli

* パフォーマンスがいい
* メジャーなプラットフォームでは対応済み
* Dockerを用いてpackageに近い形で提供している
