# 既存ファイルの追加

1. リポジトリのトップページ「Code」タブを表示していることを確認します。

![ ](images/file-operation/adding-existing-files/fig-1.png)

2. 追加したい既存ファイルを1の画面上にドラッグすると、“Drop to upload your files ”（ファイルをドロップしてアップロードします）というメッセージが表示されます。

![ ](images/file-operation/adding-existing-files/fig-2.png)

- 上記スクリーンショットではファイルは1つですが、複数ファイルもドロップできます。
- ただし、すでにリポジトリにアップロードされているファイルと、ファイル名が重複しないよう注意してください。その場合は上記画面は表示されず、アップロードできません。

3. 以下の画面に遷移します。内容を確認し、“Commit Changes” ボタン（❸）を押下して、追加を確定してください。“Commit Changes” のカラムはオプションです。必要に応じて記入してください。記入しておくと履歴を参照したいときに便利です

![ ](images/file-operation/adding-existing-files/fig-3.png)

- ❶……ドロップしたファイルがここに表示されます
- ❷……操作をキャンセルしたい場合は、この×マークをクリックしてください
- ❸……問題がなければ、この “Commit Changes” ボタンを押下してください


4. 今、追加した`index3.md`を、`vivliostyle.config.js`に追記登録します（赤矢印）。エディタ画面への行き方や編集方法は下記ページの「4」以降を参照してください。


- [新規ファイルの追加](/ja/file-operation/adding-a-new-file.md)

![ ](images/file-operation/adding-existing-files/fig-4.png)


5. GitHubリポジトリに`vivliostyle.config.js`が追加されました。

![ ](images/file-operation/adding-existing-files/fig-5.png)

6. Vivliostyle Pubを再読み込みさせて、追加した`index3.md`（赤矢印）が表示されるか確認します。

![ ](images/file-operation/adding-existing-files/fig-6.png)