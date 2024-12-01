# How to Specify Fonts

## Mechanism of Using Fonts

Fonts are specified within the theme (→[Theme (Selecting Style Information)](/functions-of-the-actions-menu/theme.md)). The typesetting engine Vivliostyle.js operates fonts according to the theme and performs layout and typesetting. Figure 1 below illustrates the mechanism of the preview.

<img src="images/create-and-save-documents/how-to-specify-fonts/fig-1.jpg" alt="Figure 1: Using Fonts in Preview" style="max-height: 500px;">

It is important to note that the typesetting for the preview performed by Vivliostyle.js (red square) is on the user's PC frontend. Therefore, **Font 1** on the same user's PC as Vivliostyle.js and **Font 3** from the web font service can be used in the preview.

Next, Figure 2 illustrates the mechanism of PDF output. The typesetting for PDF output performed by Vivliostyle.js (red square) is on the cloud backend.

<img src="images/create-and-save-documents/how-to-specify-fonts/fig-2.jpg" alt="Figure 2: Using Fonts in PDF Output" style="max-height: 500px;">

Therefore, **Font 2** installed in the cloud and **Font 3** from the web font service can be used for PDF output.

Let's summarize the explanation so far. Preview and PDF output are handled by separate typesetting engines, Vivliostyle.js (red squares in Figures 1 and 2). Each typesetting engine uses fonts from the following three locations:

- Local fonts on the user's PC (Figure 1: **Font 1**)
- Fonts installed in the cloud (Figure 2: **Font 2**)
- Fonts from the web font service (Figures 1 and 2: **Font 3**)

The Vivliostyle.js on the user's PC for preview uses local fonts (Figure 1: **Font 1**) and web font service fonts (Figures 1 and 2: **Font 3**).

On the other hand, the Vivliostyle.js on the cloud for PDF output uses fonts installed in the cloud (Figure 2: **Font 2**) and web font service fonts (Figures 1 and 2: **Font 3**).

Due to this mechanism, the only fonts that always match between preview and PDF output are the web font service fonts (Figures 1 and 2: **Font 3**). Local fonts installed on the user's PC (Figure 1: **Font 1**) cannot be used for PDF output, and fonts installed in the cloud (Figure 2: **Font 2**) cannot be used for preview.

For example, if the local font used in the preview (Figure 1: **Font 1**) is not available in the cloud, it will be replaced with a similar font from the fonts installed in the cloud for PDF output (→[Substitute Font Rules in Vivliostyle CLI on the Cloud](/create-and-save-documents/additional-information-on-fonts.md#substitute-font-rules-in-vivliostyle-cli-on-the-cloud)). As a result, the fonts between preview and PDF output will not match, causing page misalignment.

In this section, we will explain how to use the three types of fonts along with the items in the Action menu. We will also touch on how to match the fonts between preview and PDF output.

## Fonts Used in the Plain Theme

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-3.png)

The Plain theme is for quickly checking the preview with minimal effort. Unlike others, it does not have a specific theme (style information) but follows the browser's default settings. For example, the font refers to the "standard font" set in the browser. This corresponds to **Font 1** (local fonts on the user's PC) in Figure 1.

The purpose of this theme is not for output. PDF output is possible, but the browser's default settings used in the Plain theme will be replaced according to the [Substitute Font Rules in Vivliostyle CLI on the Cloud](/create-and-save-documents/additional-information-on-fonts.md#substitute-font-rules-in-vivliostyle-cli-on-the-cloud). If you want to preview or output PDF with the intended style, choose from the official Vivliostyle themes described later or create a Custom theme.

For more information on the Plain theme, please refer to the following:

- [Theme (Selecting Style Information) > Plain Theme](/functions-of-the-actions-menu/theme.md#plain-theme)

## Fonts Used in Official Vivliostyle Themes

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-4.png)

When selecting the following themes from the Action menu, the official Vivliostyle themes on the npm package management system will be used. For details on each theme, refer to the links.

