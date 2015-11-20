layout: true
---
class: center, middle, invert
### Topic 5
# Cooperate with a browser
---
# Case study

--

"Finally! I got it! It took about 3 hours to figure out!"

--

"Well... I think the link of this code should be written in a comment of the PR"

--

"Let me see... This part is L130-145 of..."

--

.center.middle.large[**/foo/bar/hoge/....../piyo/puyo/poyo/......**]

--

.center.middle.huge[**So long! No way!**]

---
class: center, middle
# If you feel so
---
class: center, middle
# **Gita browse**
---
# Gita browse ?

1. Create a URL followed by the rule<br>
  *In default, rules of GitHub and Bitbucket.org are prepared. You can add your extra rules as well*

2. You can 1) Open a browser, 2) Copy the URL, 3) Echo the URL with the URL created by the rule

3. Each rule can have schemes to create a special URL<br>
  *For example, there are "exact" and "blame" schemes for GitHub. The "exact" scheme use a hashref instead of a branch name. The "blame" scheme use a GitHub's blame URL instead of a blob URL*

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


