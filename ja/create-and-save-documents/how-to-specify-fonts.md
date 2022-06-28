# フォントの指定方法

## フォントを表示するしくみ

Vivliostyle Pubでは以下の3種類の場所にあるフォントを利用することができます。

1. ユーザーのPCにあるローカルフォント（図1：**フォント①**）
2. クラウドにインストールされたフォント（図2：**フォント②**）
3. Webフォントサービスのフォント（図1、図2：**フォント③**）

ただし、プレビューでもPDF出力でも無条件で利用できるフォントは上記3だけです。上記1はプレビューでだけ利用でき、上記2はPDF出力でだけ利用できます（IPAゴシック／IPA Pゴシックを除く）。この違いはVivliostyle Pubがフォントを表示する仕組みによります。本節では、まずこの仕組みについてプレビューとPDF出力とに分けて概説します。ついでActionメニューの項目に沿いながら、3種類のフォントを利用する方法について述べていきます。

プレビューにおいてフォントがどのように使われるかを図1に示しました。ここで注意してほしいのは、プレビューにおける組版エンジンであるVivliostyle.jsは、ユーザーのPC上のフロントエンドにあるということです。組版エンジンはフォントをハンドリングします。したがってユーザーのPCにある**フォント①**もプレビューで利用できるわけです。これ以外に、Webフォントサービスの**フォント③**も利用できます。

ただし、この図にはバックエンドが図示されていません。プレビューにおいてはクラウド上にあるバックエンドのコンポーネントは関与していないのです。したがってクラウドにインストールされた**フォント②**は利用できません。

<img src="images/create-and-save-documents/how-to-specify-fonts/fig-1.jpg" alt="図1 プレビューにおけるフォントの利用" style="max-height: 500px;">

次に、PDF出力においてフォントがどのように使われるかを図2に示しました。ここで注意してほしいのは、PDF出力における組版エンジンであるVivliostyle.jsは、クラウド上のバックエンドにあるということです。したがってクラウドにインストールされた**フォント②**がPDF出力で利用できるわけです。これ以外に、Webフォントサービスの**フォント③**も利用できます。

<img src="images/create-and-save-documents/how-to-specify-fonts/fig-2.jpg" alt="図2 PDF出力におけるフォントの利用" style="max-height: 500px;">

ただし、この図には図1にはあった、フロントエンドのvivliostyle.jsやユーザーのPCにある**フォント①**は図示されていません。PDF出力において、フロントエンドはメニューを通じて指示を出すだで、組版には関与していないのです。したがって**フォント①**は利用できません。

## Plain themeを選択した際に使われるフォント

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-3.png)

Actionメニューから「Plain theme」を選択した場合、プレビューにはブラウザ設定の「標準フォント」が使用されます。ここで使われるフォントは、前掲図1の分類では**フォント①**（ユーザーのPCにあるローカルフォント）です。

したがって、Plain themeをPDF出力すると、プレビューのフォントとは違う意図しない出力結果になることにご注意ください（ブラウザ設定の「標準フォント」でIPAゴシックかIPA Pゴシックを指定していた場合は、プレビューとPDF出力が一致します）。

- 参考：[Theme（テーマの選択）> Plain theme](/ja/functions-of-the-actions-menu/theme.md#plain-theme)

## Vivliostyle公式Themeでのフォント利用

![ ](images/create-and-save-documents/how-to-specify-fonts/fig-4.png)

Actionメニューから、以下のthemeを選択した場合、npm package 管理システム上のVivliostyle公式Themeが使用されます。ぞれぞれのthemeの詳細は、リンク先を参照してください。

- [Book theme for latin font](/ja/functions-of-the-actions-menu/theme.md#book-theme-for-latin-font)
- [文庫用のテーマ](/ja/functions-of-the-actions-menu/theme.md#文庫用のテーマ)
- [Slide theme](/ja/functions-of-the-actions-menu/theme.md#slide-theme)
- [Techbook (技術同人誌) theme](/ja/functions-of-the-actions-menu/theme.md#techbook-技術同人誌-theme)
- [Academic theme](/ja/functions-of-the-actions-menu/theme.md#academic-theme) 

これらのthemeで利用されるフォントは、前掲図1の分類では**フォント①**（ユーザーのPCにあるローカルフォント）です。したがって、これらVivliostyle公式Themeを選択した場合、PDF出力をすると意図しない出力結果になることにご注意ください。

## Custom theme／クラウドにあるフォントの利用

Custom themeでクラウドにインストールされたフォント（前掲図1の**フォント②**）を指定すると、PDF出力にこれらのフォントを利用できます。クラウドにインストールされているフォントのリストは、下記を参照してください。日本語フォントは[IPAゴシック、IPA Pゴシック](https://moji.or.jp/ipafont/)が利用できます。

- [現状の利用可能なフォントについて[vivliostyle-cli]](https://github.com/vivliostyle/vivliostyle-cli/issues/303#issuecomment-1163980308)

ただし、これらのフォントをプレビューにも使うためには、ユーザーのPCに同じフォントをインストールする必要があることにご注意ください。

たとえば、IPA Pゴシックをインストールした上で、以下のようにCustom themeに記述することで、プレビューでもPDF出力でもIPA Pゴシックが利用することができます。

```css
font-family: 'IPAPGothic', sans-serif;
```

## Custom theme／Googleフォントの利用

## Custom theme／有料Webフォントサービスの利用

## 推奨する有料Webフォントサービスの利用方法