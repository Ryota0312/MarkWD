# WD記録スクリプト
+ 評価のための正解データ作成支援スクリプト．
+ 正解データは以下のような形式で `data/wdYYYYMMDD.csv` に記録．

```
/home/ryota/Documents/meeting/280,TeX文書作成
/home/ryota/Documents/record/058nom,Markdown記録書作成
```

# Install

```
$ git clone git@github.com:Ryota0312/MarkWD.git
$ cd MarkWD
$ export PATH=$PATH:$PWD
```

# Usage
## 本日更新があったディレクトリ一覧表示
+ 以下のコマンドを実行すると本日更新があったディレクトリをソートして一覧表示できる．
  + `ACCESS_LOG_PATH` は，CFALによって収集しているアクセス履歴

`$ todays-dir ACCESS_LOG_PATH`

+ 適宜エディタ等で開いてワーキングディレクトリのみを抽出し，`data/wdYYYYMMDD.csv` に記録．

## カレントディレクトリを記録
+ 記録したいディレクトリで以下のコマンドを実行
  + `WORK_NAME` は省略すると `None` になる
  + 既に記録されている場合，上書きされる

`$ pwd-mark WORK_NAME`

+ 記録を取り消したいディレクトリで以下のコマンドを実行

`$ pwd-mark -r`
