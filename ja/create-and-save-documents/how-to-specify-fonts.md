# フォントの指定方法

## フォントを表示するしくみ

Vivliostyle Pubでは以下の3種類の場所にあるフォントを使用できます。

1. ユーザーのPCにあるローカルフォント（図1フォント①）
2. クラウドにインストールされたフォント（図2フォント②）
3. 外部Webフォントサービスのフォント（図1、図2フォント③）

上記のうち、無条件でプレビューにおいてもPDF出力においても利用できるのは3だけです。1はプレビューでだけ利用でき、2はPDF出力でだけ利用できます。この違いはVivliostyle Pubがフォントを表示する仕組みによるものです。本節では、まずこの仕組みについてプレビューとPDF出力とに分けて概説します。ついでActionメニューの項目に沿いながら、3種類のフォントの指定方法について述べていきます。

プレビューにおいてフォントがどのように使われるかを図1に示しました。ここで注意してほしいのは、プレビューにおける組版エンジンであるVivliostyle.jsは、ユーザーのPC上のフロントエンドにあるということです。組版エンジンはフォントをハンドリングします。したがってユーザーのPCにあるローカルフォントもプレビューで利用できるわけです。これ以外に、外部Webフォントサービスのフォントも利用できます。

ただし、この図にはバックエンドが図示されていません。プレビューにおいてはクラウド上にあるバックエンドのコンポーネントは関与していないのです。したがってクラウドにインストールされたフォントも利用できないという訳です。

<img src="images/create-and-save-documents/how-to-specify-fonts/fig-1.jpg" alt="図1 プレビューにおけるフォントの利用" style="max-height: 500px;">

次に、PDF出力においてフォントがどのように使われるかを図2に示しました。ここで注意してほしいのは、PDF出力における組版エンジンであるVivliostyle.jsは、クラウド上のバックエンドにあるということです。したがってクラウドにインストールされたフォントがPDF出力で利用できるわけです。これ以外に、外部Webフォントサービスのフォントも利用できます。

<img src="images/create-and-save-documents/how-to-specify-fonts/fig-2.jpg" alt="図2 PDF出力におけるフォントの利用" style="max-height: 500px;">

ただし、この図には図1にはあった、フロントエンドのvivliostyle.jsやユーザーのPCにあるローカルフォントは図示されていません。PDF出力においてはフロントエンドはメニューを通じて指示を出すだで、組版には関与していないのです。したがってユーザーのPCにあるローカルフォントも利用できないというわけです。


なお、クラウドにインストールされているフォントのリストは、下記を参照してください。

- [現状の利用可能なフォントについて[vivliostyle-cli]](https://github.com/vivliostyle/vivliostyle-cli/issues/303#issuecomment-1163980308)

日本語フォントは[IPAゴシック、IPA Pゴシック](https://moji.or.jp/ipafont/)が利用できます。ただし、ユーザーのPCにこれらのフォントがインストールされていなければ、プレビューでは利用できません。

もちろん、インストールされていれば話しは別です。たとえば以下のようにCustom themeの中で指定し、且つユーザーのPCにIPA Pゴシックがインストールされていた場合、プレビューでもPDF出力でもIPA Pゴシックが利用できます。

```
font-family: 'IPAPGothic', sans-serif;
```

## themeライブラリのフォント利用

## Custom theme／クラウドにあるフォントの利用

## Custom theme／Googleフォントの利用

## Custom theme／有料Webフォントサービスの利用

## 推奨する有料Webフォントサービスの利用方法