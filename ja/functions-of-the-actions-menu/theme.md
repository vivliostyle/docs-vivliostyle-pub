# Theme（テーマの選択）

## 概要

![ ](images/functions-of-the-actions-menu/theme/fig-1.png)

Actionメニューの「Theme」のメニュー項目を選択することで、以下のテーマ（スタイル情報）に切り替えることができます。

1. Plain theme
2. Custom theme
3. Book theme for latin font
4. 文庫用のテーマ
5. Slide theme
6. Techbook (技術同人誌) theme
7. Academic theme 

以下、テーマ毎にその内容を説明します。ご参考まで、使用したサンプルデータの出典は下記の通りです。なお、スクリーンショットは[プレゼンテーション・モード](/ja/functions-of-the-actions-menu/presentation-mode.md)の表示です。

- 1、2、4……銀河鉄道の夜（宮沢賢治、[青空文庫](https://www.aozora.gr.jp/cards/000081/card456.html)）
- 3………[The Project Gutenberg eBook of Alice’s Adventures in Wonderland, by Lewis Carroll](https://www.gutenberg.org/files/11/11-h/11-h.htm)
- 5 ………[Slide theme 付属のslide.md](https://github.com/vivliostyle/themes/blob/master/packages/%40vivliostyle/theme-slide/example/slide.md)
- 6 ………[Markdown を拡張する MDX はドキュメント作成の新たな可能性？](https://github.com/vivliostyle/vivliostyle_doc/tree/gh-pages/ja/vivliostyle-user-group-vol5/content/spring-raining)（spring-raining、[Vivliostyle で本を作ろう Vol.5所収](https://github.com/vivliostyle/vivliostyle_doc/tree/gh-pages/ja/vivliostyle-user-group-vol5/)）
- 7………[Academic theme付属のfet.md](https://github.com/vivliostyle/themes/blob/master/packages/%40vivliostyle/theme-academic/example/fet.md)

## Plain theme

シンプルで汎用的なスタイルで、Vivliostyle Viewerのデフォルトスタイルシートです。横組で文字サイズは12ポイント、ページサイズはウィンドウに追従します。フォントはブラウザの設定における「標準フォント」で指定されたものを使用します。

![ ](images/functions-of-the-actions-menu/theme/fig-2.png)

- 参考：[Plain themeを選択した際に使われるフォント](/ja/create-and-save-documents/how-to-specify-fonts.md#plain-themeを選択した際に使われるフォント)

## Custom theme

![ ](images/functions-of-the-actions-menu/theme/fig-3.png)

ユーザが作成した任意のスタイルシート（CSSファイル）を適用します。vivliostyle.config.jsでスタイルシートのpathを指定してから（赤線部）、このメニュー項目を選択します。

vivliostyle.config.jsでの記法は下記の通りです。---の部分にpathを記述してください。

```js
module.exports = {
  theme: '---',
 }
```

## Book theme for latin font

![ ](images/functions-of-the-actions-menu/theme/fig-4.png)



## 文庫用のテーマ

![ ](images/functions-of-the-actions-menu/theme/fig-5.png)

Vivliostyleが [npm package として公開](https://www.npmjs.com/package/@vivliostyle/theme-bunko)している公式Themeのひとつです。縦組で文字サイズは8.5ポイント、ページサイズは148×210mm（A5判タテ）、縦中横や柱にも対応しており、長文の読み物に合います。テーマ名の「文庫」は読み物の意味で、文庫版=B6とは違うことに注意してください。

- [@vivliostyle/theme-bunko](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-bunko)

## Slide theme

![ ](images/functions-of-the-actions-menu/theme/fig-6.png)

Vivliostyleが [npm package として公開](https://www.npmjs.com/package/@vivliostyle/theme-slide)している公式Themeのひとつです。横組で文字サイズは12ポイント、ページサイズは210×148mm（A5判ヨコ）、スライド資料に適しています。

見開きではなく、単一ページでプレビューしたい場合は、Vivliostyleのロゴからアクセスできる設定メニューから、“Page Spread View” のうち “Single page” のラジオボタンを選択してください。

- [@vivliostyle/theme-slide](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-slide)

![ ](images/functions-of-the-actions-menu/theme/fig-7.png)

## Techbook (技術同人誌) theme

Vivliostyleが [npm package として公開](https://www.npmjs.com/package/@vivliostyle/theme-techbook)している公式Themeのひとつです。横組で文字サイズは12ポイント、ページサイズは182×257mm（B5判タテ）、コードブロックのクラス指定、[脚注の記法](https://vivliostyle.org/ja/make-books-with-create-book/#%E8%84%9A%E6%B3%A8)もサポートされており、技術同人誌に適しています。

![ ](images/functions-of-the-actions-menu/theme/fig-8.png)

- [@vivliostyle/theme-techbook](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-techbook)

## Academic theme

![ ](images/functions-of-the-actions-menu/theme/fig-9.png)