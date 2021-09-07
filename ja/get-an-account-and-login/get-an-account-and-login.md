# GitHubアカウントの取得とVivliostyle Pubへのログイン

Vivliostyle Pubベータ版における、ログインまでの詳細な手順をご説明します。

## ①事前の準備（GitHubアカウント／リポジトリを作成していない方）

1. GitHubアカウントを取得する（取得ずみの人は2に進む）
    - [GitHub](https://github.com/) にアクセスし、“Sign up” をクリック、画面の指示に従う
        - 参考資料：[GitHubアカウントの作り方（外部サイト）](https://k-sasaking.net/programing/github-siginup/)
2. アカウント取得後、表示されるダッシュボード画面から、“Create repository” を選択する（fig-1, fig-2）

![Fig-1 “Create repository” の選択-1](/images/get-an-account-and-login/fig-1.png)

![Fig-2 “Create repository” の選択-2](/images/get-an-account-and-login/fig-2.png)

3. リポジトリにindex.md を新規作成する（Fig-3, Fig-4）

![Fig-3 “create a file“ を選択](/images/get-an-account-and-login/fig-3.png)

![Fig-4 ファイル名 “index.md” を入力し、なにか文字を書いて、“Commit new file“ を選択](/images/get-an-account-and-login/fig-4.png)

これで準備完了です！

## ②Vivliostyle Pubへのログイン

1. ブラウザ（Chrome）から以下のURLにアクセスして “Login” をクリック（Fig-5）

https://vivliostyle-pub-develop-proto.vercel.app/

![Fig-5  “Login” をクリックする](/images/get-an-account-and-login/fig-5.png)

2. GitHubの認証画面に遷移するので、Vivliostyle PubとGitHubアカウントを接続する（初回のみ）（Fig-6）

![Fig-6 “Authorize Vivliostyle” をクリック](/images/get-an-account-and-login/fig-6.png)

3. Vivliostyle Pubの画面に戻るので、今度は “Install GitHub Apps” をクリック（Fig-6）

![Fig-6  “Install GitHub Apps” をクリック](/images/get-an-account-and-login/fig-6.png)

4. GitHubの認証画面に遷移するので、“Install” をクリック（Fig-7）

![Fig-7  “Install” をクリック](/images/get-an-account-and-login/fig-7.png)

5. Vivliostyle Pubのウィンドウに切り替え、今度は “Refresh GitHub Access Token” をクリック（Fig-8）

![Fig-8 前のGitHub認証画面から自動でVivliostyle Pubには戻らないので、手でウィンドウを切り替える](/images/get-an-account-and-login/fig-8.png)

6. GitHub認証画面に遷移するので、今度は “Authorize vivliostyle-puv-dev ” をクリック（Fig-9）

![Fig-9 “Authorize vivliostyle-puv-dev ” をクリック](/images/get-an-account-and-login/fig-9.png)

7. 自動的にVivliostyle Pubの画面に戻るので、リポジトリ名をクリック（Fig-10）

![Fig-10 リポジトリ名をクリック](/images/get-an-account-and-login/fig-10.png)

8. Have a happy writing!（Fig-11）

![Fig-11 エディター ／プレビュー画面がひらくので、執筆をはじめましょう。](/images/get-an-account-and-login/fig-11.png)

原稿の執筆フォーマットは、Markdownのバリエーション、Vivliostyle Flavored Markdown（VFM）です。見出しや強調、引用など、一般的なMarkdownの記法が利用可能です。詳しい記法は下記のページをご参照ください。

- [GitHub で書き、フォーマットしてみる/基本的な書き方とフォーマットの構文（外部サイト）](https://docs.github.com/ja/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- [Vivliostyle Flavored Markdown](https://vivliostyle.github.io/vfm/#/vfm)
- [VFM 入門 2021 夏（アカベコ）](https://vivliostyle.org/viewer/#src=https://vivliostyle.github.io/vivliostyle_doc/ja/vivliostyle-user-group-vol5/content/&bookMode=true&f=epubcfi(/10!))