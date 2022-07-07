# Theme（テーマの選択）

## 概要

![ ](images/functions-of-the-actions-menu/theme/fig-1.png)

Actionメニューの「Theme」の項目を選択することで、以下のテーマ（スタイル情報）に切り替えることができます。

1. Plain theme
2. Custom theme
3. Book theme for latin font
4. 文庫用のテーマ
5. Slide theme
6. Techbook (技術同人誌) theme
7. Academic theme 

以下では、テーマ毎にその内容を概説します。使用したサンプルデータの出典は下記の通りです。なお、スクリーンショットは[プレゼンテーション・モード](/ja/functions-of-the-actions-menu/presentation-mode.md)での表示です。

- 1、2、4……銀河鉄道の夜（宮沢賢治、[青空文庫](https://www.aozora.gr.jp/cards/000081/card456.html)）
- 3………[The Project Gutenberg eBook of Alice’s Adventures in Wonderland, by Lewis Carroll](https://www.gutenberg.org/files/11/11-h/11-h.htm)
- 5 ………[Slide theme 付属のslide.md](https://github.com/vivliostyle/themes/blob/master/packages/%40vivliostyle/theme-slide/example/slide.md)
- 6 ………[Markdown を拡張する MDX はドキュメント作成の新たな可能性？](https://github.com/vivliostyle/vivliostyle_doc/tree/gh-pages/ja/vivliostyle-user-group-vol5/content/spring-raining)（spring-raining、[Vivliostyle で本を作ろう Vol.5所収](https://github.com/vivliostyle/vivliostyle_doc/tree/gh-pages/ja/vivliostyle-user-group-vol5/)）
- 7………[Academic theme付属のfet.md](https://github.com/vivliostyle/themes/blob/master/packages/%40vivliostyle/theme-academic/example/fet.md)

## Plain theme

ブラウザのデフォルト設定を使った、シンプルなスタイルです。横組で文字サイズは12ポイント、ページサイズは非定型でウィンドウに追従します。フォントはブラウザの設定で「標準フォント」に指定されたものが使用されます。

![ ](images/functions-of-the-actions-menu/theme/fig-2.png)

Plain themeは手早くプレビューを確認するためのもので出力は想定していません。イメージ通りのスタイルでPDF出力をしたい場合は、後述のVivliostyle公式テーマの中から選択するか、自分でCustom themeを作成してください。フォントについては下記も参照してください。

- [Plain themeで使われるフォント](/ja/create-and-save-documents/how-to-specify-fonts.md#plain-themeで使われるフォント)

## Custom theme

![ ](images/functions-of-the-actions-menu/theme/fig-3.png)

この項目を選択すると、ユーザーが作成した任意のスタイルシート（CSSファイル）が利用でき、さらにそのスタイルシートにもとづき、PDFの出力ができます（→[Export（PDF）](/ja/functions-of-the-actions-menu/export.md#export出力)）。

`vivliostyle.config.js`で以下のようにスタイルシートのpathを指定してください（上スクリーンショットの赤線部）。記法は下記の通りです。`---`の部分にpathを記述してください。

```js
module.exports = {
  theme: '---',
 }
```

その上で、`Actionメニュー > Custom theme`を選択することでCustom themeに切り替えられます。

なお、Vivliostyle PubではプレビューとPDF出力で組版エンジンのある場所が違うため、Custom themeの作成に当たってなかなか自分が指定した通りのフォントが表示されなかったり、プレビューとPDFとでページがずれてしまうことが起こり得ます。事前に以下の記事を参照して、プレビューとPDF出力とでフォントを一致するよう作成することをお勧めします。

- [フォントの指定方法](/ja/create-and-save-documents/how-to-specify-fonts.md)
- [クラウドにインストールされているフォント一覧](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウドにインストールされているフォント一覧)
- [クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)

## Book theme for latin font

英語をはじめとしたラテン文字書籍のためのスタイルシートです。横組で文字サイズは`small` （デフォルトの16pxよりも一回り小さい）、ページサイズは非定型でウィンドウサイズに追従します。

![ ](images/functions-of-the-actions-menu/theme/fig-4.png)

これはVivliostyleが [npm packageとして公開](https://www.npmjs.com/package/@vivliostyle/theme-gutenberg)している公式Theme、[@vivliostyle/theme-gutenberg](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-gutenberg)そのものです。以下にその一部を引用します。

```css
html {
  max-width: 90ch;
  margin: auto;
  font-family: Georgia, serif;
}
/* 中略 */
@page {
  font-size: small;
  font-family: Georgia, serif;
  margin: 4rem 10%;
  @top-center {
    color: gray;
    font-variant: small-caps;
  }
}

```

上記でフォントは`Georgia`と`serif`が指定されています。多くのPCには`Georgia`がインストールされているはずです。一方、Vivliostyle PubでPDF出力をおこなうクラウド（前掲図2）にも`Georgia`がインストールされているので、このテーマでは多くの場合プレビューとPDF出力のフォントは一致するでしょう。ただし、フォントのバージョン不一致により一致しない場合もあることにご注意ください（クラウドのフォントは比較的古いバージョンです）。

より詳細は下記をご参照ください。

- [Vivliostyle公式Themeで使われるフォント](/ja/create-and-save-documents/how-to-specify-fonts.md#vivliostyle公式themeで使われるフォント)
- [クラウドにインストールされているフォント一覧](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウドにインストールされているフォント一覧)

## 文庫用のテーマ

縦組で文字サイズは8.5ポイント、ページサイズは148×210mm（A5判タテ）、縦中横や柱にも対応しており、長文の読み物に合います。テーマ名の「文庫」は読み物の意味で、文庫判（B6判）とは違うことに注意してください。

![ ](images/functions-of-the-actions-menu/theme/fig-5.png)

これはVivliostyleが [npm packageとして公開](https://www.npmjs.com/package/@vivliostyle/theme-bunko)している公式Theme、[@vivliostyle/theme-bunko](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-bunko)そのものです。以下にその一部を引用します。

```css
html {
  writing-mode: vertical-rl;
  orphans: 1;
  widows: 1;
}
/* 中略 */
@page {
  size: 148mm 210mm;
  width: 360pt;
  height: 468pt;
  margin: auto;
  font-size: 8.5pt;
  font-family: "游明朝", "YuMincho", serif;
}
```

上記でフォントは`游明朝`が指定されています。WindowsでもMacでも`游明朝`はプリインストールされているので、プレビューではこれが使用されます（ただし、WindowsとMacではウェイトが多少異なります）。一方、PDF出力では`Noto Serif CJK JP`に置き換えられます。この結果、プレビューとPDF出力とでは行がずれることが起こり得ます（たとえば下記スクリーンショットではプレビューと比べて3行、後にずれています）。より詳細は下記をご参照ください。

![ ](images/functions-of-the-actions-menu/theme/fig-6.png)

- [Vivliostyle公式Themeで使われるフォント](/ja/create-and-save-documents/how-to-specify-fonts.md#vivliostyle公式themeで使われるフォント)
- [クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)

## Slide theme

横組で文字サイズは12ポイント、ページサイズは210×148mm（A5判ヨコ）、スライド資料に適しています。

![ ](images/functions-of-the-actions-menu/theme/fig-7.png)

これはVivliostyleが [npm package として公開](https://www.npmjs.com/package/@vivliostyle/theme-slide)している公式Theme、[@vivliostyle/theme-slide](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-slide)そのものです。以下にその一部を引用します。

```css
html {
  font-family: 'Noto', 'YuGothic', 'Yu Gothic', 'Meiryo', sans-serif;
  font-feature-settings: 'palt' on;
  font-size: 150%;
  font-weight: 500;
  line-height: 1.5;
}

@page {
  size: 210mm 148mm;
  margin: 12mm 0 0;
  padding: 0 0 18mm;
  background-position: center bottom;
  background-repeat: no-repeat;
  background-size: contain;
  font-size: 11pt;
  line-height: 1.2;
  /* 中略 */
  }
```

上記でフォントは優先度順に、1. `Noto Serif CJK JP`、2. `游ゴシック`、3. `メイリオ` 4. `sans-serif` と指定されています。プレビューでは、1〜3までのフォントがインストールされていない場合、ブラウザ設定の「Sans Serif フォント」の指定に従います。一方、PDF出力ではすべて`Noto Serif CJK JP`に置き換えられます。

- [Vivliostyle公式Themeで使われるフォント](/ja/create-and-save-documents/how-to-specify-fonts.md#vivliostyle公式themeで使われるフォント)
- [クラウド上のVivliostyle CLIの代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliの代替フォントルール)

なお、見開きではなく、単一ページでプレビューしたい場合は、Vivliostyleのロゴからアクセスできる設定メニューを開き、“Page Spread View” のうち “Single page” のラジオボタンを選択してください。

![ ](images/functions-of-the-actions-menu/theme/fig-8.png)

より詳細は下記をご参照ください。

- [Vivliostyle公式Themeで使われるフォント](/ja/create-and-save-documents/how-to-specify-fonts.md#vivliostyle公式themeで使われるフォント)
- [クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)

## Techbook (技術同人誌) theme

横組で文字サイズは12ポイント、ページサイズは182×257mm（B5判タテ）、コードブロックのクラス指定、[脚注の記法](https://vivliostyle.org/ja/make-books-with-create-book/#%E8%84%9A%E6%B3%A8)もサポートされており、技術同人誌に適しています。

![ ](images/functions-of-the-actions-menu/theme/fig-9.png)

これはVivliostyleが [npm package として公開](https://www.npmjs.com/package/@vivliostyle/theme-techbook)している公式Theme、[@vivliostyle/theme-techbook](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-techbook)そのものです。以下にその一部を引用します。

```css
:root {
  font-family: 'Neue Frutiger World', 'Verdana',  'Hiragino Sans', sans-serif;
  font-weight: 400;
  line-height: 1.7;
}
/* 中略 */
@media print {
  :root {
    widows: 3;
    orphans: 3;
    hyphens: auto;
    font-size: 75%;
  }
/* 中略 */  
}
/* 中略 */
@page {
  size: 182mm 257mm;
  margin-top: 25mm;
  margin-bottom: 33mm;
/* 中略 */
}
```

上記でフォントは優先度順に、1. `Neue Frutiger World`、2. `Verdana`、3. `ヒラギノ角ゴシック`、4. `sans-serif`と指定されています。プレビューで表示される文字は、1〜3の順番でフォントが割り当てられ、どのフォントも当該の文字を表示できない場合はブラウザ設定の「Sans Serif フォント」の指定に従います。たとえば原稿が日本語文の場合、英数字は`Neue Frutiger World`、なければ`Verdana`、仮名や漢字は`ヒラギノ角ゴシック`で表示されます。もしユーザーのPCに`ヒラギノ角ゴシック`がインストールされていなければ、ブラウザ設定の「Sans Serif フォント」が使われます。

一方、PDF出力においては、英数字は`Verdana`、仮名と漢字は`Noto Serif CJK JP`に置き換えられます。こうした結果、プレビューとPDF出力とでページのズレが発生する場合があることにご注意ください。

詳細は下記をご参照ください。

- [vivliostyle公式themeのフォント利用](/ja/create-and-save-documents/how-to-specify-fonts.md#vivliostyle公式themeのフォント利用)
- [クラウドにインストールされているフォント一覧](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウドにインストールされているフォント一覧)
- [クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)

## Academic theme

横組でページサイズは210×297mm（A4判タテ）、自動で章・節番号がつき、[脚注の記法](https://vivliostyle.org/ja/make-books-with-create-book/#%E8%84%9A%E6%B3%A8)もつかえる、理系の学生レポート向けのスタイルです。

![ ](images/functions-of-the-actions-menu/theme/fig-10.png)

これはVivliostyleが [npm package として公開](https://www.npmjs.com/package/@vivliostyle/theme-academic)している公式Theme、[@vivliostyle/theme-academic](https://vivliostyle.github.io/themes/#/ja/gallery#vivliostyletheme-academic)そのものです。以下にその一部を引用します。

```css
@page {
  size: 210mm 297mm;
  margin: 25mm 20mm 25mm 20mm;
/* 中略 */
}
html {
  font-family: 'Hiragino Mincho ProN', serif;
  font-size: 10pt;
  color: #000000;
  line-height: 1.8;
  orphans: 1;
  widows: 1;
}
```

上記でフォントは`Hiragino Mincho ProN`と`serif`が指定されています。プレビューでは`ヒラギノ明朝`が使われ、ユーザーのPCにインストールされていない場合はブラウザ設定の「Serif フォント」の設定に従います。PDF出力においては、すべて`Noto Serif CJK JP`に置き換えられます。こうした結果、プレビューとPDF出力とでページのズレが発生する場合があることにご注意ください。

フォントのしくみについて、詳細は下記をご参照ください。

- [vivliostyle公式themeのフォント利用](/ja/create-and-save-documents/how-to-specify-fonts.md#vivliostyle公式themeのフォント利用)
- [クラウドにインストールされているフォント一覧](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウドにインストールされているフォント一覧)
- [クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)