- [Book theme for Latin font](/functions-of-the-actions-menu/theme.md#book-theme-for-latin-font)
- [Theme for paperback books](/functions-of-the-actions-menu/theme.md#theme-for-paperback-books)
- [Slide theme](/functions-of-the-actions-menu/theme.md#slide-theme)
- [Techbook (Technical Doujinshi) theme](/functions-of-the-actions-menu/theme.md#techbook-technical-doujinshi-theme)
- [Academic theme](/functions-of-the-actions-menu/theme.md#academic-theme)

In the preview, these themes use local fonts on the user's PC (Figure 1: **Font 1**). Therefore, the fonts specified in the theme need to be installed on the user's PC. If those fonts are not installed, they will be substituted with `sans-serif` or `serif` according to the `font-family:` setting.

For PDF output, fonts installed in the cloud (Figure 2: **Font 2**) are used. If the fonts specified in the official theme are not available in the cloud, they will be replaced according to the [Substitute Font Rules in Vivliostyle CLI on the Cloud](/create-and-save-documents/additional-information-on-fonts.md#substitute-font-rules-in-vivliostyle-cli-on-the-cloud). For details on the fonts specified in each official theme and the fonts installed in the cloud, refer to the following:

- [Theme (Selecting Style Information)](/functions-of-the-actions-menu/theme.md)
- [List of Fonts Installed in the Cloud](/create-and-save-documents/additional-information-on-fonts.md#list-of-fonts-installed-in-the-cloud)

Please note that if fonts are substituted due to these replacement processes, the pages may misalign between the preview and PDF.

## Custom Theme / Matching Fonts Between Preview and PDF Output

By creating a Custom theme, you can perform preview and PDF output based on it. In this case, the local fonts on the user's PC (Figure 1: **Font 1**) are used for the preview, and the fonts installed in the cloud (Figure 2: **Font 2**) are used for PDF output.

The problem arises when the font specified in the Custom theme is only installed on the user's PC or the cloud. In such cases, a similar font will be used as a substitute, causing font mismatches between the preview and PDF output, leading to page misalignment.

However, if you install the fonts available in the cloud on your PC and specify them in the Custom theme, you can match the fonts between the preview and PDF output, preventing page misalignment. So, which fonts installed in the cloud should you install on your PC?

Vivliostyle Pub has installed all [Noto fonts](https://fonts.google.com/noto), which support a wide range of languages and scripts with rich weights and styles, in the cloud. The most efficient and effective way is to install the Japanese Gothic font [`Noto Sans CJK JP`](https://github.com/googlefonts/noto-cjk/tree/main/Sans) and the Japanese Mincho font [`Noto Serif CJK JP`](https://github.com/googlefonts/noto-cjk/tree/main/Serif) on your PC. Below, we will explain how to use `Noto Sans CJK JP` for preview and PDF output.

------------------------

1. Install `Noto Sans CJK JP` on your PC in advance.

2. Upload a stylesheet (Custom theme) with the following content to Vivliostyle Pub (→[File Upload](/file-and-folder-operations/file-list-pane-operations.md)). If you already have one, rewrite it with the following as a reference.

```css
@charset "UTF-8";

html {
  writing-mode: vertical-rl;
  font-family: 'Noto Sans CJK JP', sans-serif;
  font-style: normal;
  text-align: justify;
  text-spacing: space-first allow-end ideograph-alpha ideograph-numeric;
  line-height: 2;
  orphans: 1;
  widows: 1;
}

p {
  font-weight: 300;
  margin: 0;
  text-indent: 1em;
  hanging-punctuation: first allow-end;
}
h1 {
  font-weight: 900;
}
h2 {
  font-weight: 700; 
}

@page {
  size: 148mm 210mm;
  width: 360pt;
  height: 468pt;
  margin: auto;
  font-size: 8.5pt;
}
@page :left {
  @top-left {
    writing-mode: horizontal-tb;  
    content: counter(page) "　" env(doc-title);
    margin-left: 7pt;
    margin-top: 8.5mm;
  }
}
@page :right {
  @top-right {
    writing-mode: horizontal-tb;
    content: counter(page);
    margin-right: 7pt;
    margin-top: 8.5mm;
   }
}
```

The above is an example of a Custom theme. The root element specifies `Noto Sans CJK JP` as the `font-family`, with `font-weight: 300;` for the body text (`p`), `font-weight: 900;` for the main heading (`h1`), and `font-weight: 700;` for the subheading (`h2`), specifying different weights with the same design. The page settings (`@page`) specify A5 portrait size, width 360pt, height 468pt, and font size 8.5pt.

3. In the configuration file `vivliostyle.config.js`, specify the path to the Custom theme (→[Custom theme](/functions-of-the-actions-menu/theme.md#custom-theme)). Describe the file name to be output as PDF in `entry:`.

```js
module.exports = {
  title: 'My Book',
  author: 'Jiro Ogumawata',
  theme: 'css/style.css',
  entry: [
    'chapter-2.md',
    ]
}
```

For more details on `vivliostyle.config.js`, refer to the following:

- [Document Customization](/create-and-save-documents/document-customization.md)

4. Select "Custom theme" from the Action menu. If the theme does not switch, reload the browser.

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-5.png)

5. `Noto Sans CJK JP` is now used in the preview.

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-6.png)

6. Select [Export > PDF](/functions-of-the-actions-menu/export.md#pdf) from the Action menu to output a PDF with the Custom theme applied. Confirm that the same `Noto Sans CJK JP` is used with the same font size, line length, and line spacing as in the preview.

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-7.png)

For more details on Custom themes, refer to the following:

- [Custom theme](/functions-of-the-actions-menu/theme.md#custom-theme)

- **Supplementary Information**
    - Noto fonts have a wide variety of variations, and it may be difficult to find the desired font. It is recommended to download the **"Variable OTC"** link in the repository below.
        - [`Noto Sans CJK JP`](https://github.com/googlefonts/noto-cjk/tree/main/Sans)
        - [`Noto Serif CJK JP`](https://github.com/googlefonts/noto-cjk/tree/main/Serif)
    - There are two links: "OTC" (54.3MB) and "TTF" (57.1MB). Both are in a format called "font collection," which contains multiple font files in a single font package. When used in Vivliostyle Pub, either "OTC" or "TTF" can be used.
    - By installing the "Variable OTC," fonts for five languages (Japanese (JP), Traditional Chinese (TC), Simplified Chinese (SC), Hong Kong (HK), Korean (KR)) will be installed.
    - In addition to the method explained in this section, you can also match the fonts between preview and PDF output by using a web font service (Figures 1 and 2: **Font 3**) (refer to the following sections).

## Custom Theme / Using Google Fonts

By using web fonts (Figures 1 and 2: **Font 3**), you can match the fonts between preview and PDF output. This section explains how to use the free web font service [Google Fonts](https://fonts.google.com/) with Vivliostyle Pub.

1. First, select a font on [Google Fonts](https://fonts.google.com/), then click the (+) next to "Select this style" in Styles to choose the desired weight. Here, we selected Shippori Mincho Regular 400, Noto Sans Japanese Bold 700, and Noto Sans Japanese Medium 900.

The loading code for the selected font/style will be displayed in the right pane of the screen, so copy it. Also, copy the `font-family` code from "CSS rules to specify families."

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-8.png)

2. Upload a Custom theme with the Google Fonts loading code and `font-family` code as shown below (→[File Upload](/file-and-folder-operations/file-list-pane-operations.md)). If you already have a stylesheet (Custom theme), rewrite it with the following as a reference.

```css
@charset "UTF-8";

@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@700;900&family=Shippori+Mincho&display=swap');

html{
writing-mode: vertical-rl;
font-family: 'Shippori Mincho', serif;
font-style: normal;
text-align: justify;
text-spacing: space-first allow-end ideograph-alpha ideograph-numeric;
line-height: 2;
}

p {
  font-weight: 400;
  text-indent: 1em;
  hanging-punctuation: first allow-end;
}

h1 {
font-family: 'Noto Sans JP', sans-serif;  
font-weight: 900; 
}

h2 {
font-family: 'Noto Sans JP', sans-serif;
font-weight: 700; 
}

@page {
  size: 148mm 210mm;
  width: 360pt;
  height: 468pt;
  margin: auto;
  font-size: 8.5pt;
}
@page :left {
  @top-left {
    writing-mode: horizontal-tb;  
    content: counter(page) "　" env(doc-title);
    margin-left: 7pt;
    margin-top: 8.5mm;
  }
}
@page :right {
  @top-right {
    writing-mode: horizontal-tb;
    content: counter(page);
    margin-right: 7pt;
    margin-top: 8.5mm;
   }
}
```

Google Fonts provides two types of loading codes: `link` element and `@import`. Both load external stylesheets and function the same. Here, we prioritize the benefit of applying web fonts to multiple Markdown files and paste the `@import` loading code into the stylesheet (Custom theme) (remove the `style` elements used for HTML files).

Then, paste the specific font name specified in the `font-family` code into the Custom theme. Here, we specified Shippori Mincho Regular 400 for the root element, Noto Sans Japanese Bold 900 for `h1`, and Noto Sans Japanese Medium 700 for `h2`.

3. In the configuration file `vivliostyle.config.js`, specify the path to the Custom theme (→[Custom theme](/functions-of-the-actions-menu/theme.md#custom-theme)). Describe the file name to be output as PDF in `entry:`.

```js
module.exports = {
  title: 'My Book',
  author: 'Jiro Ogumawata',
  theme: 'css/style.css',
  entry: [
    'chapter-2.md',
    ]
}
```

4. Select the Custom theme from the Action menu and confirm that the web font is applied in the preview. If the theme does not switch, reload the browser.

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-9.png)

5. Select [Export > PDF](/functions-of-the-actions-menu/export.md#pdf) from the Action menu to output a PDF with the web font applied. Confirm that the same font is used with the same font size, line length, and line spacing as in the preview.

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-10.png)

- **Supplementary Information**
    - In this article, we pasted the `@import` code into the stylesheet (Custom theme) to apply web fonts to multiple Markdown files. If you want to apply web fonts to specific Markdown files only, paste the loading code (`link` element or `@import` wrapped in `style` elements) at the beginning of the file. Be sure to specify the `font-family` in the stylesheet.
    - [bunny.net](https://fonts.bunny.net/) offers the same fonts as Google Fonts for free.
        - This service maintains compatibility with Google Fonts (i.e., hosting the same fonts) and explicitly states that it does not track users to comply with the EU's [GDPR (General Data Protection Regulation)](https://www.jetro.go.jp/world/europe/eu/gdpr/) (→[bunny.net > about](https://fonts.bunny.net/about)).
        - It is easy to use; simply replace the `googleapis.com` part of the loading code obtained from Google Fonts with `bunny.net`.
        - Alternatively, select a font on [bunny.net](https://fonts.bunny.net/), click "Font+" in the upper right corner of the screen to obtain the loading code, and paste it into the stylesheet (Custom theme) or Markdown file.

## Custom Theme / Using Paid Web Font Services

Google Fonts has the advantage of being free, but the disadvantage is that the loading speed may be slightly slower. While it may not be a problem for short texts, the slowness may be noticeable for very long manuscripts. In such cases, consider using a paid web font service. This section explains how to use [DynaSmart V](https://www.dynacw.co.jp/product/product_dynasmart_detail.aspx?sid=25) by DynaComware with Vivliostyle Pub. The following assumes that you have already obtained an account with the company.

1. Register the domain name `vivliostyle-pub-develop.vercel.app` of Vivliostyle Pub from the DynaFont Online My Page, and then obtain the JavaScript code (script element) and `font-family` for the desired font. The following page may be helpful for details:

    - [DFO JavaScript Generator (DynaComware)](https://dfo.dynacw.co.jp/service/JS_Gen.aspx)

Here, we will use DF Kaku Mincho StdN W3 OpenType as the body text font, DF King Gothic Pro-6N Semibold OpenType for `h1`, and DF King Gothic Pro-6N Ultrabold OpenType for `h2`.

2. Paste the obtained JavaScript code at the beginning of the Markdown file (the font has not changed at this stage).

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-11.png)

3. Upload a Custom theme with the obtained `font-family` as shown below (→[File Upload](/file-and-folder-operations/file-list-pane-operations.md)). If you already have a Custom theme, rewrite it with the following as a reference.

```css
@charset "UTF-8";

html{
writing-mode: vertical-rl;
font-family: 'DFMinchoPPro6N-W3', serif;
font-style: normal;
text-align: justify;
text-spacing: space-first allow-end ideograph-alpha ideograph-numeric;
line-height: 2;
}

p {
  font-weight: 400;
  text-indent: 1em;
  hanging-punctuation: first allow-end;
}

h1 {
font-family: 'DFKingGothicJP16N-Ultrabold', sans-serif; 
}

h2 {
font-family: 'DFKingGothicJP16N-Semibold', sans-serif; 
}

@page {
  size: 148mm 210mm;
  width: 360pt;
  height: 468pt;
  margin: auto;
  font-size: 8.5pt;
}
@page :left {
  @top-left {
    writing-mode: horizontal-tb;  
    content: counter(page) "　" env(doc-title);
    margin-left: 7pt;
    margin-top: 8.5mm;
  }
}
@page :right {
  @top-right {
    writing-mode: horizontal-tb;
    content: counter(page);
    margin-right: 7pt;
    margin-top: 8.5mm;
   }
}
```

4. In the configuration file `vivliostyle.config.js`, specify the path to the Custom theme (→[Custom theme](/functions-of-the-actions-menu/theme.md#custom-theme)). Describe the file name to be output as PDF in `entry:`.

```js
module.exports = {
  title: 'My Book',
  author: 'Jiro Ogumawata',
  theme: 'css/style.css',
  entry: [
    'chapter-2.md',
    ]
}
```

5. Select "Custom theme" from the Action menu. If the theme does not switch, reload the browser.

6. DF Kaku Mincho and DF King Gothic are now used in the preview.

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-12.png)

7. Select [Export > PDF](/functions-of-the-actions-menu/export.md#pdf) from the Action menu to output a PDF with the Custom theme applied. Confirm that the same DF Kaku Mincho and DF King Gothic are used with the same font size, line length, and line spacing as in the preview.

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-13.png)

- **Supplementary Information**
    - The fast loading speed of paid web font services is due to the **dynamic subsetting** method. This technology is effective for East Asian language web fonts with a large number of characters.
    - Large font files are not suitable for web fonts that depend on the network. Therefore, before rendering, the content is parsed, and a small subset font containing only the characters in the content is created and sent to the web server for rendering. Since the subset content is always different, it is called dynamic subsetting.
    - In contrast, Google Fonts uses **static subsetting**. This method divides the font into small subsets based on usage frequency, regardless of the content. When a character is requested from the web server, the subset font containing that character is sent for rendering. The subset content is fixed, so it is called static subsetting. Compared to the former, it tends to be less efficient, and the loading speed is slower.
    - While paid web font services are convenient, it is important to note that their usage may be restricted by terms of use. These services cannot be used unconditionally with Vivliostyle Pub.
    - To ensure that paid web font services can be used safely with Vivliostyle Pub, we have selected recommended uses for each service. Please refer to the following:
       - [Recommended Uses for Paid Web Font Services](/create-and-save-documents/additional-information-on-fonts.md#recommended-uses-for-paid-web-font-services)
