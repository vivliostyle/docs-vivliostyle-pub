# Theme（テーマの選択）

## 概要

![ ](images/functions-of-the-actions-menu/theme/fig-1.png)

Actionメニューの「Theme」以下のメニュー項目を選択することで以下のテーマ（スタイル情報）に切り替えることができます。

1. Plain theme
2. Custom theme
3. 文庫用のテーマ
4. Slide theme
5. Techbook (技術同人誌) theme

以下、テーマ毎にその内容を説明します。サンプルデータの出典は下記の通りです。

- 1〜3……銀河鉄道の夜（宮沢賢治、[青空文庫](https://www.aozora.gr.jp/cards/000081/card456.html)）
- 4 ………[Slide theme 付属のslide.md](https://github.com/vivliostyle/themes/blob/master/packages/%40vivliostyle/theme-slide/example/slide.md)
- 5 ………[Markdown を拡張する MDX はドキュメント作成の新たな可能性？](https://github.com/vivliostyle/vivliostyle_doc/tree/gh-pages/ja/vivliostyle-user-group-vol5/content/spring-raining)（spring-raining、[Vivliostyle で本を作ろう Vol.5所収](https://github.com/vivliostyle/vivliostyle_doc/tree/gh-pages/ja/vivliostyle-user-group-vol5/)）

## Plain theme

シンプルで汎用的なスタイルで、Vivliostyle Viewerのデフォルトスタイルシートです。横組で文字サイズは12ポイント、ページサイズはウィンドウに追従します。

![ ](images/functions-of-the-actions-menu/theme/fig-2.png)

## Custom theme

![ ](images/functions-of-the-actions-menu/theme/fig-3.png)

ユーザが作成した任意のスタイルシート（CSSファイル）を適用します。vivliostyle.config.jsでスタイルシートのpathを指定してから（赤線部）、このメニュー項目を選択してくだい。

## 文庫用のテーマ

![ ](images/functions-of-the-actions-menu/theme/fig-4.png)

Vivliostyleが [npm package として公開](https://www.npmjs.com/package/@vivliostyle/theme-bunko)している公式Themeのひとつです。縦組で文字サイズは8.5ポイント、ページサイズは148×210mm（A5判タテ）、縦中横や柱にも対応しており、長文の読み物に合います。テーマ名の「文庫」は読み物の意味で、文庫版=B6とは違うことに注意してください。

- [@vivliostyle/theme-bunko](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-bunko)

## Slide theme

![ ](images/functions-of-the-actions-menu/theme/fig-5.png)

Vivliostyleが [npm package として公開](https://www.npmjs.com/package/@vivliostyle/theme-slide)している公式Themeのひとつです。横組で文字サイズは12ポイント、ページサイズは210×148mm（A5判ヨコ）、スライド資料に適しています。

見開きではなく、単一ページでプレビューしたい場合は、Vivliostyleのロゴからアクセスできる設定メニューから、“Page Spread View” のうち “Single page” のラジオボタンを選択してください。

- [@vivliostyle/theme-slide](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-slide)

![ ](images/functions-of-the-actions-menu/theme/fig-6.png)

## Techbook (技術同人誌) theme

Vivliostyleが [npm package として公開](https://www.npmjs.com/package/@vivliostyle/theme-techbook)している公式Themeのひとつです。横組で文字サイズは12ポイント、ページサイズは182×257mm（B5判タテ）、コードブロックのクラス指定、[脚注の記法](https://vivliostyle.org/ja/make-books-with-create-book/#%E8%84%9A%E6%B3%A8)もサポートされており、技術同人誌に適しています。

![ ](images/functions-of-the-actions-menu/theme/fig-7.png)

- [@vivliostyle/theme-techbook](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-techbook)