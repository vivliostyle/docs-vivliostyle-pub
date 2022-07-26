#  クイックスタートガイド 

## 必要環境 

- Chromeブラウザ（PC版）が動作する環境であること
- GitHubアカウントを既に取得していること

## 初期画面

以下のURLにアクセスすると、以下の初期画面が表示されます。

https://vivliostyle-pub-develop.vercel.app/

①「Login」ボタンを押して、GitHubアカウントでログインしてください（→[GitHubアカウントの取得方法](/advance-preparation/get-an-account#github%E3%82%A2%E3%82%AB%E3%82%A6%E3%83%B3%E3%83%88%E3%81%AE%E5%8F%96%E5%BE%97%E6%96%B9%E6%B3%95)）。なお、②言語メニューから使用言語を選択することができます（English / 日本語）。

![](images/readme-first/fig-1.png)

## リポジトリとブランチの選択

ログインするとすると以下の画面でリポジトリを選択します。リポジトリに複数のブランチがある場合はブランチも選択できます。公開リポジトリは“Public”、非公開は“Private” と表示されます。

![](images/readme-first/fig-2.png)

①……リポジトリの選択<br>
②……リポジトリ表示の更新<br>
③……GitHubアプリのインストール（→[最初のログインで必要な作業](/advance-preparation/login.md)）<br>
④……GitHubアクセス・トークンのリフレッシュ（→[最初のログインで必要な作業](/advance-preparation/login.md)）<br>
⑤……GitHubアカウントのユーザ名（[GitHub > Settings > Public profile](https://github.com/settings/profile)）<br>
⑥……言語メニュー（English / 日本語）<br>

いずれかのリポジトリ（①）をクリックすると、自動的にエディタ／プレビュー画面に遷移します。

## ログアウト／利用者アンケートの送付／不具合のフィードバック

GitHubアカウントのユーザ名をクリックすると、プルダウンメニューが表示されます。ログアウトはメニュー項目の一番下です。これを選択すると、ログアウトして初期画面に戻ります。また、このメニューから利用者アンケートの送付や不具合のフィードバックができます。ぜひご利用ください。

![](images/readme-first/fig-3.png)

①……利用者アンケートの送付<br>
②……不具合のフィードバック<br>
③……ログアウト<br>

## エディタ／プレビュー画面

![](images/readme-first/fig-4.png)

**ペイン境界線の移動**：ファイル一覧ペイン、エディタ・ペイン、プレビュー・ペインの境界線は変更できます。それぞれの区画の境界線上にマウスカーソルを置いてください。左右矢印の形状に変わったところでマウスボタンをプレスして右か左にドラッグすると、境界線が左右に移動します。

### メニュー・エリア

![](images/readme-first/fig-5.png)

①……ユーザ名 / リポジトリ名<br>
②……ブランチ切り替えメニュー<br>
③……ファイル保存ボタン<br>
④……GitHubアカウントのユーザ名（プルダウンメニュー→アンケート送付／フィードバック／ログアウト）<br>
⑤……言語メニュー（English / 日本語）<br>
⑥……ファイル一覧ペインの表示／非表示<br>
⑦……エディタ・ペインの表示／非表示<br>
⑧……プレビュー・ペインの表示／非表示<br>
⑨……Actionメニュー（→ [Theme（スタイル情報の選択）](/ja/functions-of-the-actions-menu/theme.md)、[Export（出力）](/ja/functions-of-the-actions-menu/export.md)など）<br>

### ファイル一覧ペイン

![](images/readme-first/fig-6.png)

- ①……リポジトリ内のファイル名を検索<br>
- ②……リポジトリのファイル一覧を再取得<br>
- ③……![](https://github.com/microsoft/vscode-codicons/raw/main/src/icons/arrow-up.svg) リポジトリにファイルをアップロード<br>
- ④……![](https://github.com/microsoft/vscode-codicons/raw/main/src/icons/new-folder.svg) リポジトリにフォルダを新規作成<br>
- ⑤……![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/new-file.svg) リポジトリにファイルを新規作成<br>
- ⑥……現在編集中のファイル（**太字**）<br>
- ⑦……リポジトリ内のファイル一覧<br>
- **アイコン種別一覧**
  - ![](https://raw.githubusercontent.com/astrit/css.gg/master/icons/svg/corner-left-up.svg)……上位フォルダへ移動
  - ![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/folder.svg)……フォルダ
  - ![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/file-media.svg)……画像ファイル
  - ![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/code.svg)……HTMLファイル
  - ![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/symbol-namespace.svg)……CSSファイル
  - ![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/markdown.svg)……Markdownファイル
  - ![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/settings-gear.svg)……vivliostyle.config.js
  - ![](https://raw.githubusercontent.com/microsoft/vscode-codicons/main/src/icons/file.svg)……その他のファイル



### プレビュー・ペイン

![](images/readme-first/fig-7.png)

①……ファイル内の文字列を検索<br>
②……ページ移動ボタン（左から先頭ページへ移動、前のページへ移動、後のページへ移動、末尾ページへ移動／単一ページの場合はグレイアウト）<br>
③……ページカウンター（現在のページ／総ページ）<br>
④……文字サイズ変更（左から小さく、大きく、デフォルト）<br>
⑤……ズーム（左から縮小、拡大、等倍、フィットページ）<br>
⑥……ページ移動スライドバー<br>