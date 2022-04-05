# Theme（テーマの選択）

## 概要

![ ](images/functions-of-the-actions-menu/theme/fig-1.png)

Actionメニューの「Theme」以下のメニュー項目を選択することで以下のテーマ（スタイル情報）に切り替えることができます。

1. Plain theme
2. Custom theme
3. 文庫用のテーマ
4. Slide theme
5. Techbook (技術同人誌) theme

## Plain theme

シンプルで汎用的なスタイルで、Vivliostyle Viewerのデフォルトスタイルシートです。横組で文字サイズは12ポイント、ページサイズはウィンドウに追従します。

![ ](images/functions-of-the-actions-menu/theme/fig-2.png)

## Custom theme

![ ](images/functions-of-the-actions-menu/theme/fig-3.png)

ユーザが作成した任意のスタイルシート（CSSファイル）を適用します。vivliostyle.config.jsでスタイルシートのpathを指定してから（赤線部）、このメニュー項目を選択してくだい。

## 文庫用のテーマ

![ ](images/functions-of-the-actions-menu/theme/fig-4.png)

Vivliostyleが npm package として公開している公式Themeのひとつです。縦組で文字サイズは8.5ポイント、ページサイズは148×210mm（A5判タテ）、縦中横やルビにも対応しており、長文の読み物に合います。テーマ名の「文庫」は読み物の意味で、文庫版=B6とは違うことに注意してください

- [@vivliostyle/theme-bunko](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-bunko)

## Slide theme

![ ](images/functions-of-the-actions-menu/theme/fig-5.png)

Vivliostyleが npm package として公開している公式Themeのひとつです。横組で文字サイズは12ポイント、ページサイズは210×148mm（A5判ヨコ）、スライド資料に適しています。

- [@vivliostyle/theme-slide](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-slide)

見開きではなく、単一ページで表示したい場合は、Vivliostyleのロゴからアクセスできる設定メニューから、Page Spread ViewでSingle pageのラジオボタンを選択してください。

![ ](images/functions-of-the-actions-menu/theme/fig-6.png)

## Techbook (技術同人誌) theme

Vivliostyleが npm package として公開している公式Themeのひとつです。横組で文字サイズは12ポイント、ページサイズは182×257mm（B5判タテ）、コードブロックのクラス指定、[脚注の記法](https://vivliostyle.org/ja/make-books-with-create-book/#%E8%84%9A%E6%B3%A8)もサポートされており、技術同人誌に適しています。

![ ](images/functions-of-the-actions-menu/theme/fig-7.png)

- [@vivliostyle/theme-techbook](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-techbook)


