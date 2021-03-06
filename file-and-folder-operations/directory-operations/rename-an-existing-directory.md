# GitHubでフォルダ名を変更する

1. リポジトリのトップページで「Code」タブが選択されていることを確認します。変更したいフォルダ名をクリックしてください（赤丸）。ここでは`chapter-3`を変更することにします

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-1.png)

2. フォルダ内のファイル一覧画面に遷移しました。フォルダ名の変更は、リポジトリからファイルまでのパス名（経路名）を変更する方法でおこないます。ここでは`section-1.md`（赤丸）をクリックします

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-2.png)

3. `section-1.md`のファイル操作画面に遷移しました。画面右側の鉛筆アイコン（赤丸）をクリックしてください

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-3.png)

4. エディタ画面に遷移します。ファイル名のカラム（赤丸①）をクリックし、写真のようにカーソルをカラム左端まで移動させてください

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-4-1.png)

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-4-2.png)

5. その状態でバックスペースキーを押してみてください。するとフォルダのカラムとファイル名のカラムが1つに合体し、カーソルはフォルダ名とファイル名の間に表示され、フォルダ名`chapter-3`が編集可能になります

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-4-3.png)


6. `-3`の部分をバックスペースキーで削除して、代わりに`-100`と入力しましょう

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-4-4.png)

7. この状態で`/`を入力してください。すると今変更した`chapter-100`がフォルダ名になりました

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-4-5.png)

8. “Commit Changes” （コミットの変更）ボタン（「4」赤丸②）を押下して、変更を確定してください。以下のような`section-1.md`のファイル操作画面に戻ります。画面左上のリポジトリ名（赤丸）をクリックしてください

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-5.png)

9. リポジトリのトップページに戻りました。今おこなったフォルダ名の変更を`vivliostyle.config.js`に反映させましょう。赤丸をクリックします

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-6.png)

10. `vivliostyle.config.js`のファイル操作画面に遷移します。画面右側の鉛筆アイコン（赤丸）をクリックしてください

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-7.png)

11. エディタ画面に遷移しました。以前のフォルダ名`chapter-3`を、変更したフォルダ名`chapter-100`に書き換えましょう（赤矢印）。終わったら、“Commit Changes” （コミットの変更）ボタンを押下して、変更を確定してください

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-8.png)

**変更前**
```js
'chapter-3/section-1.md',
```

**変更後**
```js
'chapter-100/section-1.md',
```

12. リポジトリのトップ画面にもどると、`chapter-100`が追加され、フォルダが2つに増えてていることが分かります（赤丸）

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-9.png)

13. Vivliostyle Pubを再読み込みさせて、追加した`chapter-100/section-1`（赤矢印）が表示されるか確認します

![ ](images/file-and-folder-operations/directory-operations/rename-an-existing-directory/fig-10.png)