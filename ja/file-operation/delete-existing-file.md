# ファイル操作

## 既存ファイルの削除

1. Vivliostyle Pub、画面左側のファイルの選択ペインのファイル（赤丸）のうち、任意のものを削除します

![ ](images/file-operation/delete-existing-file/fig-1.png)

2. リポジトリのトップページ「Code」タブを表示していることを確認し、リネームするファイルをクリックしてください。ここでは `index2.md`を削除してみましょう（赤丸）

![ ](images/file-operation/delete-existing-file/fig-2.png)

3. `index3.md` のファイル操作画面に遷移します。画面右側のゴミ箱アイコン（赤丸）をクリックしてください。マウスホバーするとアイコンが赤に変わり、ツールチップで “Delite this file”（このファイルを削除）と表示されます

![ ](images/file-operation/delete-existing-file/fig-3.png)

4. Commit画面に遷移するので、“Commit Changes” ボタン（赤丸）を押下して削除を確定してください。“Commit Changes” のカラムはオプションです。必要に応じて記入してください。記入しておくと履歴を参照したいときに便利です

![ ](images/file-operation/delete-existing-file/fig-4.png)

5. リポジトリのトップページに遷移します。`index2.md`が削除されていることを確認してください

![ ](images/file-operation/delete-existing-file/fig-5.png)

6. `vivliostyle.config.js`を編集して変更内容を反映します。`entry: [`以降の行（赤丸❶）から`index2.md`を削除ししてください。終わったら “Commit Changes” ボタン（赤丸❷）を押下して変更を確定してください。“Commit Changes” のカラムはオプションです。

![ ](images/file-operation/delete-existing-file/fig-6.png)

**変更前**

```
    'index4.md',
    'index2.md',
    'index.md',
```

**変更後**

```
    'index4.md',
    'index.md',
```

エディタ画面への行き方や編集方法は下記ページの「4」以降を参照してください

- [新規ファイルの追加](/ja/file-operation/adding-a-new-file.md)


7. Vivliostyle Pubを再読み込みさせて、ファイルの選択ペインから`index2.md`が削除されているか確認します（赤丸）

![ ](images/file-operation/delete-existing-file/fig-7.png)