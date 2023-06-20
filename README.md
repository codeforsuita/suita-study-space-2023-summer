# 遊具のある公園マップ

## 目的
* 子どもたちの希望に沿った公園を探すことができる
* 公園以外にも、遊具がある場所を探すことができる
* 街で見つけた素敵な場所を地図で共有できる

## 今後
* 公園の健康器具も取り扱いたい（大人も楽しむ）
* 水飲み場や自動販売機も表示するべき？（悩む）

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
  - `overpass-custom.json` に、 OpenStreetMapのAPIへのリクエストパラメータを設定する
- 最初に出てくる画像
  - `splash.url`
- TODO: タイトル、説明、メタタグ、etc..
