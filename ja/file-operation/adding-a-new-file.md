# 新規ファイルの追加

1. Vivliostyle Pubで表示させるファイルを、GitHubリポジトリに作成します。リポジトリのトップページで「Code」タブを表示させたとき、もしリポジトリ内にファイルがない場合、下記のような画面が表示されます。赤丸で囲んだ “creating a new file”（新規ファイル作成）をクリックしてください。文字が小さいので、違う場所をクリックしないよう気をつけてください

![ ](images/file-operation/adding-a-new-file/fig-1.png)

2. エディタ画面に遷移します。なにか文字を書いてください。この段階では内容は仮のもので大丈夫です。終わったら “Commit Changes” ボタン（❺）を押下して、内容を確定してください

![ ](images/file-operation/adding-a-new-file/fig-2.png)


- ❶ファイル名……新規追加するファイル名を英数字でここに入力してください。**拡張子は必ず`.md`を指定してください。**
- ❷Edit new fileタブ……ファイルの内容を入力・編集できます
- ❸Commit名……新規ファイル名を入力すると、ここにもそのファイル名が自動的に入力されます（オプション）
- ❹Commitの説明……追加するファイルの内容、意図など説明をここに書きます（オプション）
- ❺Commit new file……ファイルの編集が終わったらこのボタンを押して、終了してください
- ❻Cancel Changes……変更を破棄して終了します


3. ちなみに、エディタ画面の「Preview」タブをクリックすると、Markdown形式をHTML形式で描画したプレビューが確認できます。ただし、[GitHub Flavored Markdown - GFM記法](https://docs.github.com/ja/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)による描画なので、Vivliostyle Pubのプレビューと異なる部分もあります。参考に留めてください（→[VFM (Vivliostyle Flavored Markdown) の記法]()）

![ ](images/file-operation/adding-a-new-file/fig-3.png)


4. リポジトリのトップページ「Code」タブに戻ると、さっき追加した`chapter-1.md`が追加されていることが確認できます（赤矢印）。この画面から新規にファイルを追加することもできます。引き続き、`chapter-2.md`を追加してみましょう。「Add file」（ファイル追加）ボタンをクリックするとメニュー項目が表示されます（赤丸）。その中から「Create new file」（新規ファイル作成）を選択します

![ ](images/file-operation/adding-a-new-file/fig-4.png)


5. 前記「2」と同じエディタ画面に遷移します。❶のカラムにファイル名`chapter-2.md`を記入、仮のファイル内容を書き、終わったら “Commit Changes” ボタン（❷）を押下して確定してください

![ ](images/file-operation/adding-a-new-file/fig-5.png)

6. `chapter-2.md`が追加されました（赤矢印）。最後に設定ファイル`vivliostyle.config.js`を新規作成します。再度、リポジトリのトップページからAdd file」（ファイル追加）ボタンをクリックし、「Create new file」（新規ファイル作成）を選択します

![ ](images/file-operation/adding-a-new-file/fig-6.png)


7. エディタ画面に遷移するので、ファイル名のカラム（❶）に`vivliostyle.config.js`と入力し、下記の雛形を参考にしてファイルを完成させてください。終わったら “Commit Changes” ボタン（❷）を押下して、内容を確定します

![ ](images/file-operation/adding-a-new-file/fig-7.png)

`vivliostyle.config.js`の雛形は下記のとおりです。コピーしてお使いください。`----`の部分を書き換えていきます。

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
`title: `（書名）と`author:`（作者）はオプションですが、`entry`のファイル名は必須です。`entry: [`の次の行から、Vivliostyle Pubで表示させたいファイル名をシングルクォート`'　'`で囲み、行末をカンマ`,`で区切って記入していってください。2つ以上のファイルを追加する場合も、この部分にファイルを追記していきます（→[既存ファイルの追加](/ja/file-operation/adding-existing-files.md)）。なお、Vivliostyle Pubはこの部分を参照し、ここで記述された順番どおりに表示します（→[複数ファイルの並べ替え](/ja/file-operation/reordering-files.md)）

- **ご注意**：それぞれの値を囲むシングルクォート`'　'`、値を区切るカンマ`,`をお忘れなく！　間違うとVivliostyle Pubは正しく表示されません。


8. `vivliostyle.config.js`が追加されました

![ ](images/file-operation/adding-a-new-file/fig-8.png)

9. Vivliostyle Pubを再読み込みさせて、追加した`chapter-2.md`（赤矢印）が表示されるか確認します

![ ](images/file-operation/adding-a-new-file/fig-9.png)