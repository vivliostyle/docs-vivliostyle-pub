# フォントの指定方法

## フォントを表示するしくみ

Vivliostyle Pubでは以下の3種類の場所にあるフォントを利用することができます。

1. ユーザーのPCにあるローカルフォント（図1：**フォント①**）
2. クラウドにインストールされたフォント（図2：**フォント②**）
3. Webフォントサービスのフォント（図1、図2：**フォント③**）

ただし、プレビューでもPDF出力でも無条件で利用できるフォントは上記3だけです。上記1はプレビューでだけ利用でき、上記2はPDF出力でだけ利用できます（IPAゴシック／IPA Pゴシックを除く）。

この違いはVivliostyle Pubがフォントを表示する仕組みによります。本節では、まずこの仕組みについてプレビューとPDF出力とに分けて概説します。ついでActionメニューの項目に沿いながら、3種類のフォントを利用する方法について述べていきます。

プレビューにおいてフォントがどのように使われるかを図1に示しました。ここで注意してほしいのは、実際に組版をおこなうVivliostyle.js（赤色）は、プレビューにおいてはユーザーのPC上のフロントエンドにあるということです。組版エンジンはフォントをハンドリングします。したがってユーザーのPCにある**フォント①**がプレビューで利用できるわけです。これ以外に、Webフォントサービスの**フォント③**も利用できます。

ただし、この図にはバックエンドが図示されていません。プレビューにおいてはクラウド上にあるバックエンドのコンポーネントは関与していないのです。したがってクラウドにインストールされた**フォント②**は利用できません。

<img src="images/create-and-save-documents/how-to-specify-fonts/fig-1.jpg" alt="図1 プレビューにおけるフォントの利用" style="max-height: 500px;">

次に、PDF出力においてフォントがどのように使われるかを図2に示しました。注意してほしいのは、実際に組版をおこなうVivliostyle.js（赤色）は、PDF出力ではクラウド上のバックエンドにあるということです。したがってクラウドにインストールされた**フォント②**がPDF出力で利用できるわけです。これ以外に、Webフォントサービスの**フォント③**も利用できます。

<img src="images/create-and-save-documents/how-to-specify-fonts/fig-2.jpg" alt="図2 PDF出力におけるフォントの利用" style="max-height: 500px;">

ただし、上の図には図1にはあった、フロントエンドのvivliostyle.jsやユーザーのPCにある**フォント①**は図示されていません。PDF出力において、フロントエンドはメニューを通じて指示を出すだけで、組版には関与していないのです。したがって**フォント①**も利用できません。

## Plain themeを選択した際に使われるフォント

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-3.png)

Plain themeはデフォルト設定です。プレビューにおけるスタイルはブラウザのデフォルト設定にしたがいます。たとえばフォントは、ブラウザ設定の「標準フォント」が参照されます。これは、前掲図1の分類では**フォント①**（ユーザーのPCにあるローカルフォント）です。一方、PDF出力ではクラウド上のVivliostyle CLIのデフォルト設定にしたがいます。この結果、Plain themeをPDF出力すると、プレビューのフォントとは違う意図しない出力結果になることにご注意ください。

Plain themeについては、以下もご参照ください。

- [Theme（テーマの選択）> Plain theme](/ja/functions-of-the-actions-menu/theme.md#plain-theme)

## Vivliostyle公式Themeでのフォント利用

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-4.png)

Actionメニューから、以下のthemeを選択した場合、npm package 管理システム上のVivliostyle公式Themeが使用されます。ぞれぞれのthemeの詳細は、リンク先を参照してください。

- [Book theme for latin font](/ja/functions-of-the-actions-menu/theme.md#book-theme-for-latin-font)
- [文庫用のテーマ](/ja/functions-of-the-actions-menu/theme.md#文庫用のテーマ)
- [Slide theme](/ja/functions-of-the-actions-menu/theme.md#slide-theme)
- [Techbook (技術同人誌) theme](/ja/functions-of-the-actions-menu/theme.md#techbook-技術同人誌-theme)
- [Academic theme](/ja/functions-of-the-actions-menu/theme.md#academic-theme) 

これらのthemeで利用されるフォントは、前掲図1の分類では**フォント①**（ユーザーのPCにあるローカルフォント）です。プレビューにおいて、もしユーザーのPCにそれらのフォントがインストールされていなければ、`font-family:`の設定に従って`sans-serif`ないしは`serif`に代替されます。それぞれの公式themeでどのようなフォントが指定されているかは、下記をご参照ください。

- [Theme（テーマの選択）](/ja/functions-of-the-actions-menu/theme.md#plain-theme)

PDF出力においても公式themeで指定されたフォントが利用できるべきですが、今のところ以下の問題でそれができません。

- [ themeの設定により「テーマの準備に失敗しました」エラーになる #202 ](https://github.com/vivliostyle/vivliostyle-pub/issues/202)

したがって、PDF出力では公式themeで指定されているフォントは利用できず、意図しない出力結果になることにご注意ください。

## Custom theme／クラウドにあるフォントの利用

Custom themeでクラウドにインストールされたフォント（前掲図2の**フォント②**）を指定すると、PDF出力でそれらのフォントが利用できます。クラウドにインストールされているフォントのリストは、下記を参照してください。日本語フォントは[IPAゴシック、IPA Pゴシック](https://moji.or.jp/ipafont/)が利用できます。

- [現状の利用可能なフォントについて[vivliostyle-cli]](https://github.com/vivliostyle/vivliostyle-cli/issues/303#issuecomment-1163980308)

ただし、これらのフォントをプレビューにも使うためには、ユーザーのPCにもIPAゴシック、IPA Pゴシックをインストールする必要があることにご注意ください（前掲図1の**フォント①**）。

たとえば、IPA Pゴシックをインストールした場合、以下のようにCustom themeに記述することで、プレビューでもPDF出力でもIPA Pゴシックが利用できます。

```css
font-family: 'IPAPGothic', sans-serif;
```

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-5.png)

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-6.png)

Custom themeの利用方法については、下記もご参照ください。

- 参考：[Theme（テーマの選択）> Custom theme](/ja/functions-of-the-actions-menu/theme.md#custom-theme)

## Custom theme／Googleフォントの利用

Webフォント（前掲図1／図2の**フォント③**）を利用することで、プレビューでもPDF出力でもお好みのフォントを利用することができます。本項では無料のWebフォントサービス、GoogleフォントをVivliostyle Pubで使用する方法を説明します。

1. まず[Googleフォント](https://fonts.google.com/)でフォント選択し、つぎにStylesで使いたい太さを “Select this style” 右横にある[+]　をクリックして選択します。ここでは、しっぽり明朝 Regular 400、Noto Sans Japanese Bold 700、Noto Sans Japanese Medium 500を選択しました。

すると、画面右ペインに選択したフォントの読み込み用コードが表示されるので、これをコピーします。また、「CSS rules to specify families」から`font-family`のコードもコピーします。

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

## Custom theme／有料Webフォントサービスの利用

## 推奨する有料Webフォントサービスの利用方法