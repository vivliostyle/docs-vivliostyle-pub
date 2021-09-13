# 既存ファイルの削除

1. Vivliostyle Pub、画面左側のファイルの選択ペインのファイル（赤丸）のうち、任意のものを削除します

![ ](images/file-operation/delete-existing-file/fig-1.png)

2. リポジトリのトップページ「Code」タブを表示していることを確認し、リネームするファイルをクリックしてください。ここでは`chapter-100.md`を削除してみましょう（赤丸）

![ ](images/file-operation/delete-existing-file/fig-2.png)

3. `chapter-100.md`のファイル操作画面に遷移します。画面右側のゴミ箱アイコン（赤丸）をクリックしてください。マウスホバーするとアイコンが赤に変わり、ツールチップで “Delite this file”（このファイルを削除）と表示されます

![ ](images/file-operation/delete-existing-file/fig-3.png)

4. Commit画面に遷移するので、“Commit Changes” ボタン（赤丸）を押下して削除を確定してください

![ ](images/file-operation/delete-existing-file/fig-4.png)

5. リポジトリのトップページに遷移します。`chapter-100.md`が削除されていることを確認してください

![ ](images/file-operation/delete-existing-file/fig-5.png)

6. つづいて、今変更したファイル名を、設定ファイルに反映させます。リポジトリのトップページ「Code」タブから、`vivliostyle.config.js`（赤矢印）をクリックしてください

![ ](images/file-operation/delete-existing-file/fig-6.png)


7. `vivliostyle.config.js`のファイル操作画面で鉛筆アイコン（赤丸）をクリックします。

![ ](images/file-operation/delete-existing-file/fig-7.png)


8. エディタ画面に遷移します。`entry: [`以降の行（赤丸❶）から`chapter-100.md`を削除ししてください。終わったら “Commit Changes” ボタン（赤丸❷）を押下して変更を確定してください。“Commit Changes” のカラムはオプションです

![ ](images/file-operation/delete-existing-file/fig-8.png)

**変更前**

```
    `chapter-100.md`,
    `chapter-2.md`,
    `chapter-1.md`,
```

**変更後**

```
    `chapter-2.md`,
    `chapter-1.md`,
```

詳細なエディタ画面の操作方法は下記ページの「2」「3」を、`vivliostyle.config.js`の編集方法は同ページの「7」を参照してください

- [新規ファイルの追加](/ja/file-operation/adding-a-new-file.md)



9. Vivliostyle Pubを再読み込みさせて、ファイルの選択ペインから`chapter-100.md`が削除されているか確認します（赤丸）

![ ](images/file-operation/delete-existing-file/fig-9.png)