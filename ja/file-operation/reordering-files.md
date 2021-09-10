# ファイル操作

## 複数ファイルの並べ替え

1. Vivliostyle Pub、画面左側のファイルの選択ペインのファイルの順番（赤丸）を、任意のものに変更します

![ ](images/file-operation/reordering-files/fig-1.png)

2. リポジトリのトップページ「Code」タブを表示していることを確認し、`vivliostyle.config.js`（赤丸）をクリックしてください

![ ](images/file-operation/reordering-files/fig-2.png)

3. `vivliostyle.config.js`のファイル操作画面に遷移します。画面右側の鉛筆アイコン（赤丸）をクリックしてください

![ ](images/file-operation/reordering-files/fig-3.png)

4. エディタ画面に遷移するので、Edit new fileタブで編集してください。必要に応じて記入してください。記入しておくと履歴を参照したいときに便利です

![ ](images/file-operation/reordering-files/fig-4.png)

**変更前**

```
    'index.md',
    'index2.md',
    'index4.md',
```

**変更後**

```
    'index4.md',
    'index2.md',
    'index.md',
```

エディタ画面への行き方や編集方法は下記ページの「4」以降を参照してください


- [新規ファイルの追加](ja/file-operation/adding-a-new-file.md)


5. Vivliostyle Pubを再読み込みさせて、ファイルの選択ペインのファイルの順番（赤丸）が降順に変更されたか確認します

![ ](images/file-operation/reordering-files/fig-5.png)