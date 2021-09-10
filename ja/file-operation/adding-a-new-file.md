# 新規ファイルの追加

1. リポジトリのトップページ「Code」タブの「Add file」（ファイル追加）ボタンをクリックすると、メニュー項目が表示されます（赤丸）。その中から「Create new file」（新規ファイル作成）を選択します。

![ ](images/file-operation/adding-a-new-file/fig-1.png)

2. エディタ画面に遷移します。

![ ](images/file-operation/adding-a-new-file/fig-2.png)

- ❶ファイル名……新規追加するファイル名を英数字でここに入力してください
- ❷Previewタブ……Markdown形式をHTML形式で描画したプレビューが確認できます。ただし、[GitHub Flavored Markdown - GFM記法](https://docs.github.com/ja/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)による描画です。Vivliostyle PubがもとづくVFM記法はこの拡張版なので、描画できないものもあることにご注意ください（→[VFM (Vivliostyle Flavored Markdown) の記法]()）
- ❸Edit new fileタブ……ファイルの内容を入力・編集できます
- ❹Commit名……新規ファイル名を入力すると、ここにそのファイル名が自動的に入力されます
- ❺Commitの説明……追加するファイルの内容、意図など説明をここに書きます（オプション）
- ❻Cancel Changes……変更を破棄して終了します
- ❼Commit new file……ファイルの編集が終わったらこのボタンを押して、終了してください

3. 「index2.md」が追加されました

![ ](images/file-operation/adding-a-new-file/fig-3.png)

4. 再度、リポジトリのトップページからAdd file」（ファイル追加）ボタンをクリックし、「Create new file」（新規ファイル作成）を選択します。

![ ](images/file-operation/adding-a-new-file/fig-4.png)

5. エディタ画面で設定ファイル`vivliostyle.config.js`を新規作成します。2つ以上のファイルをVivliostyle Pubで扱うためにはこのファイルが必須になります（単一ファイルの場合は不要）。

ファイル名を❶に記入し、作成が終わったら❷を押します。

![ ](images/file-operation/adding-a-new-file/fig-5.png)

内容の雛形は下記のとおりです。コピーしてお使いください。`----`の部分を書き換えていきます。

```
module.exports = {
  title: '---',
  author: '----',
  entry: [
    '----',
    '----',
  ]
}
```
`title: `（書名）と`author:`（作者）は必須ではありませんが、ファイル名は必須です。`entry: [`の次の行から、Vivliostyle Pubで表示させたいファイル名をシングルクォート`'　'`で囲み、行末をカンマ`,`で区切って記入していってください。

6. `vivliostyle.config.js`が追加されました。

![ ](images/file-operation/adding-a-new-file/fig-6.png)

7. Vivliostyle Pubを再読み込みさせて、追加したファイル（赤矢印）が表示されるか確認します。

![ ](images/file-operation/adding-a-new-file/fig-7.png)