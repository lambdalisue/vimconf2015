layout: true
---
class: center, middle, invert
### Topic 4
# コミットメッセージ
---
class: center, middle
Gita status のように
# コミットメッセージの編集
も簡単にできます。そう vim-gita ならね
---
class: center, middle
# **Gita commit**
---
# Gita commit ?

- コミット編集用バッファでコミットメッセージを編集できます<br>
  *まぁ fugitive の `Gcommit` と同じですね*

- `Gita commit` を呼ぶか先ほどのステージングバッファで `cc`, `cA`, or `cC` を押せばおｋ<br>
  *`cc`, `cA`, `cC` はそれぞれ `Gita commit`, `Gita commit --amend`, `Gita commit --no-amend` を呼びます*

- `:w` で一時保存や `:q` or `CC` でコミットします<br>
  *`Gcommit` と似たキー設計になってます*

---
layout: true
class: center, middle
---
<video controls src="img/gita_commit_50k.webm"></video>
---
# Very **benri**

