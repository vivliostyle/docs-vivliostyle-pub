# 文書のカスタマイズ

文書全体の設定ファイルが`vivliostyle.config.js`です。 pathはリポジトリのルートです

![](/images/create-and-save-documents/document-customization/fig-1.png)

もちろんVivliostyle Pubを使って編集でき、保存すると文書全体に反映されます。記法は下記`{ }` の内部に次項のような値を記入していくことで、文書のカスタマイズができます

```js
module.exports = {

}
```

## 書名の指定

 `title` で書名を指定できます（値をシングルクォートで括る。以下同じ）

```js
title: '私の本',
```

## 著者名とメールアドレスの指定

 `author`  で著者名を指定できます

```js
author: '尾久綿次郎 <ogwata@example.com>',
```

## 使用言語の指定

`language`で文書で使用する言語を指定できます。英語は  `en`、日本語は `ja`、その他 [ISO 639-1](https://www.loc.gov/standards/iso639-2/php/code_list.php )に規定された2文字コードが指定できます

```js
language: 'ja',
```

## 判型の指定

`size`で判型を指定できます

```js
size: 'JIS-B5',
```

[CSS Paged Media Module Level 3 (7.1. Page size)](https://drafts.csswg.org/css-page-3/#page-size-prop )に規定された下記の値が指定できます。なお、日本での一般的なB5は `JIS-B5` ですのでご注意ください (B4も同様)

- `A5`
- `A4`
- `A3`
- `B5`
- `B4`
- `JIS-B5`
- `JIS-B4`
- `letter`
- `legal`
- `ledger`

## テーマの指定

 `theme` で任意のスタイルシート（Custom theme）を指定できます

```js
theme: 'css/style.css',
```

Custom themeについては、下記もご参照ください

- [Custom theme](/ja/functions-of-the-actions-menu/theme.md#custom-theme)
- [Custom theme／プレビューとPDF出力とでフォントを一致させる](/ja/create-and-save-documents/how-to-specify-fonts.md#custom-theme／プレビューとpdf出力とでフォントを一致させる)

## 複数文書の出力

`entry` で下記のように指定することで、複数のmarkdownファイルをまとめて1冊の本として出力できます

```js
entry: [
    "Chapter-1.md",
    "Chapter-2.md",
    "Chapter-3.md",
],
```

出力したくないファイルがあれば、行頭に`//`を記入すればコメントアウトになります

## 目次の追加

以下の手順で目次を追加することができます

1. あらかじめ以下のような目次用の markdown ファイルを用意し、ファイル名を `index.md` としてアップロードします（→[ファイルのアップロード](/ja/file-and-folder-operations/file-list-pane-operations.md#ファイルのアップロード)）。他と違って以下はHTML構文なので、指定するのもHTMLファイルであることにご注意ください

```md
# 本のタイトル

<nav id="toc" role="doc-toc">

## 目次

- [記事タイトル1](Chapter-1.html)
- [記事タイトル2](Chapter-2.html)
- [記事タイトル3](Chapter-3.html)

</nav>
```

なお、HTMLのタグがある行とmarkdownの行の間は、必ず空行をいれるよう注意してください。そうしないとエラーになります

2. `vivliostyle.config.js` の `entry` の先頭行に、用意した `index.md` を指定します

```js
entry: [
    "index.md",
    "Chapter-1.md",
    "Chapter-2.md",
    "Chapter-3.md",
],
```

## 奥付の追加

以下の手順で奥付を追加することができます

1. あらかじめ以下のような markdownファイルを用意し、ファイル名を `colophon.md` としてアップロードします（→[ファイルのアップロード](/ja/file-and-folder-operations/file-list-pane-operations.md#ファイルのアップロード)）

```md
<section id="colophon" role="doc-colophon">

## 私が書いた本
20xx年x月x日　初版発行
- 発行　私が書いた本刊行会
- 著者　尾久綿次郎
- 印刷　Sample Printing
© My Book Publishing, 20xx

</section>
```

2. `vivliostyle.config.js` の `entry` の末尾行に、用意した `colophon.md` を指定します

```js
entry: [
    "index.md",
    "Chapter-1.md",
    "Chapter-2.md",
    "Chapter-3.md",
    "colophon.md",
],
```
