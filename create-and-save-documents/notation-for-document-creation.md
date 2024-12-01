# Notation for Document Creation

Documents in Vivliostyle Pub are created using a notation called Markdown. Here, we will introduce only the main notations. For details, please refer to the following:

- [Special Feature: Let's Create a Doujinshi with Create Book!](https://vivliostyle.org/make-books-with-create-book/#vfm-%E3%81%A7%E5%8E%9F%E7%A8%BF%E3%82%92%E6%9B%B8%E3%81%84%E3%81%A6%E3%81%BF%E3%82%88%E3%81%86)
- [Introduction to VFM Summer 2021](https://vivliostyle.github.io/vivliostyle_doc/vivliostyle-user-group-vol5/content/akabeko/index.html)
- [Vivliostyle Flavored Markdown](https://vivliostyle.github.io/vfm/#/vfm)

## Headings

There are six levels of headings. From the largest heading `#` to the smallest `######`, the more hashes, the lower the level of the heading. Please write the heading text with a space after the hash.

### Notation

```md
# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6
```
### Vivliostyle Pub Editor

![ ](images/create-and-save-documents/notation-for-document-creation/fig-1.png)

### Vivliostyle Pub Preview

![ ](images/create-and-save-documents/notation-for-document-creation/fig-2.png)

## Lists

There are three types of lists: lists with `*`, `-`, or `+` at the beginning (disc), lists with numbers and periods (decimal), and checkboxes. Note that in numbered lists, it is not necessary to write the numbers in order. They will be rendered in descending order from the first number.

### Notation

```md
## Disc List

* The ball that is hit high enters the clouds and falls back into the hands of the person (Shiki Masaoka)
- The ball that is hit high enters the clouds and falls back into the hands of the person (Shiki Masaoka)
+ The ball that is hit high enters the clouds and falls back into the hands of the person (Shiki Masaoka)

## Decimal List

1. The ball that is hit high enters the clouds and falls back into the hands of the person (Shiki Masaoka)
1. The ball that is hit high enters the clouds and falls back into the hands of the person (Shiki Masaoka)
2. The ball that is hit high enters the clouds and falls back into the hands of the person (Shiki Masaoka)

## Checkbox List

- [ ] The ball that is hit high enters the clouds and falls back into the hands of the person (Shiki Masaoka)
- [x] The ball that is hit high enters the clouds and falls back into the hands of the person (Shiki Masaoka)
```

### Vivliostyle Pub Editor

![ ](images/create-and-save-documents/notation-for-document-creation/fig-3.png)

### Vivliostyle Pub Preview

![ ](images/create-and-save-documents/notation-for-document-creation/fig-4.png)

## Emphasis

There are two types of emphasis. Enclosing text with `*` makes it italic, and enclosing it with `**` makes it bold. In HTML notation, the former corresponds to the em element and the latter to the strong element.

### Notation

```md
## Emphasis

### em Element

"Hey, criminals. *This spider's thread is mine. Who did you ask to climb up?* Get down. Get down." he shouted. At that moment, the spider's thread, which had been fine until then, suddenly snapped from where Kandata was hanging.

### strong Element

"Hey, criminals. **This spider's thread is mine. Who did you ask to climb up?** Get down. Get down." he shouted. At that moment, the spider's thread, which had been fine until then, suddenly snapped from where Kandata was hanging.
```

### Vivliostyle Pub Editor

![ ](images/create-and-save-documents/notation-for-document-creation/fig-5.png)

### Vivliostyle Pub Preview

![ ](images/create-and-save-documents/notation-for-document-creation/fig-6.png)

## Strikethrough

Enclosing text with `~~` makes it strikethrough.

### Notation

```md
## Strikethrough

"Hey, criminals. ~~This spider's thread is mine. Who did you ask to climb up?~~ Get down. Get down." he shouted. At that moment, the spider's thread, which had been fine until then, suddenly snapped from where Kandata was hanging.
```

### Vivliostyle Pub Editor

![ ](images/create-and-save-documents/notation-for-document-creation/fig-7.png)

### Vivliostyle Pub Preview

![ ](images/create-and-save-documents/notation-for-document-creation/fig-8.png)

## Links

In the format `[string](URL)`, the "string" part can be made clickable. Writing the URL directly also makes it clickable. You can also write embedded elements such as Twitter and YouTube.

### Notation

```html
## Links

[Vivliostyle](https://vivliostyle.org/) is an open-source project that creates a new typesetting system for electronic publishing and web publishing using the latest web standard technologies.

https://vivliostyle.org/

<blockquote class="twitter-tweet" data-partner="tweetdeck"><p lang="en" dir="ltr">
We released Vivliostyle CLI v4.1.0 with Vivliostyle.js v2.9.1.<br>✅Support the @ supports CSS at-rule (feature queries)<br>
✅MathJax Content MathML extension is enabled<a href="https://t.co/Me1coX2Hlp">https://t.co/Me1coX2Hlp
</a></p>&mdash; Vivliostyle (@Vivliostyle) <a href="https://twitter.com/Vivliostyle/status/1436735010921332736?ref_src=twsrc%5Etfw">
September 11, 2021</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

```

### Vivliostyle Pub Editor

![ ](images/create-and-save-documents/notation-for-document-creation/fig-9.png)

### Vivliostyle Pub Preview

![ ](images/create-and-save-documents/notation-for-document-creation/fig-10.png)

## Ruby

Ruby can be written in the format `{base|ruby}`. Please note that half-width characters are used instead of full-width characters.

### Notation

```md
## Ruby

- {打|う}ち{揚|あ}ぐる　ボールは{高|たか}く{雲|くも}に{入|い}りて　{又|また}{落|お}ち{来|きた}る{人|ひと}の{手|て}の{中|なか}に（正岡子規）
- マッチ{擦|す}る　つかのま{海|うみ}に{霧|きり}ふかし　{身捨|みす}つるほどの{祖国|そこく}はありや（寺山修司）
- {友|とも}がみな　われよりえらく{見|み}ゆる{日|ひ}よ　{花|はな}を{買|か}ひ{来|き}て{妻|つま}としたしむ（石川啄木）
- ああ{皐月|さつき}　{仏蘭西|ふらんす}の{野|の}は{火|ひ}の{色|いろ}す　{君|きみ}も{雛罌粟|こくりこ}われも{雛罌粟|こくりこ}（与謝野晶子）
```

### Vivliostyle Pub Editor

![ ](images/create-and-save-documents/notation-for-document-creation/fig-11.png)

### Vivliostyle Pub Preview

![ ](images/create-and-save-documents/notation-for-document-creation/fig-12.png)

## Tables

You can create tables by enclosing the text in cells with `|`. By inserting a row with cell text as `|-----|` in the second row, you can make the first row a header.

### Notation

```md
## Tables

| Header1  | Header2  | Header3 |
| ------  | -------  | -----  |
| Column1  | Column2  | Column3 |
| Column4  | Column5  | Column6 |
```

### Vivliostyle Pub Editor

![ ](images/create-and-save-documents/notation-for-document-creation/fig-13.png)

### Vivliostyle Pub Preview

![ ](images/create-and-save-documents/notation-for-document-creation/fig-14.png)

## Tategaki (Vertical Writing)

Unfortunately, vertical writing cannot be expressed in Markdown yet. Use the HTML span element and the tcy attribute `<span class="tcy">` and the closing tag `</span>` to enclose the numbers.

### Notation

```html
## Tategaki (Vertical Writing)

The village of Hayama was born through a merger, but <span class="tcy">36</span> years later, in Taisho <span class="tcy">14</span>
(<span class="tcy">1</span><span class="tcy">9</span><span class="tcy">2</span><span class="tcy">5</span>), on January <span class="tcy">1</span>, it became "Hayama Town" without merging again. The range of Hayama Town is the same as that of Hayama Village 320 years ago, and at the same time, it coincides with the range of the six villages in the Edo period, making it a rare example in Japan.
```

### Vivliostyle Pub Editor

![ ](images/create-and-save-documents/notation-for-document-creation/fig-15.png)

### Vivliostyle Pub Preview

![ ](images/create-and-save-documents/notation-for-document-creation/fig-16.png)

## Image Captions and Size Specification

### Notation

```md
## Image Captions and Size Specification

![View of the southern sky from the ruins of Chigasaki Battery](IMG_5694-2.jpeg){width=100%}
```

### Vivliostyle Pub Editor

![ ](images/create-and-save-documents/notation-for-document-creation/fig-17.png)

### Vivliostyle Pub Preview

![ ](images/create-and-save-documents/notation-for-document-creation/fig-18.png)
