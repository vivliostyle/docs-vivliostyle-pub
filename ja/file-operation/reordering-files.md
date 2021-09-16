# 複数ファイルの並べ替え

1. Vivliostyle Pub、画面左側のファイルの選択ペインのファイルの順番（赤丸）を、任意のものに変更します

![ ](images/file-operation/reordering-files/fig-1.png)

2. リポジトリのトップページで「Code」タブが選択されていることを確認し、`vivliostyle.config.js`（赤丸）をクリックしてください

![ ](images/file-operation/reordering-files/fig-2.png)

3. `vivliostyle.config.js`のファイル操作画面に遷移します。画面右側の鉛筆アイコン（赤丸）をクリックしてください

![ ](images/file-operation/reordering-files/fig-3.png)

4. エディタ画面に遷移します。ファイル名を任意の順番に書き換えてください（赤丸①）。ここでは昇順から降順に書き換えています。編集が終わったら、“Commit Changes” （コミットの変更）ボタンを押下して、変更を確定してください（赤丸②）

![ ](images/file-operation/reordering-files/fig-4.png)

**変更前**

```js
    'chapter-1.md',
    'chapter-2.md',
    'chapter-100.md',
```

**変更後**

```js
    'chapter-100.md',
    'chapter-2.md',
    'chapter-1.md',
```

詳細なエディタ画面の操作方法は下記ページの「2」「3」を、`vivliostyle.config.js`の編集方法は同ページの「7」を参照してください

- [新規ファイルの追加](/ja/file-operation/adding-a-new-file.md)



5. Vivliostyle Pubを再読み込みさせて、ファイルの選択ペインのファイルの順番（赤丸）が降順に変更されたか確認します

![ ](images/file-operation/reordering-files/fig-5.png)