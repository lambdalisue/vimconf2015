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

"Which one should I stage? Check it with `gita status`..."

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

.center.middle.highlight.huge[So many! So long！]

---
layout: true
class: center, middle
---
When you edit a lot of files and need to call `git add` .highlight[individually]
## Can you be bothered to do that?
Or you may call `git add .` to mix everything into a single commit :-p
---
# Then
---
# .highlight[Gita status]
---
layout: true
---
# Gita status ?

- An alternative of `Gstatus` in fugitive<br>
  .subtle[It shows statuses in *Short format* while fugitive shows in *Normal format*. *Short format* is a friend for user who used to git]
- The following actions are available in the staging buffer.
  - `--` - Toggle status (staged / unstaged)
  - `-a`, `-r` - git add or git reset
  - `ee`, `dd` - Edit, diff the file
  - `ss` - Open a special diff buffer to solve conflicts
  - `cc`, `cA`, `cC` - Open gita:commit buffer
---
# Unfavorable points of Gstatus
.absolute[.center.w100[![fugitive Gstatus](img/fugitive_Gstatus.png)]]
---
# Unfavorable points of Gstatus
.absolute.transparent[.center.w100[![fugitive Gstatus](img/fugitive_Gstatus.png)]]
- The output of `git status` is a bit redundant <br>
  .subtle[It is good for beginners but beginners never being a beginner]

--

- The order of files will be changed after you stage / unstage a file<br>
  .subtle[You may lost which file you just staged.]

--

- It is not possible to specify options of `git status`. You may feel it is a really unfavorable behavior when you have a repository which has abundant submodules<br>
  .subtle[I quickly checked help and couldn't find it. I'm sorry if there is a way]
---
# Advantage of Gita status
.absolute[.center.w100[![gita status](img/gita_status.png)]]
---
# Advantage of Gita status
.absolute.transparent[.center.w100[![gita status](img/gita_status.png)]]
- It use *Short format*, friendly for professionals<br>
  .subtle[It provides a cheat sheet for beginners. Hit `?s`]

--

- The file order won't change even after you staged / unstaged files<br>
.subtle[Recently implemented. You can toggle as you much :-)]

--

- Several options of `git status` are available in `Gita status` command. You can improve the response with `--ignore-submodules` for a repository which has abundant submodules<br>
  .subtle[The options can be specified via global variables or command arguments]
---
layout: true
class: center, middle
---
<video controls style="width: 100%">
  <source src="img/gita_status.webm">
</video>
---
# Very .highlight[benri (useful)]

