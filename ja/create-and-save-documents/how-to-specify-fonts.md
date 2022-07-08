# フォントの指定方法

## フォントを使用するしくみ

Vivliostyle Pubでは以下の3種類の場所にあるフォントを利用することができます。

1. ユーザーのPCにあるローカルフォント（図1：**フォント1**）
2. クラウドにインストールされたフォント（図2：**フォント2**）
3. Webフォントサービスのフォント（図1、図2：**フォント3**）

ただし、プレビューで使われるフォントとPDF出力で使われるフォントが、無条件に一致するのは上記のうち3だけです。これ以外の1、2では、互いに似たフォントが使われますが、一致しないことが多いのが実際です（一致しない場合、ページがずれる可能性があります）。これはVivliostyle PubではプレビューとPDF出力が、別々の機構によって処理されることによります。本節ではまずその仕組みを概説し、ついでActionメニューの項目に沿いながら、3種類のフォントを利用する方法について説明していきます。

では、プレビューにおいてフォントがどのように使われるかをみてみましょう（図1）。ここで注意してほしいのは、実際に組版をおこなうVivliostyle.js（赤色）は、プレビューにおいてはユーザーのPC上のフロントエンドにあるということです。組版エンジンはフォントを直接操作します。したがって同じユーザーのPCにある**フォント1**がプレビューで利用できるわけです。

ただし、この図にはバックエンドが図示されていません。プレビューではクラウド上にあるバックエンドのコンポーネントは関与しない仕組みです。したがってクラウドにインストールされた**フォント2**も利用できません。

<img src="images/create-and-save-documents/how-to-specify-fonts/fig-1.jpg" alt="図1 プレビューにおけるフォントの利用" style="max-height: 500px;">

次に、PDF出力においてフォントがどのように使われるかをみてみましょう（図2）。注意してほしいのは、PDF出力では実際に組版をおこなうVivliostyle.js（赤色）はクラウド上のバックエンドにあるということです。したがって同じクラウドにインストールされている**フォント2**がPDF出力で利用できるわけです。

<img src="images/create-and-save-documents/how-to-specify-fonts/fig-2.jpg" alt="図2 PDF出力におけるフォントの利用" style="max-height: 500px;">

ただし、上の図にはフロントエンドのVivliostyle.jsやユーザーのPCにある**フォント1**は図示されていません。PDF出力において、フロントエンドはメニューを通じて指示を出すだけで、組版には関与しない仕組みです。したがってユーザーのPCにある**フォント1**も利用できません。

一方、Webフォントサービスの**フォント3**は、図1にも図2にも図示されています。つまり、フロントエンドのVivliostyle.jsでもバックエンドにあるVivliostyle.jsでも、同じ**フォント3**を使うことができます。こうしてプレビューで使われるフォントとPDF出力で使われるフォントを一致させることができるわけです。

## Plain themeで使われるフォント

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-3.png)

Plain themeは最小の手間で素早くプレビューを確認するために用意されたテーマです。プレビューのスタイルはブラウザのデフォルト設定にしたがいます。たとえばフォントはブラウザ設定の「標準フォント」が参照されます。これは、前掲図1の分類では**フォント1**（ユーザーのPCにあるローカルフォント）に当たります。

PDF出力に際しては[クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)に従ってフォントが使用されます。ただしこのテーマの目的上、出力は想定されていません（PDF出力そのものは可能ですが、Plain themeと無関係に`vivliostyle.config.js`での設定で出力されます）。イメージ通りのスタイルでプレビューやPDF出力をしたい場合は、後述のVivliostyle公式テーマの中から選択するか、Custom themeを作成してください。

Plain themeについては、以下もご参照ください。

- [Theme（テーマの選択）> Plain theme](/ja/functions-of-the-actions-menu/theme.md#plain-theme)

## Vivliostyle公式Themeで使われるフォント

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-4.png)

Actionメニューから、以下のthemeを選択した場合、npm package管理システム上のVivliostyle公式Themeが使用されます。ぞれぞれのthemeの詳細は、リンク先を参照してください。

