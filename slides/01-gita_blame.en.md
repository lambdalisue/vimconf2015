layout: true
class: center, middle
---
class: invert
### Topic 6
# Who did it?
---
When you are developing in a team, you may often face to
# **"What da hell !?"**
The best way to manage this kind of code is executing `git blame`.
---
So you love `git blame`, mean that you would love
# **Gita blame**
which perform `git blame` in Gita interface.
---
layout: true
---
# Gita blame ?

- An alternative of `Gblame` in fugitive<br>
  *However, the UI is completely different*

- To get cool UI, it is a bit slower than `Gblame`<br>
  *There are several points which can improve the performance so I would like to fix these in future*

- Cooperate well with Gita diff, Gita file, Gita browse<br>

- Tons of bugs while it is in a start point of the development

---
# Unfavorable points of Gblame
.center[![fugitive Gblame](img/fugitive_Gblame.png)]

---
# Unfavorable points of Gblame
.left-column[.center[![fugitive Gblame](img/fugitive_Gblame.png)]]

--
.right-column[
- Too many username, too redundant<br>
*At least one user name is required for each commit chunk*
]

--

.right-column[
- Too many commit time, too redundunt<br>
*At least one commit time is required for each commit chunk*
]

--

.right-column[
- Commit messages are not visible<br>
*You need to scroll right. Commit messages are probably most important information in `git blame`*
]

--

.right-column[
- Too difficult to distinguish the commit chunk<br>
*The colors of hashref are different but it is a bit far from the source code*
]

---
# Advantage of Gita blame

--

.center[![gita blame](img/gita_blame.png)]

--

.center.large[**No words needed**]

---
# Advantage of Gita blame

.left-column[
.center[![gita blame](img/gita_blame.png)]
]

.right-column[
- It is easy to distinguish the commit chunk<br>
 *Chunks are separated via psedu lines*
]

--

.right-column[
- No redundant information<br>
 *While chunks are clear, no redundant informations are required*
]

--

.right-column[
- Hit return lead you to the target commit or previous commit<br>
  *Very useful to find a target commit*
]

--

.right-column[
- Cooperate well with `Gita file`, `Gita diff`<br>
 *It would help you to find a target commit as well*
]

---
layout: true
class: center, middle
---
<video controls src="img/gita_blame.webm"></video>
---
# Ultra .highlight[benri] !!!

