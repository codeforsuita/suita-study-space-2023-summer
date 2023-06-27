# 吹田市内の自習マップ 2023 年夏版

## 目的
* 夏休みの学習スペースを探す助けとなる

## 方針
1シーズンなど、期間限定。年を超えた長期メンテナンスはしない。

## 今後


## 動かし方

### 用意するもの

- github リポジトリ を作る
  - ※ チーム運用するなら github organization の方が良いかも？
- github Pages を設定する
  - [GitHub Pages サイトを作成する - GitHub Docs](https://docs.github.com/ja/pages/getting-started-with-github-pages/creating-a-github-pages-site)
- 以下のような google スプレッドシート を作る
  - https://docs.google.com/spreadsheets/d/1BrxbNH36Bx4wk_-IPL32ji_CxYwcVRggLO9iTKEztSY/edit?usp=sharing
- スプレッドシートに App Script を追加する
  - 追加するスクリプト `gscript/doGet.gs`
  - 追加の仕方
    - スプレッドシートのメニュー 「拡張機能」→ 　「App Script」
    - 「スクリプト」にコードをペーストして、「デプロイ」ボタンを押す → 種類は「ウェブアプリ」
    - WebAPI の url が発行される。その url を `config-user.jsonc` の `google.AppScript`(※ 55 行目) に設定する。

## (TODO 未確認)　カスタマイズ方法

- 表示する施設の変更方法
  - `config-user.jsonc` の `listTable.targets` 他。
  - `overpass-custom.json` に、 OpenStreetMap の API へのリクエストパラメータを設定する
- 最初に出てくる画像
  - `splash.url`
- TODO: タイトル、説明、メタタグ、etc..
