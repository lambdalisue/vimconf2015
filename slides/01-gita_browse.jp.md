layout: true
---
class: center, middle, invert
### Topic 5
# それ、ブラウザで
---
# けーすすたでぃー

--

「まじかよ、うわーこれ見つけるのに３時間もかかったわー、これ見つ（ｒｙ」

--

「これはこのコードのリンク PR のコメントに書いといたほうがいいな」

--

「えっと……これは 130-145 行目で、このファイルは……」

--

.center.middle.large[**/foo/bar/hoge/....../piyo/puyo/poyo/......**]

--

.center.middle.huge[**So long! No way!**]

---
class: center, middle
# もし、そう思うなら
---
class: center, middle
# **Gita browse**
---
# Gita browse ?

1. ルールに従って URL を作ります<br>
  *デフォルトでは GitHub と BitBucket.org 用のルールが用意されています。もちろんルールの追加も可能です*

2. 上記で作成した URL を 1) ブラウザで開く, 2) クリップボードにコピー, 3) エコー が可能です

3. 各ルールには scheme があり、微妙な URL 調整が可能<br>
  *例えば GitHub 用のルールにはハッシュを利用して URL を作成する "exact" と GitHub の blame を表示する "blame" スキームがあります*

---
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

<video controls src="img/gita_browse_50k.webm"></video>
---

# Very **benri**
