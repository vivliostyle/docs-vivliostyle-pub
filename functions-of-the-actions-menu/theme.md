# Theme (Selecting Style Information)

## Overview

![ ](images/functions-of-the-actions-menu/theme/fig-1.png)

By selecting the "Theme" item from the Action menu, you can switch to the following style information.

1. Plain theme
2. Custom theme
3. Book theme for Latin font
4. Theme for Japanese paperback
5. Slide theme
6. Techbook theme
7. Academic theme

Below, we will outline the content of each theme. The sources of the sample data used are as follows. Note that the screenshots are displayed in [Presentation Mode](/functions-of-the-actions-menu/presentation-mode.md).

- 1, 2, 4: Night on the Galactic Railroad (Kenji Miyazawa, [Aozora Bunko](https://www.aozora.gr.jp/cards/000081/card456.html))
- 3: [The Project Gutenberg eBook of Alice’s Adventures in Wonderland, by Lewis Carroll](https://www.gutenberg.org/files/11/11-h/11-h.htm)
- 5: [slide.md included with Slide theme](https://github.com/vivliostyle/themes/blob/master/packages/%40vivliostyle/theme-slide/example/slide.md)
- 6: [Is MDX, which extends Markdown, a new possibility for document creation?](https://github.com/vivliostyle/vivliostyle_doc/tree/gh-pages/vivliostyle-user-group-vol5/content/spring-raining) (spring-raining, [Included in Let's Make a Book with Vivliostyle Vol.5](https://github.com/vivliostyle/vivliostyle_doc/tree/gh-pages/vivliostyle-user-group-vol5/))
- 7: [fet.md included with Academic theme](https://github.com/vivliostyle/themes/blob/master/packages/%40vivliostyle/theme-academic/example/fet.md)

## Plain theme

A simple style using the browser's default settings. It is horizontally aligned with a font size of 12 points, and the page size is non-standard, following the window. The font used is the one specified as the "standard font" in the browser settings.

![ ](images/functions-of-the-actions-menu/theme/fig-2.png)

The Plain theme is intended for quickly checking previews and is not meant for output. If you want to output a PDF in the desired style, select one of the official Vivliostyle themes mentioned below or create your own Custom theme. Refer to the following for fonts.

- [Fonts used in Plain theme](/create-and-save-documents/how-to-specify-fonts.md#fonts-used-in-plain-theme)

## Custom theme

### How to Specify a Custom theme

To use any theme (CSS stylesheet) created by the user, follow these steps.

1. Specify the path of the theme in `vivliostyle.config.js` (red line in the screenshot)
2. Select `Action menu > Custom theme`

![ ](images/functions-of-the-actions-menu/theme/fig-3.png)

By selecting the Custom theme, you can output a PDF file with this theme applied (→ [Export](/functions-of-the-actions-menu/export.md#export)). The notation for specifying the path of the theme is as follows. Write the path in the `---` part.

```js
module.exports = {
  theme: '---',
 }
```

For more details on `vivliostyle.config.js`, please refer to the following.

- [Document Customization](/create-and-save-documents/document-customization.md)

### Specifying the Page Size

If you want to use a custom page size, specify it within the theme. The following page sizes can be specified as values for the `size` property in the `@page` rule. Note that the common B5 size in Japan is `JIS-B5` (the same applies to B4).

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

The notation is as follows. Here, A5 size is specified.

```css
@page {
   size: A5;
}
```

### Specifying Crop Marks and Bleed

Crop marks are indicators used to cut printed materials to the specified size or to align the printing positions of multiple colors. To add crop marks, specify them within the Custom theme.

<img src="images/functions-of-the-actions-menu/theme/fig-4.png" alt="Specifying Crop Marks and Bleed" style="max-height: 500px;">

Specifically, along with the aforementioned `size`, specify `crop` and `cross` as values for the `marks` property in the `@page` rule. `crop` indicates the positions of the four corners of the page, and `cross` indicates the central positions of the top, bottom, left, and right. Usually, both are specified.

Additionally, if you want to place colors or illustrations up to the edge of the page (i.e., print to the edge of the paper), you need a bleed area outside the specified page size. This is called "bleed" and is specified with the `bleed` property in the `@page` rule. The width of the area is specified as a value, with the default being 6pt (about 2.1mm). In the Japanese printing industry, 3mm is common, so specify this value.

```css
@page {
   size: A5;
   marks: crop cross;
   bleed: 3mm;
}
```

For more details, please refer to the following.

- [Introduction to CSS Typesetting with Vivliostyle Viewer > Adding Crop Marks](https://vivliostyle.github.io/vivliostyle_doc/vivliostyle-user-group-vol1/shinyu/index.html#%E3%83%88%E3%83%B3%E3%83%9C%E3%82%92%E3%81%A4%E3%81%91%E3%82%8B%E3%81%AB%E3%81%AF)

### Matching Fonts in Preview and PDF Output

In Vivliostyle Pub, the typesetting engine is located in different places for preview and PDF output. Therefore, even if you create a Custom theme, the fonts may not be displayed/output as you imagined, and the pages may be misaligned between the preview and PDF. It is recommended to refer to the following articles in advance to create a Custom theme that matches the fonts in the preview and PDF output.

- [How to Specify Fonts](/create-and-save-documents/how-to-specify-fonts.md)
- [List of Fonts Installed in the Cloud](/create-and-save-documents/additional-information-on-fonts.md#list-of-fonts-installed-in-the-cloud)
- [Substitute Font Rules in Vivliostyle CLI on the Cloud](/create-and-save-documents/additional-information-on-fonts.md#substitute-font-rules-in-vivliostyle-cli-on-the-cloud)

### Using Official Vivliostyle Themes as Templates

If you are unsure about writing a Custom theme from scratch, it is recommended to use the official Vivliostyle themes as templates and customize them to your liking. The official Vivliostyle theme repository contains each theme in the [package directory](https://github.com/vivliostyle/themes/tree/master/packages/%40vivliostyle). Follow these steps:

1. Find and download the `theme_common.css` file of the official theme that is closest to your image.
2. Upload it to your repository using Vivliostyle Pub (→ [Uploading Files](/file-and-folder-operations/file-list-pane-operations.md))
3. Customize it in the Vivliostyle Pub editor.
4. Open `vivliostyle.config.js` in the editor and specify the path of the Custom theme (refer to this section).
5. Select `Action menu > Custom theme` (refer to this section).

## Book theme for Latin font

A theme (CSS stylesheet) for books with Latin characters, such as English. It is horizontally aligned with a font size of `small` (slightly smaller than the default 16px), and the page size is non-standard, following the window size.

![ ](images/functions-of-the-actions-menu/theme/fig-5.png)

This is the official theme [@vivliostyle/theme-gutenberg](https://vivliostyle.github.io/themes/#/gallery#vivliostyletheme-gutenberg) published by Vivliostyle as an [npm package](https://www.npmjs.com/package/@vivliostyle/theme-gutenberg). Below is an excerpt.

```css
html {
  max-width: 90ch;
  margin: auto;
  font-family: Georgia, serif;
}
/* omitted */
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

In the above, the fonts `Georgia` and `serif` are specified. Most PCs should have `Georgia` installed. On the other hand, the cloud used for PDF output in Vivliostyle Pub (Figure 2 above) also has `Georgia` installed, so in most cases, the fonts in the preview and PDF output will match with this theme. However, please note that there may be discrepancies due to font version mismatches (the cloud fonts are relatively old versions).

For more details, please refer to the following.

- [Fonts used in Official Vivliostyle Themes](/create-and-save-documents/how-to-specify-fonts.md#fonts-used-in-official-vivliostyle-themes)
- [List of Fonts Installed in the Cloud](/create-and-save-documents/additional-information-on-fonts.md#list-of-fonts-installed-in-the-cloud)

## Theme for Japanese paperback

A vertically aligned theme with a font size of 8.5 points, a page size of 148×210mm (A5 portrait), supporting tate-chu-yoko (horizontal text in vertical writing) and headers, suitable for long reading materials. Note that the theme name "文庫" means reading material and is different from the bunkoban (B6 size).

![ ](images/functions-of-the-actions-menu/theme/fig-6.png)

This is the official theme [@vivliostyle/theme-bunko](https://vivliostyle.github.io/themes/#/gallery#vivliostyletheme-bunko) published by Vivliostyle as an [npm package](https://www.npmjs.com/package/@vivliostyle/theme-bunko). Below is an excerpt.

```css
html {
  writing-mode: vertical-rl;
  orphans: 1;
  widows: 1;
}
/* omitted */
@page {
  size: 148mm 210mm;
  width: 360pt;
  height: 468pt;
  margin: auto;
  font-size: 8.5pt;
  font-family: "Yu Mincho", serif;
}
```

In the above, the font `Yu Mincho` is specified. It is pre-installed on both Windows (`Yu Mincho`) and Mac (`Yu Mincho`), so it will be used in the preview (although the weight is slightly different between Windows and Mac).

On the other hand, in PDF output, it is replaced with `Noto Serif CJK JP`. As a result, there will be discrepancies between the preview and PDF output (for example, in the screenshot below, it is shifted by 3 lines compared to the preview). For more details, please refer to the following.

![ ](images/functions-of-the-actions-menu/theme/fig-7.png)

- [Fonts used in Official Vivliostyle Themes](/create-and-save-documents/how-to-specify-fonts.md#fonts-used-in-official-vivliostyle-themes)
- [Substitute Font Rules in Vivliostyle CLI on the Cloud](/create-and-save-documents/additional-information-on-fonts.md#substitute-font-rules-in-vivliostyle-cli-on-the-cloud)

## Slide theme

A horizontally aligned theme with a font size of 24 points (150% of the default), a page size of 210×148mm (A5 landscape), suitable for slide presentations.

![ ](images/functions-of-the-actions-menu/theme/fig-8.png)

This is the official theme [@vivliostyle/theme-slide](https://vivliostyle.github.io/themes/#/gallery#vivliostyletheme-slide) published by Vivliostyle as an [npm package](https://www.npmjs.com/package/@vivliostyle/theme-slide). Below is an excerpt.

```css
html {
  font-family: 'Noto', 'Yu Gothic', 'Meiryo', sans-serif;
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
  /* omitted */
}
```

In the above, the fonts are specified in order of priority: 1. `Noto Sans CJK JP`, 2. `Yu Gothic`, 3. `Meiryo`, 4. `sans-serif`. In the preview, if the user's PC does not have fonts 1-3 installed, it will follow the browser's "Sans Serif Font" setting. On the other hand, in PDF output, all fonts are replaced with `Noto Sans CJK JP`.

If you are concerned about discrepancies between the preview and PDF output, installing [`Noto Sans CJK JP`](https://fonts.google.com/noto/specimen/Noto+Serif+JP) on the user's PC may improve the situation.

For more details, please refer to the following.

- [Fonts used in Official Vivliostyle Themes](/create-and-save-documents/how-to-specify-fonts.md#fonts-used-in-official-vivliostyle-themes)
- [Matching Fonts in Preview and PDF Output](/create-and-save-documents/how-to-specify-fonts.md#custom-theme/matching-fonts-in-preview-and-pdf-output)
- [Substitute Font Rules in Vivliostyle CLI on the Cloud](/create-and-save-documents/additional-information-on-fonts.md#substitute-font-rules-in-vivliostyle-cli-on-the-cloud)

If you want to preview in single-page mode instead of spread mode, open the settings menu accessible from the Vivliostyle logo and select the "Single page" radio button under "Page Spread View".

![ ](images/functions-of-the-actions-menu/theme/fig-9.png)

## Techbook theme

A horizontally aligned theme with a font size of 12 points, a page size of 182×257mm (B5 portrait), supporting class specifications for code blocks and [footnote notation](https://vivliostyle.org/make-books-with-create-book/#%E8%84%9A%E6%B3%A8), suitable for technical books.

![ ](images/functions-of-the-actions-menu/theme/fig-10.png)

This is the official theme [@vivliostyle/theme-techbook](https://vivliostyle.github.io/themes/#/gallery#vivliostyletheme-techbook) published by Vivliostyle as an [npm package](https://www.npmjs.com/package/@vivliostyle/theme-techbook). Below is an excerpt.

```css
:root {
  font-family: 'Neue Frutiger World', 'Verdana', 'Hiragino Sans', sans-serif;
  font-weight: 400;
  line-height: 1.7;
}
/* omitted */
@media print {
  :root {
    widows: 3;
    orphans: 3;
    hyphens: auto;
    font-size: 75%;
  }
/* omitted */
}
/* omitted */
@page {
  size: 182mm 257mm;
  margin-top: 25mm;
  margin-bottom: 33mm;
/* omitted */
}
```

In the above, the fonts are specified in order of priority: 1. `Neue Frutiger World`, 2. `Verdana`, 3. `Hiragino Sans`, 4. `sans-serif`. The text displayed in the preview is assigned fonts in the order of 1-3, and if none of the fonts can display the text, it follows the browser's "Sans Serif Font" setting. For example, in the case of Japanese text, alphanumeric characters are displayed in `Neue Frutiger World`, if not available, then `Verdana`, and kana and kanji are displayed in `Hiragino Sans`. If `Hiragino Sans` is not installed on the user's PC, the browser's "Sans Serif Font" setting is used.

On the other hand, in PDF output, alphanumeric characters are replaced with `Verdana`, and kana and kanji are replaced with `Noto Sans CJK JP`. As a result, there may be discrepancies between the preview and PDF output.

For more details, please refer to the following.

- [Fonts used in Official Vivliostyle Themes](/create-and-save-documents/how-to-specify-fonts.md#fonts-used-in-official-vivliostyle-themes)
- [List of Fonts Installed in the Cloud](/create-and-save-documents/additional-information-on-fonts.md#list-of-fonts-installed-in-the-cloud)
- [Substitute Font Rules in Vivliostyle CLI on the Cloud](/create-and-save-documents/additional-information-on-fonts.md#substitute-font-rules-in-vivliostyle-cli-on-the-cloud)

## Academic theme

A horizontally aligned theme with a page size of 210×297mm (A4 portrait), automatically numbering chapters and sections, and supporting [footnote notation](https://vivliostyle.org/make-books-with-create-book/#%E8%84%9A%E6%B3%A8), suitable for scientific student reports.

![ ](images/functions-of-the-actions-menu/theme/fig-11.png)

This is the official theme [@vivliostyle/theme-academic](https://vivliostyle.github.io/themes/#/gallery#vivliostyletheme-academic) published by Vivliostyle as an [npm package](https://www.npmjs.com/package/@vivliostyle/theme-academic). Below is an excerpt.

```css
@page {
  size: 210mm 297mm;
  margin: 25mm 20mm 25mm 20mm;
/* omitted */
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

In the above, the fonts `Hiragino Mincho ProN` and `serif` are specified. If `Hiragino Mincho ProN` is installed on the user's PC, it will be used in the preview. If not installed, it follows the browser's "Serif Font" setting.

On the other hand, in PDF output, all fonts are replaced with `Noto Serif CJK JP`. As a result, there may be discrepancies between the preview and PDF output. For more details on the font mechanism, please refer to the following.

- [Fonts used in Official Vivliostyle Themes](/create-and-save-documents/how-to-specify-fonts.md#fonts-used-in-official-vivliostyle-themes)
- [List of Fonts Installed in the Cloud](/create-and-save-documents/additional-information-on-fonts.md#list-of-fonts-installed-in-the-cloud)
- [Substitute Font Rules in Vivliostyle CLI on the Cloud](/create-and-save-documents/additional-information-on-fonts.md#substitute-font-rules-in-vivliostyle-cli-on-the-cloud)