- [Book theme for latin font](/ja/functions-of-the-actions-menu/theme.md#book-theme-for-latin-font)
- [文庫用のテーマ](/ja/functions-of-the-actions-menu/theme.md#文庫用のテーマ)
- [Slide theme](/ja/functions-of-the-actions-menu/theme.md#slide-theme)
- [Techbook (技術同人誌) theme](/ja/functions-of-the-actions-menu/theme.md#techbook-技術同人誌-theme)
- [Academic theme](/ja/functions-of-the-actions-menu/theme.md#academic-theme) 

プレビューにおいて、これらのthemeで使用されるのはユーザーのPCにあるローカルフォント（前掲図1の**フォント1**）です。したがってthemeで指定されたフォントがインストールされている必要があります。もしユーザーのPCにそれらのフォントがインストールされていなければ、`font-family:`の設定に従って`sans-serif`ないしは`serif`に代替されます。

一方、PDF出力ではクラウドにインストールされたフォント（前掲図2の**フォント2**）が使用されます。もし公式themeで指定されているフォントがクラウドになければ、[クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)に従って別のフォントが使用されます。それぞれの公式themeで、どのようなフォントが指定されているか、クラウド上にどのようなフォントがインストールされているのかは下記をご参照ください。

- [Theme（テーマの選択）](/ja/functions-of-the-actions-menu/theme.md)
- [クラウドにインストールされているフォント一覧](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウドにインストールされているフォント一覧)

こうした代替処理によりプレビューとPDF出力でフォントが異なることで、ページがずれる可能性があることにご注意ください。

## Custom theme／プレビューとPDF出力とでフォントを一致させる

自作したスタイルシートのpathを`vivliostyle.config.js`で指定することにより、そのスタイルシートを使ったPDF出力ができます（→[Custom theme](/ja/functions-of-the-actions-menu/theme.md#custom-theme)）。この時使用されるのはクラウドにインストールされたフォント（前掲図2の**フォント2**）です。

Vivliostyle Pubのクラウドにどのようなフォントがインストールされているのか、またクラウドにインストールされていないフォントが指定された際どのようなフォントで代替されるかは、下記をご参照ください。

- [クラウドにインストールされているフォント一覧](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウドにインストールされているフォント一覧)
- [クラウド上のVivliostyle CLIにおける代替フォントルール](/ja/create-and-save-documents/additional-information-on-fonts.md#クラウド上のvivliostyle-cliにおける代替フォントルール)

ここで問題になるのは、ユーザーのPCにクラウドにあるフォント（前掲図1の**フォント1**）がインストールされていなかった場合です。その場合はプレビューとPDF出力で使われるフォントが一致しないことになります（似たフォントで代替されます）。逆の言い方をすれば、クラウドにあるフォントをPCにもインストールすればプレビューとPDF出力とでフォントを一致させられ、ページのズレも発生しません。

もっとも確実なのは、クラウドにインストールされている[Notoシリーズ](https://fonts.google.com/?query=noto)をPCにもインストールすることです。Googleによるフリーフォントで、ウェイトや対応言語がとても豊富なので、誌面を同じデザインで統一できるメリットもあります。

たとえば、`Noto Sans CJK JP`をインストールした場合、以下のようにCustom themeに記述することで、プレビューでもPDF出力でも`Noto Sans CJK JP`が利用できます。

```css
font-family: 'Noto Sans CJK JP', sans-serif;
```

これ以外にも、Webフォントサービス（図1、図2：**フォント3**）を利用することで、同様にプレビューとPDF出力とでフォントを一致させることができます（次節参照）。

## Custom theme／Googleフォントの使用

Webフォント（前掲図1／図2の**フォント3**）を利用することで、プレビューとPDF出力とでフォントを一致させることができます。本項では無料のWebフォントサービス、GoogleフォントをVivliostyle Pubで使用する方法を説明します。

1. まず[Googleフォント](https://fonts.google.com/)でフォント選択し、つぎにStylesで使いたい太さを “Select this style” 右横にある(+)　をクリックして選択します。ここでは、しっぽり明朝 Regular 400、Noto Sans Japanese Bold 700、Noto Sans Japanese Medium 500を選択しました。

すると、画面右ペインに選択したフォント／スタイルの読み込み用コードが表示されるので、これをコピーします。また、「CSS rules to specify families」から`font-family`のコードもコピーします。

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-7.png)

2. コピーした読み込み用コードをCustom themeにペーストします。

Googleフォントの読み込みコードは、`link`要素と`@import`の2種類用意されていますが、どちらも外部スタイルシートを読み込むもので、機能的には同一です。今回は複数のMarkdownファイルにWebフォントを適用したいので、スタイルシート（CSSファイル）に`@import`の読み込みコードをペーストすることにします（HTMLファイルに使うため前後に`style`要素が入っていますが、それらは取り除いてください）。

それから、忘れずに具体的なフォント名を指定する`font-family`のコードもスタイルシートにペーストします。ここではルート要素にしっぽり明朝 Regular 400を、H1にNoto Sans Japanese Bold 700を、H2にNoto Sans Japanese Medium 500を指定しました。

なお、特定のMarkdownファイルにだけWebフォントを適用したい場合は、当該ファイルの先頭に読み込みコード（`link`要素、及び`style`要素で囲った`@import`のどちらか）をペーストします。スタイルシートで`font-family`を指定するのもお忘れなく。

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-8.png)

3. ActionメニューでCustom themeを選択し、プレビューにWebフォントが適用されたことを確認します。

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-9.png)

4. ActionメニューでExport（出力）>PDFを選択すると、WebフォントでPDF出力ができます。

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-10.png)

Custom themeの利用方法については、下記もご参照ください。

- 参考：[Theme（テーマの選択）> Custom theme](/ja/functions-of-the-actions-menu/theme.md#custom-theme)

## Custom theme／有料Webフォントサービスの使用      

Googleフォントは無料で利用できるWebフォントサービスですが、デメリットは

