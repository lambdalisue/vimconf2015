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

&Lambda; "Hum... I think Perl is not for **Pythonista**. I would like to write **Vimscript**..."

--

&Lambda; "Anyway, I need to fix it. Let me check the path of this file..."

--

.center.large[**/foo/bar/hoge/……/piyo/well/done.pm**]

--

.center.middle.huge[**So long !**]

---
layout: true
class: center, middle
---
Like this. While code are reviewed on website usually,
## Don't you think it is **a bit lazy to find files** in local?
Especially when there are a lot of files with similar names
---
# If so
---
# **Gita diff-ls**
---
layout: true
---
# Gita diff-ls ?

- `Gita diff-ls [{commit}]` show a list of files changed compared to `{commit}`<br>
  *If you specify `origin/HEAD...` to `{commit}`, you can compare to a fork point from `origin/HEAD`*

- The following actions are available in the list window

  - `ee` - Edit the file in the working tree
  - `oo` - Open the file of the specified commit
  - `dd` - Show diff in diff style (one panel)
  - `DD` - Show diff in vimdiff style (two panel)
---
layout: true
class: center, middle
---
<video controls src="img/gita_diff-ls.webm"></video>
---
# Very **useful**

