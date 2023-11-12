# インターネットTV

## 概要

好きな時間に好きな場所で話題の動画を無料で楽しめる「インターネットTVサービス」を新規に作成することになりました。  
仕様は次の通りです。

- ドラマ1、ドラマ2、アニメ1、アニメ2、スポーツ、ペットなど、複数のチャンネルがある
- 各チャンネルの下では時間帯ごとに番組枠が1つ設定されており、番組が放映される
- 番組はシリーズになっているものと単発ものがある。シリーズになっているものはシーズンが1つものと、シーズン1、シーズン2のように複数シーズンのものがある。各シーズンの下では各エピソードが設定されている
- 再放送もあるため、ある番組が複数チャンネルの異なる番組枠で放映されることはある
- 番組の情報として、タイトル、番組詳細、ジャンルが画面上に表示される
- 各エピソードの情報として、シーズン数、エピソード数、タイトル、エピソード詳細、動画時間、公開日、視聴数が画面上に表示される。単発のエピソードの場合はシーズン数、エピソード数は表示されない
- ジャンルとしてアニメ、映画、ドラマ、ニュースなどがある。各番組は1つ以上のジャンルに属する
- KPIとして、チャンネルの番組枠のエピソードごとに視聴数を記録する。なお、一つのエピソードは複数の異なるチャンネル及び番組枠で放送されることがあるので、属するチャンネルの番組枠ごとに視聴数がどうだったかも追えるようにする

番組、シーズン、エピソードの関係について、以下のようなイメージです(シリーズになっているものの例)。

- 番組：鬼滅の刃
- シーズン：1
- エピソード：1話、2話、...、26話

## ファイル構成

- 提出QUEST (テーブル設計, テーブル構築, 抽出クエリ)：[internet_tv.md](internet_tv.md)  

- サンプルデータ挿入クエリ：[sample_data.sql](sample_data.sql)  
ターミナルで以下のコマンドを実行するとサンプルデータが挿入されます。  
ユーザー名の部分には、Root権限を持つユーザー名を入れてください。

```bash
mysql -u ユーザー名 -p internet_tv < sample_data.sql
```