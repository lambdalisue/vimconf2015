layout: true
---
class: center, middle, invert
### Topic 4
# ちゃちゃっとコミット
---
class: center, middle
さて、先ほどの Gita status は便利ですよね？
# この流れでコミットメッセージの編集も簡単にできます
---
class: center, middle
# .highlight[Gita commit]
---
# Gita commit ?

- `Gita commit` と呼び出すかステージング編集バッファで `cc`, `cA`, `cC` を押すことで表示される<br>
  .subtle[`cc`, `cA`, `cC` はそれぞれ `Gita commit`, `Gita commit --amend`, `Gita commit --no-amend`]

- `Gita status` からシームレスに移動可能<br>
  .subtle[普段使いの `cc` はコミット完了まで状態を保持するので amend 後は常に amend で開く]

- `:w` での一時保存、 `:q` や `CC` でのコミットに対応<br>
  .subtle[使い勝手はほぼ fugitive の `Gcommit` と同じ]
---
layout: true
class: center, middle
---
<video controls style="width: 100%">
  <source src="img/gita_commit.webm">
</video>
---
# とても.highlight[便利]
