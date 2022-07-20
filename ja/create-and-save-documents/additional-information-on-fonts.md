# フォントに関する補足情報

## クラウドにインストールされているフォント一覧

PDF出力で使われるクラウドのフォントは、なるべく多くの環境との互換性を確保する目的で、下記のフォントセットをインストールしています。

1. [Noto fonts](https://fonts.google.com/noto)
2. [Microsoft TrueType core fonts](https://packages.ubuntu.com/focal/ttf-mscorefonts-installer)

1は1,000以上の言語と150以上の文字体系に対応し、複数のウェイトと幅、そしてゴシック、明朝、等幅といったスタイルをもつ巨大なフォントファミリーです。2はマイクロソフトによるWeb用の標準フォントのパックです。

このほか、Linuxシステム上での標準的なフォントとして次のフォントがインストールされています：

- [liberation-fonts](https://packages.ubuntu.com/focal/fonts-liberation)
- [Thai Loma font](https://packages.ubuntu.com/focal/fonts-tlwg-loma-otf)
- [Ubuntu font](https://design.ubuntu.com/font/)
- [urw-base35-fonts](https://github.com/ArtifexSoftware/urw-base35-fonts)

個々の`font-family`名は下記の通りです。これらをCustom theme（スタイル情報）の中で指定することにより、出力するPDFに埋め込むことができます（→[フォントを利用するしくみ](/ja/create-and-save-documents/how-to-specify-fonts.md#フォントを利用するしくみ)）

`Andale Mono`<br>
`Arial`<br>
`Arial Black`<br>
`C059`<br>
`Comic Sans MS`<br>
`Courier New`<br>
`D050000L`<br>
`Georgia`<br>
`Impact`<br>
`Liberation Mono`<br>
`Liberation Sans`<br>
`Liberation Sans Narrow`<br>
`Liberation Serif`<br>
`Loma`<br>
`Nimbus Mono PS`<br>
`Nimbus Roman`<br>
`Nimbus Sans`<br>
`Nimbus Sans Narrow`<br>
`Noto Color Emoji`<br>
`Noto Kufi Arabic`<br>
`Noto Mono`<br>
`Noto Music`<br>
`Noto Naskh Arabic`<br>
`Noto Naskh Arabic UI`<br>
`Noto Nastaliq Urdu`<br>
`Noto Sans`<br>
`Noto Sans Adlam`<br>
`Noto Sans Adlam Unjoined`<br>
`Noto Sans Arabic`<br>
`Noto Sans Arabic UI`<br>
`Noto Sans Armenian`<br>
`Noto Sans Avestan`<br>
`Noto Sans Bamum`<br>
`Noto Sans Bassa Vah`<br>
`Noto Sans Batak`<br>
`Noto Sans Bengali`<br>
`Noto Sans Bengali UI`<br>
`Noto Sans Bhaiksuki`<br>
`Noto Sans Brahmi`<br>
`Noto Sans Buginese`<br>
`Noto Sans Buhid`<br>
`Noto Sans CJK HK`<br>
`Noto Sans CJK JP`<br>
`Noto Sans CJK KR`<br>
`Noto Sans CJK SC`<br>
`Noto Sans CJK TC`<br>
`Noto Sans Carian`<br>
`Noto Sans Chakma`<br>
`Noto Sans Cham`<br>
`Noto Sans Cherokee`<br>
`Noto Sans Coptic`<br>
`Noto Sans Cuneiform`<br>
`Noto Sans Cypriot`<br>
`Noto Sans Deseret`<br>
`Noto Sans Devanagari`<br>
`Noto Sans Devanagari UI`<br>
`Noto Sans Display`<br>
`Noto Sans Duployan`<br>
`Noto Sans Elbasan`<br>
`Noto Sans Ethiopic`<br>
`Noto Sans Georgian`<br>
`Noto Sans Glagolitic`<br>
`Noto Sans Gothic`<br>
`Noto Sans Grantha`<br>
`Noto Sans Gujarati`<br>
`Noto Sans Gujarati UI`<br>
`Noto Sans Gunjala Gondi`<br>
`Noto Sans Gurmukhi`<br>
`Noto Sans Gurmukhi UI`<br>
`Noto Sans Hanunoo`<br>
`Noto Sans Hatran`<br>
`Noto Sans Hebrew`<br>
`Noto Sans Indic Siyaq Numbers`<br>
`Noto Sans Javanese`<br>
`Noto Sans Kaithi`<br>
`Noto Sans Kannada`<br>
`Noto Sans Kannada UI`<br>
`Noto Sans Kayah Li`<br>
`Noto Sans Kharoshthi`<br>
`Noto Sans Khmer`<br>
`Noto Sans Khmer UI`<br>
`Noto Sans Khojki`<br>
`Noto Sans Khudawadi`<br>
`Noto Sans Lao`<br>
`Noto Sans Lao UI`<br>
`Noto Sans Lepcha`<br>
`Noto Sans Limbu`<br>
`Noto Sans Linear A`<br>
`Noto Sans Linear B`<br>
`Noto Sans Lisu`<br>
`Noto Sans Lycian`<br>
`Noto Sans Lydian`<br>
`Noto Sans Mahajani`<br>
`Noto Sans Malayalam`<br>
`Noto Sans Malayalam UI`<br>
`Noto Sans Mandaic`<br>
`Noto Sans Manichaean`<br>
`Noto Sans Marchen`<br>
`Noto Sans Masaram Gondi`<br>
`Noto Sans Math`<br>
`Noto Sans Mayan Numerals`<br>
`Noto Sans Meetei Mayek`<br>
`Noto Sans Mende Kikakui`<br>
`Noto Sans Meroitic`<br>
`Noto Sans Miao`<br>
`Noto Sans Modi`<br>
`Noto Sans Mongolian`<br>
`Noto Sans Mono`<br>
`Noto Sans Mono CJK HK`<br>
`Noto Sans Mono CJK JP`<br>
`Noto Sans Mono CJK KR`<br>
`Noto Sans Mono CJK SC`<br>
`Noto Sans Mono CJK TC`<br>
`Noto Sans Mro`<br>
`Noto Sans Multani`<br>
`Noto Sans Myanmar`<br>
`Noto Sans Myanmar UI`<br>
`Noto Sans Nabataean`<br>
`Noto Sans New Tai Lue`<br>
`Noto Sans Newa`<br>
`Noto Sans Ogham`<br>
`Noto Sans Ol Chiki`<br>
`Noto Sans Old Italic`<br>
`Noto Sans Old Permic`<br>
`Noto Sans Old Persian`<br>
`Noto Sans Old Sogdian`<br>
`Noto Sans Old Turkic`<br>
`Noto Sans Oriya`<br>
`Noto Sans Oriya UI`<br>
`Noto Sans Osage`<br>
`Noto Sans Osmanya`<br>
`Noto Sans Pahawh Hmong`<br>
`Noto Sans Palmyrene`<br>
`Noto Sans Pau Cin Hau`<br>
`Noto Sans PhagsPa`<br>
`Noto Sans Phoenician`<br>
`Noto Sans Rejang`<br>
`Noto Sans Runic`<br>
`Noto Sans Samaritan`<br>
`Noto Sans Saurashtra`<br>
`Noto Sans Sharada`<br>
`Noto Sans Shavian`<br>
`Noto Sans Siddham`<br>
`Noto Sans Sinhala`<br>
`Noto Sans Sinhala UI`<br>
`Noto Sans Sogdian`<br>
`Noto Sans Soyombo`<br>
`Noto Sans Sundanese`<br>
`Noto Sans Syloti Nagri`<br>
`Noto Sans Symbols`<br>
`Noto Sans Symbols2`<br>
`Noto Sans Syriac`<br>
`Noto Sans Tagalog`<br>
`Noto Sans Tagbanwa`<br>
`Noto Sans Tai Le`<br>
`Noto Sans Tai Tham`<br>
`Noto Sans Tai Viet`<br>
`Noto Sans Takri`<br>
`Noto Sans Tamil`<br>
`Noto Sans Tamil Supplement`<br>
`Noto Sans Tamil UI`<br>
`Noto Sans Telugu`<br>
`Noto Sans Telugu UI`<br>
`Noto Sans Thaana`<br>
`Noto Sans Thai`<br>
`Noto Sans Thai UI`<br>
`Noto Sans Tibetan`<br>
`Noto Sans Tifinagh`<br>
`Noto Sans Tirhuta`<br>
`Noto Sans Ugaritic`<br>
`Noto Sans Vai`<br>
`Noto Sans Wancho`<br>
`Noto Sans Warang Citi`<br>
`Noto Sans Yi`<br>
`Noto Serif`<br>
`Noto Serif Ahom`<br>
`Noto Serif Armenian`<br>
`Noto Serif Balinese`<br>
`Noto Serif Bengali`<br>
`Noto Serif CJK JP`<br>
`Noto Serif CJK KR`<br>
`Noto Serif CJK SC`<br>
`Noto Serif CJK TC`<br>
`Noto Serif Devanagari`<br>
`Noto Serif Display`<br>
`Noto Serif Dogra`<br>
`Noto Serif Ethiopic`<br>
`Noto Serif Georgian`<br>
`Noto Serif Gujarati`<br>
`Noto Serif Gurmukhi`<br>
`Noto Serif Hebrew`<br>
`Noto Serif Kannada`<br>
`Noto Serif Khmer`<br>
`Noto Serif Lao`<br>
`Noto Serif Malayalam`<br>
`Noto Serif Myanmar`<br>
`Noto Serif Sinhala`<br>
`Noto Serif Tamil`<br>
`Noto Serif Tamil Slanted`<br>
`Noto Serif Tangut`<br>
`Noto Serif Telugu`<br>
`Noto Serif Thai`<br>
`Noto Serif Tibetan`<br>
`P052`<br>
`Standard Symbols PS`<br>
`Times New Roman`<br>
`Trebuchet MS`<br>
`URW Bookman`<br>
`URW Gothic`<br>
`Ubuntu`<br>
`Ubuntu Condensed`<br>
`Ubuntu Mono`<br>
`Verdana`<br>
`Webdings`<br>
`Z003`<br>

なお、 各フォントがサポートするウェイトを含む詳細なリストは、こちらをご参照ください（→[fc-list.sorted](/ja/create-and-save-documents/fc-list.sorted.md)）

## クラウド上のVivliostyle CLIにおける代替フォントルール

PDF出力に際して、前項のリストにないフォントが指定された場合、以下のように代替されます。

| 指定されたフォント                                                                                                                                            | 代替されるフォント      |     | 
| ------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | --- | 
|  Times  |  Times New Roman  |
|  Helvetica  |  Arial  |
|  Courier  | Courier New   |
|  `font-family: fantasy;`  |  Impact  |
|  `font-family: cursive`  |  Comic Sans MS  |
|  `font-family: monospace;`  |  Andale Mono  |
| Source Han Serif<br>Hiragino Mincho ProN<br>Hiragino Mincho Pro<br>YuMincho<br>Yu Mincho<br>MS Mincho<br>MS PMincho                                     | Noto Serif CJK JP |     | 
| Source Han Sans<br>Hiragino Sans<br>Hiragino Kaku Gothic ProN<br>Hiragino Kaku Gothic Pro<br>YuGothic<br>Yu Gothic<br>Meiryo<br>MS Gothic<br>MS PGothic | Noto Sans CJK JP  | 
|  上記以外の欧文フォント  |  Times New Roman  |
|  上記以外の日本語フォント  |  Noto Sans CJK JP  |

- **ご注意**
    - たとえばスタイルシートで`font-family: "IPA明朝", serif;`と指定されていた場合、IPA明朝は前項のリストにも上の表にもありませんから、PDF出力ではブラウザ設定「Serif」のフォント（日本語環境では明朝体）が使用されるはずです。しかし、実際にはNoto Sans CJK JPが使用されてしまいます。
    - 上の表で`Noto Serif CJK JP`に代替されるフォント以外の明朝体フォント全てにこの問題が発生します（逆の言い方をすれば、上の表で`Noto Serif CJK JP`に代替されるフォントはこの問題は発生しません）。私たちはこの問題の解決に努めています。詳細は下記をご参照ください。
        - [font-family: serif を指定しても明朝体にならない問題と対策](https://github.com/vivliostyle/vivliostyle-cli/issues/303#issuecomment-1169786479)

## 推奨する有償Webフォントサービスの用途

有償Webフォントサービスは利用規約によって用途を制限しており、Vivliostyle Pubで無条件にこれらのサービスを利用できるわけではありません。

本来、利用規約の解釈は契約者間で解決すべきであり、第三者である私たちが判断できるものではありません。とはいえ、このままではユーザが安心してVivliostyle PubでWebフォントを使うことはできないでしょう。そこで、各社とコミュニケーションをとりながら、以下の用途を利用規約が許容しているか調査しました。

- Webフォントを使ってプレビューができる
- Webフォントを使ってPDF出力、及びオフセット／オンデマンド印刷ができる
- Webフォントを使って成果物の有償販売ができる

その結果を踏まえ、Webフォントサービスごとに推奨できる用途を選定したのが下記のものです。

|              | [DynaSmart V](https://www.dynacw.co.jp/product/product_dynasmart_detail.aspx?sid=25)           | [DynaSmart T](https://www.dynacw.co.jp/product/product_dynasmart_detail.aspx?sid=43)  | [TypeSquare](https://typesquare.com/ja/)    |[fonts.com](https://www.fonts.com/ja)  | [FONTPLUS](https://fontplus.jp/)※  | [Adobe Fonts](https://fonts.adobe.com/)     |
| ------------ | -------------- | ---------------- | --------------- |  -------------- | ---------------- | --------------- |
| プレビュー | ○                    | ○                      | ×                     | ×                      | ○                   |    ×                 | 
| PDF出力／印刷 |  ○             | ○                      | ×                    | ×                      | ×                   |    ×               | 
| 有償販売     |  ○                    | ○                      | ×                    | ×                      | ×                   |    ×               | 

※……FONTPLUSはプレビューのみ○（ブログでの使用と同じと解釈）。ただし、PDF出力等については個別判断になるので要問い合わせ

より詳細については、以下をご参照ください。

- [VivliostyleでWebフォントを使う 調査編：小形克宏（YouTube）](https://www.youtube.com/watch?v=czVRSsekLjc)
- [VivliostyleでWebフォントを使う：調査編（スライド）](https://vivliostyle.org/viewer/#src=https://github.com/ogwata/slide-20220423-2/blob/main/myslide.html&bookMode=true&spread=false)

## GoogleフォントのうちVivliostyleのPDF出力で “Type 3” にならない日本語フォント一覧

以下は、[Googleフォント](https://fonts.google.com/?subset=japanese)に収録されている日本語フォント50書体のうち、私たちのテストの結果、VivliostyleによるPDF出力で “Type 3” ではなく “TrueType (CID)” として埋め込まれたフォントです。結果として、Noto Sans JapaneseとNoto Serif Japanese を除くすべての日本語フォントでもあります。

一般に “Type 3” としてフォントが埋め込まれたPDFファイルは印刷に不適とされています。一方で “TrueType (CID)” として埋め込まれていれば問題はないとされています。詳細は下記をご参照ください。

- [Actionメニューの機能 > Export（出力）> 補足情報](/ja/functions-of-the-actions-menu/export.md#補足情報)

----------------------------

BIZ UDGothic<br>
BIZ UDMincho<br>
BIZ UDPGothic<br>
BIZ UDPMincho<br>
Dela Gothic One<br>
DotGothic16<br>
Hachi Maru Pop<br>
Hina Mincho<br>
Kaisei Decol<br>
Kaisei HarunoUmi<br>
Kaisei Opti<br>
Kaisei Tokumin<br>
Kiwi Maru<br>
Klee One<br>
Kosugi<br>
Kosugi Maru<br>
M PLUS 1<br>
M PLUS 1 Code<br>
M PLUS 1p<br>
M PLUS 2<br>
M PLUS Rounded 1c<br>
Mochiy Pop One<br>
Mochiy Pop P One<br>
Murecho<br>
New Tegomin<br>
Potta One<br>
Rampart One<br>
Reggae One<br>
RocknRoll One<br>
Sawarabi Gothic<br>
Shippori Antique<br>
Shippori Antique B1<br>
Shippori Mincho<br>
Shippori Mincho B1<br>
Stick<br>
Train One<br>
Yomogi<br>
Yuji Boku<br>
Yuji Mai<br>
Yuji Syuku<br>
Yusei Magic<br>
Zen Antique<br>
Zen Antique Soft<br>
Zen Kaku Gothic Antique<br>
Zen Kaku Gothic New<br>
Zen Kurenaido<br>
Zen Maru Gothic<br>
Zen Old Mincho<br>




