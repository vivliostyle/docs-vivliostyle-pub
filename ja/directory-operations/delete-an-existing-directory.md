# 既存ディレクトリの削除

1. リポジトリのトップページで「Code」タブが選択されていることを確認します。削除したいディレクトリ名をクリックしてください（赤丸）。ここでは`chapter-100`を削除することにします

![ ](images/directory-operations/delete-an-existing-directory/fig-1.png)

2. ディレクトリ内のファイル一覧画面に遷移しました。ディレクトリ名の削除は、リポジトリからファイルまでのパス名（経路名）のうちディレクトリ名を削除する方法でおこないます。手順は[既存ファイル名の変更](/ja/file-operation/renaming-an-existing-file.md)とよく似ています。ディレクトリ内のいずれかのファイル名をクリックしてください。ここでは`section-1.md`（赤丸）をクリックします

![ ](images/directory-operations/delete-an-existing-directory/fig-2.png)

3. `section-1.md`のファイル操作画面に遷移しました。画面右側の鉛筆アイコン（赤丸）をクリックしてください

![ ](images/directory-operations/delete-an-existing-directory/fig-3.png)

4. エディタ画面に遷移します。ファイル名のカラム（赤丸①）をクリックし、写真のようにカーソルをカラム左端まで移動させてください

![ ](images/directory-operations/delete-an-existing-directory/fig-4.png)

![ ](images/directory-operations/delete-an-existing-directory/fig-4a.png)

5. その状態でバックスペースキーを押してみてください。するとディレクトリのカラムとファイル名のカラムが1つに合体し、カーソルはディレクトリ名とファイル名の間に表示され、ディレクトリ名`chapter-100`が編集可能になります

![ ](images/directory-operations/delete-an-existing-directory/fig-5a.png)

6. `chapter-100`の部分をそっくりバックスペースキーで削除しましょう。

![ ](images/directory-operations/delete-an-existing-directory/fig-6a.png)

7. 削除が終わったら“Commit Changes” （コミットの変更）ボタン（赤丸）を押下して変更を確定すると、ファイル操作画面に戻ります。画面左上のリポジトリ名をクリックしてください

![ ](images/directory-operations/delete-an-existing-directory/fig-7.png)

8. リポジトリのトップページに戻りました。今おこなったディレクトリの削除を`vivliostyle.config.js`に反映させましょう。赤丸をクリックします

![ ](images/directory-operations/delete-an-existing-directory/fig-8.png)

9. `vivliostyle.config.js`のファイル操作画面に遷移します。画面右側の鉛筆アイコン（赤丸）をクリックしてください

![ ](images/directory-operations/delete-an-existing-directory/fig-9.png)

10. エディタ画面に遷移しました。削除したディレクトリ名`chapter-100/`の部分を削除しましょう（赤矢印）

![ ](images/directory-operations/delete-an-existing-directory/fig-10.png)

![ ](images/directory-operations/delete-an-existing-directory/fig-10a.png)

![ ](images/directory-operations/delete-an-existing-directory/fig-11a.png)

詳細なエディタ画面の操作方法は下記ページの「2」「3」を参照してください

- [新規ファイルの追加](/ja/file-operation/adding-a-new-file.md)


11. 削除し終わったら、“Commit Changes” （コミットの変更）ボタン（赤丸）を押下して、変更を確定してください。

![ ](images/directory-operations/delete-an-existing-directory/fig-11.png)

12. Vivliostyle Pubを再読み込みさせて、追加した`chapter-100/`（赤矢印）が削除されているか確認します

![ ](images/directory-operations/delete-an-existing-directory/fig-12.png)