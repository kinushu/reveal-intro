# 手軽にプレゼン環境を作りたい　メモ

2015/10/09(fri)

shuhei kinukawa(@kinushu)


---

## どーん

---

## 楽しい

---

## 承前：技術プレゼンのネタ探し

+ 何にしよう
+ 形から入ってみよう
+ 資料作りのツール何があるかな。
+ markdownで資料作れるのがあったはず

---

## 検索:「markdown プレゼン」

+ 結構あるな、、、
+ web上で作成できそうなのたくさんありますが、ローカルで実行できるもの…
+ reveal.js というのがあった。

---

## reveal.js

+ HTML,css,jsだけでプレゼンを構成する。
+ プレゼン内容記述には HTML, markdown を使用できる。

https://github.com/hakimel/reveal.js/

---

## このプレゼンのためにやったこと

1.コード落とす（zipファイルでも可）

```
git clone git@github.com:hakimel/reveal.js.git 20151008presen

```

2.index.html を書き換える

```
				<section data-markdown="./contents.md"
				    data-separator="\n---\n$"
				    data-vertical="\n--\n">
				    <script type="text/template">
				    </script>
				</section>
```

3.contents.md を書いていく

---

よし、index.html をクリック

あれ?
```
Failed to get the Markdown file ./contents.md. ... Failed to execute 'send' on 'XMLHttpRequest'...

```

+ markdownファイルを外だししてる場合、webサーバ経由で見ないといけない、めんどい…
+ (index.html内に直接markdown書く場合は大丈夫のよう)


---

## とりあえずwebサーバ立てたい

4.カレントフォルダ上でwebサーバ

```
$ python -m SimpleHTTPServer
Serving HTTP on 0.0.0.0 port 8000 ...
```

pythonか…

```
$ php -S localhost:8000
PHP 5.5.27 Development Server started at Fri Oct  9 15:53:25 2015
```

phpか…

---

http://localhost:8000/

これでこのプレゼンが表示されています。

---

## reveal.js 操作方法

+ 右 左 でページを移動
+ esc でページリスト

---

## 利点

+ （あまり体裁を凝らなくていい場合）テキストベースでばっと書ける
+ (内容優先で書ける)
+ テキストベースなのでgit管理しやすい
+ webブラウザで表示できる。


---

## 補足

+ ツールによって気分（人格）が変わる。
+ PowerPointならこんな気分にならない。

---

ご静聴ありがとうございました。
