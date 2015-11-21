layout: true
class: center, middle
---
class: invert
### Topic 6
# どうしてこうなった
---
チームなどで開発しているとよく発生する
# **どうしてこうなった！？**
これを解決する手っ取り早い方法が `git blame` ですね
---
みんな大好き `git blame` そんな貴方は
# **Gita blame**
のことも、きっと気にいると思います
---
layout: true
---
# Gita blame ?

- fugitive の `Gblame` みたいなもんです<br>
  *ただ、UIは根本的に異なります*

- いい感じの UI 作るために無茶やってるのでちょっと遅いです<br>
 *リファクタリング可能な部分が山ほどあるのでそのうち高速化したい*

- Gita diff, Gita file や Gita browse と連携<br>

- バグだらけです。開発中なのでご了承

---
# Gblame の辛いところ
.center[![fugitive Gblame](img/fugitive_Gblame.png)]

---
# Gblame の辛いところ
.left-column[.center[![fugitive Gblame](img/fugitive_Gblame.png)]]

--
.right-column[
- ユーザーネームの嵐<br>
*コミット単位ごとでいいですよね……*
]

--

.right-column[
- コミットタイムの嵐<br>
*これもコミット単位ごとでいいですよね……*
]

--

.right-column[
- コミットメッセージが見えない<br>
*右にスクロールしないと見えません。おそらく `git blame` でもっとも重要な印象なはずなのに……*
]

--

.right-column[
- コミット単位がわかりにくい<br>
*ハッシュが色分けされてますが、ソースコードから遠すぎて辛い感じです*
]

---
# Gita blame のいいところ

--

.center[![gita blame](img/gita_blame.png)]

--

.center.large[**説明不要の美しさ……！**]

---
# Gita blame のいいところ

.left-column[
.center[![gita blame](img/gita_blame.png)]
]

.right-column[
- コミット単位がわかりやすい<br>
 *仮想的なラインで区切られています。もちろん行番号も正しく表示してます*
]

--

.right-column[
- 情報はシンプルに。冗長な情報は省く<br>
 *コミット単位がわかりやすいので、最低限必要な情報だけ表示してます*
]

--

.right-column[
- Enter でコミットを巡れる<br>
  *問題のコミットを探すのに便利*
]

--

.right-column[
- `Gita file` や `Gita diff` といい感じに連携<br>
  *問題のコミットを探すのに便利*
]

---
layout: true
class: center, middle
---
<video controls src="img/gita_blame_50k.webm"></video>
---
# Ultra **benri** !!!

