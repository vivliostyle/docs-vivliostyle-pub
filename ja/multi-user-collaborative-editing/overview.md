# 概要

## GitHubを利用するメリット

Vivliostyle Pubはユーザーファイルの管理に、外部のバージョン管理システム、[GitHub](https://github.co.jp/)を利用しています。ユーザにとってバージョン管理システムは、以下のようなメリットがあります。

1. ファイルの変更履歴が記録できる
2. ファイルを以前の状態に戻せる
3. 複数ユーザによる共同編集ができる

残念ながら、現在のバージョンでは上記、1、2をVivliostyle Pub上から実行できません。これらの機能は各種GitHubクライアントでご利用ください。たとえば、GitHubの公式クライアントである[GitHub Desktop](https://docs.github.com/ja/desktop/installing-and-configuring-github-desktop)での操作は、下記を参照してください。

- [ブランチ履歴の表示](https://docs.github.com/ja/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/viewing-the-branch-history)
- [プロジェクトへの変更のコミットやレビュー](https://docs.github.com/ja/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/committing-and-reviewing-changes-to-your-project)

ここでは上記3、複数ユーザによる共同編集をVivliostyle Pubでおこなう方法について説明します。

## 共同編集の概要

（この文書では、個々の作業者を「コミッター」、プロジェクトを統括する者を「管理者」とします）

共同編集では、GitHubの[「保護されたブランチ」](https://docs.github.com/ja/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches)機能を使います。この機能により、本流であるデフォルトブランチで直接編集することが禁止され、作業者は傍流である自分の作業ブランチで編集し、これを管理者のレビューを介してデフォルトブランチへ合流させることが徹底されます。こうした共同作業の結果、間違いの少ない文書を効率的に制作できます。

共同編集は、おおむね以下のような手順ですすめます（次章で詳しく説明します）。

1. コミッターがGitHubのリポジトリでブランチを新規作成する
1. コミッターがVivliostyle Pubでそのブランチを選択する
1. コミッターがVivliostyle Pubで文書を編集し、保存する
1. コミッターがGitHubでプルリクエストを作成する
1. 管理者がGitHubでプルリクエストをレビューし、承認とマージをする

## 共同編集に必要な条件

上に述べた[「保護されたブランチ」](https://docs.github.com/ja/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches)機能を使うには、GitHubの有償アカウントを取得するか、無償アカウント（Free）の場合はリポジトリを公開（Public）する必要があります。詳細は下記を参照してください。

- [GitHub の商品と価格プランの概要](https://docs.github.com/ja/get-started/learning-about-github/githubs-products)