layout: true
---
class: center, middle, invert
### Topic 3
# Stage or unstage changes
---
# Case study

--

"Alright, I should commit **this finished part**."

--

"Which files should I stage? Let me see..."

--

```
$ git status
```

--

```
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   foo/bar/hoge/……/piyo/puyo/ponyo.pl
        modified:   foo/bar/hoge/……/piyo/puyo/oyo.pl
        .
        .
        .
```
--

.center.middle.huge[**So many! So long!**]

---
layout: true
class: center, middle
---
When you edit a lot of files and need to call `git add` **individually**
## Can you be bothered to do that?
Or you may call `git add .` to mix everything into a single commit
---
# Then
---
# **Gita status**
---
layout: true
---
# Gita status ?

- An alternative of `Gstatus` in fugitive<br>
  *It shows statuses in Short format while fugitive shows in Normal format. Short format is a friend for user who used to git*

- The following actions are available in the staging buffer
  - `--` - Toggle status (staged / unstaged)
  - `-a`, `-r` - git add or git reset
  - `ee`, `dd` - Edit, diff the file
  - `ss` - Open a special diff buffer to solve conflicts
  - `cc`, `cA`, `cC` - Open gita:commit buffer

---
# Unfavorable points of Gstatus
.center[![fugitive Gstatus](img/fugitive_Gstatus.png)]

---
# Unfavorable points of Gstatus
.left-column[.center[![fugitive Gstatus](img/fugitive_Gstatus.png)]]
.right-column[
- The output of `git status` is a bit redundant <br>
  *It is good for beginners but not for professionals*
]

--

.right-column[
- The order of files will be changed after you stage / unstage a file<br>
*You may lost which file you just staged*
]

--

.right-column[
- No options? You may feel it is a really unfavorable behavior when you have a repository which has abundant submodules<br>
*I quickly checked help and couldn't find it. So the way may exist*
]

---
# Advantage of Gita status
.center[![gita status](img/gita_status.png)]]

---
# Advantage of Gita status
.left-column[.center[![gita status](img/gita_status.png)]]
.right-column[
- It use the Short format, friendly for professionals<br>
  *In case, gita provides a cheat sheet for beginners. Hit `?s` to display it*
]

--
.right-column[
- The file order won't change even after you staged / unstaged files<br>
  *Toggle, toggle, toggle*
]

--

.right-column[
- Several options of `git status` are available. E.g. you can improve the response with `--ignore-submodules` for a repository which has abundant submodules<br>
  *The options can be specified via global variables or command arguments*
]

---
layout: true
class: center, middle
---
<video controls src="img/gita_status_50k.webm"></video>
---
# Very **benri**

.footnote[benri &#8776; useful]
