layout: true
---
class: center, middle, invert
### Topic 2
# Figure out which files are changed
---
# Case study

--

R "Check out GitHub. I finished my code review."

--

&Lambda; "Ok. I will"

--

&Lambda; "I see... I didn't know the code can be written like this."

--

&Lambda; "Hum... I think Perl is not for .highlight[Pythonista]. I would like to write .highlight[Vimscript]..."

--

&Lambda; "Anyway, I need to fix it. Let me check the path of this file..."

--

.center.highlight.large[/foo/bar/hoge/……/piyo/well/done.pm]

--

.center.middle.highlight.huge[So long！]

---
layout: true
class: center, middle
---
Like this. While code are reviewed on website usually,
## Don't you think it is .highlight[quite lazy to figure out the file] in the local?
Especially when there are a lot of similar file names
---
# If so
---
# .highlight[Gita diff-ls]
---
layout: true
---
# Gita diff-ls ?

- Gita diff-ls .highlight[{commit}] show a list of files changed compared to .highlight[{commit}]<br>
  .subtle[If you specify `origin/HEAD...` to {commit}, you can compare to a fork point from master.]

- The following actions are available in the list window

  - `ee` - Edit the file in the working tree
  - `oo` - Open the file of the specified commit
  - `dd` - Show diff in diff style (one panel)
  - `DD` - Show diff in vimdiff style (two panel)
---
layout: true
class: center, middle
---
<video controls style="width: 100%">
  <source src="img/gita_diff-ls.webm">
</video>
---
# Very .highlight[useful]

