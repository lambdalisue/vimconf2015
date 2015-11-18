layout: true
---
class: center, middle, invert
### Topic 2
# どのファイルが更新されたの？
---
# けーすすたでぃー

--

レ「GitHub 上でコードレビューしたので確認しといて」

--

&Lambda;「わかりましたー」

--

&Lambda;「あぁ、なるほど。ここはこういう書き方もできるのか」

--

&Lambda;「.highlight[Pythonista] に Perl は辛い…… .highlight[Vimscript 書きたい……]」

--

&Lambda;「とりあえず修正しよう。えっと、該当ファイルは……」

--

.center.highlight.large[/foo/bar/hoge/……/piyo/well/done.pm]

--

.center.middle.highlight.huge[So long！]

---
layout: true
class: center, middle
---
このように、レビューで指摘を受けたファイル
## 手元で探すの.highlight[面倒くさくないですか？]
とくに似たパスがたくさんあるときは補完すら面倒
---
# そこで
---
# .highlight[Gita diff-ls]
---
layout: true
---
# Gita diff-ls ?

- Gita diff-ls .highlight[{commit}] とすることで .highlight[{commit}] と差があるファイルを一覧表示<br>
  .subtle[{commit} に `origin/HEAD...` を指定することで **master から分岐した時点との比較が可能** = GitHub の PR 差分表示とリンク]

- 一覧表示ウィンドウでは、以下のアクションが可能

  - `ee` でワーキングスペースの該当ファイルを開く
  - `oo` で対象コミットのファイルを開く
  - `dd` で Diff を表示 (diff 形式)
  - `DD` で Diff を表示 (vimdiff 形式)
---
layout: true
class: center, middle
---
<video controls style="width: 100%">
  <source src="img/gita_diff-ls.webm">
</video>
---
# とても.highlight[便利]
