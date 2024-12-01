# Document Customization

The configuration file for the entire document is `vivliostyle.config.js`. The path is the root of the repository.

![](/images/create-and-save-documents/document-customization/fig-1.png)

`vivliostyle.config.js` can be edited using Vivliostyle Pub itself, and once saved, the changes will be reflected in the entire document. The syntax involves filling in values inside the `{ }` as shown below.

```js
module.exports = {

}
```

## Specifying the Title

You can specify the title with `title` (enclose the value in single quotes. The same applies below).

```js
title: 'My Book',
```

## Specifying the Author Name and Email Address

You can specify the author's name with `author`.

```js
author: 'Jiro Ogwata <ogwata@example.com>',
```

## Specifying the Language

You can specify the language used in the document with `language`. English is `en`, Japanese is `ja`, and other languages can be specified with the two-letter codes defined in [ISO 639-1](https://www.loc.gov/standards/iso639-2/php/code_list.php).

```js
language: 'ja',
```

## Specifying the Format

The format should be specified in the theme, not in `vivliostyle.config.js`. For details, please refer to the following.

- [Theme (Selecting Style Information) > Custom theme > Specifying the Format](/functions-of-the-actions-menu/theme.md#specifying-the-format)

## Specifying the Target Document

You can specify the target document for processing with the syntax `entry: [ ]`. Multiple documents can be specified, and by specifying them as shown below, you can output multiple markdown files as a single book.

```js
entry: [
    "Chapter-1.md",
    "Chapter-2.md",
    "Chapter-3.md",
],
```

If there are files you do not want to output, you can comment them out by adding `//` at the beginning of the line.

## Adding a Table of Contents

You can add a table of contents by following these steps:

1. Prepare a markdown file for the table of contents as shown below, and upload it with the filename `index.md` (→[Uploading Files](/file-and-folder-operations/file-list-pane-operations.md#upload-file)). Note that the following is HTML syntax, so the file to be specified should also be an HTML file.

```md
# Book Title

<nav id="toc" role="doc-toc">

## Table of Contents

- [Article Title 1](Chapter-1.html)
- [Article Title 2](Chapter-2.html)
- [Article Title 3](Chapter-3.html)

</nav>
```

Note that there must be a blank line between lines with HTML tags and markdown lines. Otherwise, it will result in an error.

2. Specify the prepared `index.md` at the top line of `entry` in `vivliostyle.config.js`.

```js
entry: [
    "index.md",
    "Chapter-1.md",
    "Chapter-2.md",
    "Chapter-3.md",
],
```

## Adding a Colophon

You can add a colophon by following these steps:

1. Prepare a markdown file for the colophon as shown below, and upload it with the filename `colophon.md` (→[Uploading Files](/file-and-folder-operations/file-list-pane-operations.md#uploading-files)).

```md
<section id="colophon" role="doc-colophon">

## The Book I Wrote
First Edition Published on xx xx, 20xx
- Publisher: The Book I Wrote Publishing Association
- Author: Jiro Ogwata
- Printing: Sample Printing

© My Book Publishing, 20xx

</section>
```

2. Specify the prepared `colophon.md` at the last line of `entry` in `vivliostyle.config.js`.

```js
entry: [
    "index.md",
    "Chapter-1.md",
    "Chapter-2.md",
    "Chapter-3.md",
    "colophon.md",
],
```

## Summary

To summarize the explanation so far, the description of `vivliostyle.config.js` will be as follows:

```js
module.exports = {
	title: 'My Book',
	author: 'Jiro Ogwata <ogwata@example.com>',
	language: 'ja',
	theme: 'css/style.css',
	entry: [
		"index.md",
		"Chapter-1.md",
		"Chapter-2.md",
		"Chapter-3.md",
		"colophon.md",
	],
}
```

- [Action Menu Functions > Export > Additional Information](/functions-of-the-actions-menu/export.md#supplementary-information)