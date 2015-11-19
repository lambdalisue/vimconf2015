class: invert
### Topic 1
# fugitive was not for me
---
You may have seen
## **E492: Not an editor command: Gstatus**
while using fugitive, it is a bit annoying isn't it?
---
layout: true
---
# When do you see
1. Execute the command in a directory outside of a git repository<br>
  *It is fair enough while you are not in a git repository*

2. The current directory is in a git repository but the current buffer is a non file buffer<br>
  *Like `VimFiler`, `quickfix`, or whatever. You have to open an actual file to enable fugitive*

3. Somehow, really somehow<br>
  *This is most annoying case. Even `E429` is not appeared, fugitive often fail to recognize a correct git repository*

---
layout: true
class: center, middle
---
Wow, It is so critical
## **The world want me to fix it and send PRs**
I thought. Until I checked the source code...
---
![vim-fugitive](img/vim-fugitive-01.png)

Hum... where is the `autoload` directory?

---
![vim-fugitive](img/vim-fugitive-02.png)

One file... Well...

---
![vim-fugitive](img/vim-fugitive-03.png)

**3049 lines...**

---
layout: true
class: center, middle
---
# Ok
---
# Let's make **an another one**
---
Most of the reasons were omitted but this was a story why I made
# **vim-gita**
I would like to introduce you about this plugin today.

---
Ok now. Let's start my topic
## "Things I **actually** want"

---
class: center, middle
# **CAUTION**

# UNDER DEVELOPMENT

It is under development and still contains critical bugs.

Any change would be applied without any announcement.

Any feature shown in this slide would not work in future.

Please DO NOT send me pull request while<br>
any contribution on this plugin would be lost in future.
