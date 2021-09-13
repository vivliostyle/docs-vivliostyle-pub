# 新規ディレクトリの作成


1. リポジトリのトップページ「Code」タブを表示していることを確認します。「Add file」（ファイル追加）ボタンをクリックするとメニュー項目が表示されます（赤丸）。その中から「Create new file」（新規ファイル作成）を選択します

![ ](images/directory-operations/create-a-new-directory/fig-1.png)

2. エディタ画面に遷移します。❶のカラムに新規ディレクトリ名として`chapter-3`と記入してください

![ ](images/directory-operations/create-a-new-directory/fig-2.png)

3. ディレクトリ名`chapter-3`（写真上）につづけて、`/`を入力します。するとすぐ右に新しいカラムが出現して、フォーカスもこのカラムに移動します（写真中）。さっき入力した`chapter-3`は自動的にディレクトリ名になります。新しいカラムにファイル名`section-1.md`を入力してください（写真下）。なお、**ファイルの拡張子は必ず`.md`を指定してください。**Vivliostyle Pubで表示できません

![ ](images/directory-operations/create-a-new-directory/fig-3-1a.png)
<br/><span style="text-indent: 250px;">**↓**</span><br/>
![ ](images/directory-operations/create-a-new-directory/fig-3-2a.png)
<br/>**↓**<br/>
![ ](images/directory-operations/create-a-new-directory/fig-3-3a.png)

4. “Commit Changes” ボタン（赤丸）を押下して、変更を確定してください

![ ](images/directory-operations/create-a-new-directory/fig-4.png)


5. つづけて、今作成したディレクトリ`chapter-3`の中に、もう1つファイルを追加してみましょう。パス（赤丸）が`mybook/chapter-3`と表示されていることを確認して、「Add file」（ファイル追加）ボタンをクリックするとメニュー項目が表示されます（赤丸）。その中から「Create new file」（新規ファイル作成）を選択します

![ ](images/directory-operations/create-a-new-directory/fig-5.png)

6. 前記「3」「4」と同じ操作をします。ファイル名のカラムには`chapter-3/section-2`と入力してください。“Commit Changes” ボタンで変更を確定すると、以下のような画面になります。新たに`section-2.md`（赤矢印）が追加されていることを確認してください

![ ](images/directory-operations/create-a-new-directory/fig-6.png)

7. 次に今追加したファイルを、設定ファイルに追記登録します。`vivliostyle.config.js`（赤丸）をクリックしてください

![ ](images/directory-operations/create-a-new-directory/fig-7.png)

8. `vivliostyle.config.js`のファイル操作画面に遷移します。画面右側の鉛筆アイコン（赤丸）をクリックしてください

![ ](images/directory-operations/create-a-new-directory/fig-8.png)

9. エディタ画面に遷移しました。`chapter-3/section-1`と`chapter-3/section-2`を追記しましょう（赤矢印）。編集が終わったら“Commit Changes” ボタン（赤丸）を押下して、変更を確定してください

![ ](images/directory-operations/create-a-new-directory/fig-9.png)

**変更前**
```
module.exports = {
  title: '私の本',
  author: '尾久綿次郎',
  entry: [
    'chapter-2.md',
    'chapter-1.md',
  ]
}
```

**変更後**
```
module.exports = {
  title: '私の本',
  author: '尾久綿次郎',
  entry: [
    'chapter-2.md',
    'chapter-1.md',
    'chapter-3/section-1.md',
    'chapter-3/section-2.md',
  ]
}
```
詳細なエディタ画面の操作方法は下記ページの「2」「3」を参照してください

- [新規ファイルの追加](/ja/file-operation/adding-a-new-file.md)


10. Vivliostyle Pubを再読み込みさせて、追加した`chapter-3/section-1`と`chapter-3/section-2`（赤矢印）が表示されるか確認します。

![ ](images/directory-operations/create-a-new-directory/fig-10.png)



