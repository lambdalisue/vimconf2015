layout: true
class: center, middle
---
class: invert
### Topic 7
# なんだよこの糞コード……<br>って俺のコードじゃねぇか!
---
共同で開発している時によく発生する
# .highlight[「どうしてこうなった！」]
それを解決する一番の方法は `git blame` ですね
---
みんな大好き `git blame`。それを Gita で行うのが
# .highlight[Gita blame]
きっとあなたも好きになる
---
layout: true
---
# Gita blame ?

- fugitive の `Gblame` 相当。ただし UI は全く異なる<br>
  .subtle[GitHub の Blame がとても見やすいのでそちらに近づけた]

- UI 向上のために凄いことしてるので低速<br>
  .subtle[リファクタリング可能な部分がたくさんあるので治したい]

- Gita diff, Gita file, Gita browse などとも連携<br>
  .subtle[blame 対象のファイルを開いたり GitHub で blame を見たり]
- 絶賛開発中。バグ多し

---
# Gblame (fugitive) の難点
.absolute[.center.w100[![fugitive Gblame](img/fugitive_Gblame.png)]]
---
# Gblame (fugitive) の難点
.absolute.transparent[.center.w100[![fugitive Gblame](img/fugitive_Gblame.png)]]

.center[
言葉に出来ないくらいとりあえず
# .highlight[見づらい]
]
--

- ユーザー名がとても冗長

--

- コミット時間がとても冗長

--

- コミットメッセージが隠れてる（横スクロールすれば見える）

--

- コミット単位（チャンク）がわかりにくい
---
# Gita blame の利点
--

.center.highlight.huge[見たまえ！<br>これが<ruby><rb>&Lambda;</rb><rt>ラムダ</rt>の雷だ！]

---

.center.w100[![gita blame](img/gita_blame.png)]

--

.center.highlight.huge[圧倒的視認性...!!!]

---
# Gita blame の利点
--

- コミット単位でわかりやすく分割されている。

--

- 冗長な情報が表示されないようになっているので目に優しい

--

- `<Enter>` で下層に潜ることができ、blame 旅行が可能

--

- `Gita browse` を実行すると GitHub の blame に飛ぶ

---
layout: true
class: center, middle
---
<video controls style="width: 100%">
  <source src="img/gita_blame.webm">
</video>
---
# とても.highlight[便利]
