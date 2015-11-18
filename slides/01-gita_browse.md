layout: true
---
class: center, middle, invert
### Topic 5
# シェアする
---
# けーすすたでぃー

--

「あ、やっとわかった。ここで foo が bar に書き換えられるから Fried になるんだ……」

--

「ちょっとこれは後学のためにも該当コードのリンクを PR にコメントしとこう」

--

「えっと……これは 130-145 行目で、このファイルは……」

--

.center.middle.highlight.large[/foo/bar/hoge/....../piyo/puyo/poyo/......]

--

.center.middle.highlight.huge[So long！No way!]

---
class: center, middle
# そんな貴方に
---
class: center, middle
# .highlight[Gita browse]
---
# Gita browse ?

1. あらかじめ決められたルールに従い URL を作成 -> 表示する<br>
  .subtle[ルールはカスタマイズ可能。自分は職場用の GHE (ローカル) のルールを登録してる]

2. ブラウザを開く・URLをコピペする・URLを表示するの三種類の動作が可能

3. ルールには複数の Scheme を設定でき、Scheme を指定することで違った表示が可能<br>
  .subtle[GitHub 用には URL に hashref を使う Scheme と blame を表示する Scheme がデフォルトで用意されている]
---
# Extra rule

```vim
let g:gita#features#browse#extra_translation_patterns = {
      \ 'gitlab.kawaz.org': [
      \   [
      \     '\vhttps?://(%domain)/(.{-})/(.{-})%(\.git)?$',
      \     '\vgit://(%domain)/(.{-})/(.{-})%(\.git)?$',
      \     '\vgit\@(%domain):(.{-})/(.{-})%(\.git)?$',
      \     '\vssh://git\@(%domain)/(.{-})/(.{-})%(\.git)?$',
      \   ], {
      \     '_':     'https://\1/\2/\3/blob/%c1/%pt%{#L|}ls%{-L|}le',
      \     'exact': 'https://\1/\2/\3/blob/%r1/%pt%{#L|}ls%{-L|}le',
      \     'blame': 'https://\1/\2/\3/blame/%c1/%pt%{#L|}ls%{-L|}le',
      \   },
      \ ],
      \}
```
    %c1	A commit1
    %c2	A commit2. It might be an empty string.
    %r1	A revision (SHA256) of commit1.
    %r2	A revision (SHA256) of commit2. It might be an empty string
    %pt	A relative file path from a top of git working tree
    %ls	A start line number of selection
    %le	A end line number of selection
---
layout: true
class: center, middle
---
<video controls style="width: 100%">
  <source src="img/gita_browse.webm">
</video>
---
# とても.highlight[便利]

