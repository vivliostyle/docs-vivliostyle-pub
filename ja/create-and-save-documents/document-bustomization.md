# 文書のカスタマイズ

`vivliostyle.config.js` を編集することで、次のようなカスタマイズが可能になります。

## 書名の指定

以下のように `title` を指定すると書名となります (値をシングルクォートで括る。以下同じ)。

```js
title: 'mybook',
```

## 著者名とメールアドレスの指定

インストール時に `author name`  で入力した著者名がデフォルトになりますが、以下のように指定すると、それが優先されます。

```js
author: 'yamada <yamadataro@example.com>',
```

## 使用する言語の指定

`language` のコメントアウト (スラッシュ部分) を削除すると、本で使用する言語を指定できます。デフォルトの英語は  `en`、日本語は `ja`。その他、 [ISO 639-1](https://www.loc.gov/standards/iso639-2/php/code_list.php )に規定された2文字コードが指定できます。

```js
// language: 'ja',
```
↓
```js
language: 'ja',
```

## 判型の指定

`size`のコメントアウトを削除すると判型を指定できます。[CSS Paged Media Module Level 3 (7.1. Page size)](https://drafts.csswg.org/css-page-3/#page-size-prop )に規定された下記の値が指定できます。なお、日本での一般的なB5は `JIS-B5` ですのでご注意ください (B4も同様)。

- `A5`
- `A4` (デフォルト)
- `A3`
- `B5`
- `B4`
- `JIS-B5`
- `JIS-B4`
- `letter`
- `legal`
- `ledger`

```js
// size: 'A4',
```
↓
```js
size: 'JIS-B5',
```
