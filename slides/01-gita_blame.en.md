layout: true
class: center, middle
---
class: invert
### Topic 6
# Who did it?
---
When you are developping in a team, you may often face to
# .highlight["What da hell !?"]
The best way to manage this kind of code is executing `git blame`.
---
So you love `git blame`, mean that you would love
# .highlight[Gita blame]
which perform `git blame` in Gita interface.
---
layout: true
---
# Gita blame ?

- An alternative of `Gblame` in fugitive<br>
  .subtle[However, the UI is completely different]

- To get cool UI, it is a bit slower than `Gblame`<br>
  .subtle[There are several points which can improve the performance so I would like to fix these in future]

- Cooperate well with Gita diff, Gita file, Gita browse<br>

- Tons of bugs while it is in a start point of the development

---
# Unfavorable points of Gblame
.absolute[.center.w100[![fugitive Gblame](img/fugitive_Gblame.png)]]
---
# Unfavorable points of Gblame
.absolute.transparent[.center.w100[![fugitive Gblame](img/fugitive_Gblame.png)]]

.center[
Well... For me, it is quite
# .highlight[Difficult to understand]
]
--

- Too many username, too redundant

--

- Too many commit time, too redundunt

--

- Commit message is not visible (you need to scroll right)

--

- Too difficult to distinguish the commit chunk
---
# Advantage of Gita blame
--

.center.w100[![gita blame](img/gita_blame.png)]

--

.center.highlight.huge[Beautiful...!!!]

---
# Advantage of Gita blame

.absolute.transparent[.center.w100[![gita blame](img/gita_blame.png)]]

- It is easy to distinguish the commit chunk

--

- No redundunt information

--

- Dig into the commit or previous commit with `<Enter>`

--

- `Gita browse` lead you to a blame page of GitHub

---
layout: true
class: center, middle
---
<video controls style="width: 100%">
  <source src="img/gita_blame.webm">
</video>
---
# Ultra .highlight[benri] !!!

