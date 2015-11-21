layout: true
---
class: center, middle, invert
### Topic 2
# どのファイルが更新された
---
# けーすすたでぃー

--

レ 「レビュー終わったから GitHub チェックしといて」

--

&Lambda; 「うっす」

--

&Lambda; 「へーここはこうやって書くこともできるのか……」

--

&Lambda; 「うーん **Pythonista** に Perl 辛い…… **Vimscript** 書きたい」

--

&Lambda; 「まぁいいや、とりあえず直さないと。えっと、このファイルは……」

--

.center.large[**/foo/bar/hoge/……/piyo/well/done.pm**]

--

.center.middle.huge[**So long !**]

---
layout: true
class: center, middle
---
このように、ウェブ上でレビューを受けたファイル
## ローカルから探して開くの**面倒くさくないですか？**
特に似たような名前のファイルがいっぱいある時
---
# そこで
---
# **Gita diff-ls**
---
layout: true
---
# Gita diff-ls ?

- `Gita diff-ls [{commit}]` とすることで `{commit}` から変更のあったファイルを一覧表示します<br>
  *`origin/HEAD...` と `{commit}` に指定することで `origin/HEAD` からフォークした時点と比較可能*

- 以下のようなマッピングが与えられています

  - `ee` - 編集用にワーキングツリーのファイルを開く
  - `oo` - 指定されたコミット時点のファイルを表示する
  - `dd` - Diff を表示する
  - `DD` - Diff を 2 ペインで表示する
---
layout: true
class: center, middle
---
<video controls src="img/gita_diff-ls_50k.webm"></video>
---
# ベリー **useful**

