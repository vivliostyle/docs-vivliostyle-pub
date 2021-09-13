# 既存ファイルの追加

1. リポジトリのトップページ「Code」タブを表示していることを確認します。

![ ](images/file-operation/adding-existing-files/fig-1.png)

2. 追加したい既存ファイルを1の画面上にドラッグすると、“Drop to upload your files ”（ファイルをドロップしてアップロードします）というメッセージが表示されます。

![ ](images/file-operation/adding-existing-files/fig-2.png)

- 上記スクリーンショットではファイルは1つですが、複数ファイルもドロップできます。
- ただし、すでにリポジトリにファイルがある場合、追加しようとしているものとファイル名が重複しないよう注意してください。その場合は上記画面は表示されず、アップロードできません。


3. 以下の画面に遷移します。内容を確認し、“Commit Changes” ボタン（❸）を押下して、追加を確定してください。

![ ](images/file-operation/adding-existing-files/fig-3.png)

- ❶……ドロップしたファイルがここに表示されます
- ❷……操作をキャンセルしたい場合は、この×マークをクリックしてください
- ❸……問題がなければ、この “Commit Changes” ボタンを押下してください


4. `chapter-3.md`がリポジトリに追加されたことを確認します。次に今追加したファイルを、設定ファイルに追記登録します。`vivliostyle.config.js`（赤丸）をクリックしてください

![ ](images/file-operation/adding-existing-files/fig-4.png)

5. `vivliostyle.config.js`のファイル操作画面に遷移します。画面右側の鉛筆アイコン（赤丸）をクリックしてください

![ ](images/file-operation/adding-existing-files/fig-5.png)

6. エディタ画面に遷移しました。赤矢印の部分に下記の雛形をペースとして`chapter-3.md`を追記しましょう。編集が終わったら“Commit Changes” ボタン（赤丸）を押下して、追加を確定してください

```
    'chapter-3.md',
```

詳細なエディタ画面の操作方法は下記ページの「2」「3」を参照してください

- [新規ファイルの追加](/ja/file-operation/adding-a-new-file.md)



![ ](images/file-operation/adding-existing-files/fig-6.png)

7. Vivliostyle Pubを再読み込みさせて、追加した`chapter-3.md`（赤矢印）が表示されるか確認します。

![ ](images/file-operation/adding-existing-files/fig-7.png)