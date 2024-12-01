# Export

## PDF

Selecting "Export > PDF" from the Action menu will output a PDF. The output file is processed based on the contents of `vivliostyle.config.js`, regardless of the preview. Therefore, if there is no `vivliostyle.config.js`, the PDF will not be output. When outputting a PDF for the first time, create `vivliostyle.config.js` in the root and specify the file name to be output, referring to the following.

- [Document Customization](/create-and-save-documents/document-customization.md)

For related information, please refer to the following.

- [How to Specify Fonts > Mechanism to Use Fonts](/create-and-save-documents/how-to-specify-fonts.md#mechanism-to-use-fonts)
- [Theme > Custom theme](/functions-of-the-actions-menu/theme.md#custom-theme)

If you want to output only specific Markdown files among multiple files, specify only the files to be output in `vivliostyle.config.js` or comment out the files not to be output. For details, please refer to the following.

- [Document Customization > Specifying Target Documents](/create-and-save-documents/document-customization.md#specifying-target-documents)

1. Select "Action Menu > PDF"

![](images/functions-of-the-actions-menu/export/fig-1.png)

2. A message "Build started" will be displayed at the bottom of the screen

![](images/functions-of-the-actions-menu/export/fig-2.png)

3. After a while, a message "Click the link below to view the PDF" will be displayed. Click the "View PDF" part

![](images/functions-of-the-actions-menu/export/fig-3.png)

This display will disappear after a certain period. If you want to check again, you can check the "View PDF" link from the log display

- [Quick Start Guide > Log Display](/readme-first/quick-start-guide-and-required-environment.md#displaying-logs)

4. The browser will transition to the PDF viewing screen. Click the downward arrow "↓" (red circle) at the top left of the window to open the file dialog and download the PDF

![](images/functions-of-the-actions-menu/export/fig-4.png)

## How to Add Crop Marks

To create a PDF file with crop marks, add the following description to the custom stylesheet.

```css
@page {
  marks: crop cross;
  bleed: 3mm;
}
```

However, please note that adding the above will add crop marks not only to the output but also to the preview (although it is planned to be modified to output a PDF with crop marks from the Action menu in the future).

## Submitting to a Printing Company

There are services that can actually print and bind PDF files output by Vivliostyle Pub.

- [mybooksPOD](https://pod.mybooks.jp/)

The above is a service by [Obun Printing Co., Ltd.](https://obun.jp/), which allows users to print and bind PDF files they have created from a single copy. Users who wish to use the service should fill out the form on the above page and upload the PDF file they wish to print. A quote will be sent by return email, and if it is acceptable, place a formal order. Please note the following points when using the service.

- If there are no crop marks in the PDF file, the printing company will add them
- Since the current Vivliostyle Pub does not have a cover creation function, users will need to prepare it separately or request the printing company to create it
- For specific usage flow, please refer to the following → [Service to Print PDFs Created with Vivliostyle Pub Begins](https://vivliostyle.org/blog/2022/09/07/service-to-print-pdfs/)
- For details of this service, please contact Obun Printing Co., Ltd.

## Supplementary Information

- The following two issues have been pointed out regarding PDF output by Vivliostyle
    - [Vivliostyle CLI: There are cases where the text in the output PDF does not become K100 #276](https://github.com/vivliostyle/vivliostyle-cli/issues/276)
    - Vivliostyle.js: When outputting a PDF, the font is converted to a Type 3 font and embedded
        - [please use CID instead of Type3 #437](https://github.com/vivliostyle/vivliostyle.js/issues/437)
        - [the reversed string is returned on Preview.app when selecting PDF contents which uses Type3 #439](https://github.com/vivliostyle/vivliostyle.js/issues/439)
- The issue of not becoming K100 can cause printing troubles such as misregistration and blocking in commercial printing (offset printing), which requires uniform quality for large quantities, and we are considering solutions
- However, in small-quantity doujinshi printing (toner printing), the quality required is not as high as in commercial printing, so it is not considered a major problem. For example, it is highly likely that the problem can be solved by converting the output PDF to grayscale using an external site such as the following
    - [DeftPDF (Sictec Infotech, Inc.)](https://deftpdf.com/grayscale-pdf)
- Next, the issue of being converted to a Type 3 font is generally considered unsuitable for commercial printing, and a quick resolution of this issue is desired
- However, the cause is not Vivliostyle.js but an external library (Chromium), so the solution can only be awaited by updating the relevant library
- Nevertheless, there are the following workarounds
    - Use Adobe's paid software [Adobe Acrobat Pro DC](https://www.adobe.com/jp/products/acrobat-pro-cc.html) to convert to PDF/X standard
        - [Convert from PDF to PDF/X, PDF/A, or PDF/E (Adobe)](https://helpx.adobe.com/jp/acrobat/using/pdf-x-pdf-a-pdf.html)
    - Specify TrueType fonts to avoid being converted to Type 3 fonts. For example, refer to the following list and use the free web font service, Google Fonts
        - [List of Japanese fonts in Google Fonts that do not become "Type 3" in Vivliostyle's PDF output](/create-and-save-documents/additional-information-on-fonts.md#list-of-japanese-fonts-in-google-fonts-that-do-not-become-type-3-in-vivliostyle-pdf-output)
    - Instead of using Vivliostyle Pub, use [Create Book](https://github.com/vivliostyle/create-book) and build a PDF compliant with PDF/X-1a using the `--press-ready` option of [Vivliostyle CLI](https://github.com/vivliostyle/vivliostyle-cli)
        - Note that when creating PDF/X-1a with the above option, the font is outlined and loses text attributes, making it impossible to search, etc. This option is for creating print data and is not suitable for distributing PDFs. For details, please refer to the following.
            - [Create Book > Generating PDF Files for 4-Color Printing](https://docs.vivliostyle.org/#/create-book#4%E8%89%B2%E5%8D%B0%E5%88%B7%E7%94%A8pdf%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB-%E3%81%AE%E7%94%9F%E6%88%90)
- Even if this issue is a problem in commercial printing, it may not be a major problem in small-quantity doujinshi printing
    - In our tests, a PDF (A5 size, 281 pages, 1.01GB) output from the `build` command of Vivliostyle CLI, i.e., the same environment as PDF output in Vivliostyle Pub, was printed on an on-demand printing machine [bizhub PRESS 1085 (Konica Minolta)](https://www.konicaminolta.jp/business/products/graphic/ondemand_print/color/bizhub_press_c1100_c1085/index.html)
        - This PDF has Type 3 fonts embedded, which is likely to be considered unsuitable data for normal offset printing
    - We have also successfully converted the same PDF to intermediate data from the RIP workflow [EQUIOS (SCREEN Graphic Solutions)](https://www.screen.co.jp/ga/product/category/workflow)
    - In any case, there is no guarantee that it will be printed as it appears in all cases. We recommend that you communicate well with the printing company before submitting your data
