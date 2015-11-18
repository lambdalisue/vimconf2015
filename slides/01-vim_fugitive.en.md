class: invert
### Topic 1
# fugitive was not for me
---
You may have seen
## .highlight[E492: Not an editor command: Gstatus]
while using fugitive, it is a bit annoying isn't it?
---
layout: true
---
# When do you see
1. Execute the command in a directory outside of a git repository<br>
  .subtle[It is fair enough while you are not in a git repository]
2. The current directory is in a git repository but the current buffer is a non file buffer<br>
  .subtle[Like VimFiler, quickfix, or whatever. You have to open an actual file to enable fugitive]
3. Somehow, really somehow<br>
  .subtle[This is most annoying case. Even E429 is not appeared, fugitive often fail to recognize a correct git repository]
---
layout: true
class: center, middle
---
Wow, It is so critical
## .highlight[I would fix it and send PRs to tpope]
I thought. Until I checked the source code...
---
.w100[![vim-fugitive](img/vim-fugitive-01.png)]

Hum... where is the `autoload` directory?
---
.w100[![vim-fugitive](img/vim-fugitive-02.png)]

.highlight[Oh... There is a single file...]
---
.w100[![vim-fugitive](img/vim-fugitive-03.png)]

.highlight[Well... 3049 lines...]
---
layout: true
---
# After I checked the source code

1. I really .highlight[surprised] that tpope can maintain this .highlight[complicated] code<br>
  .subtle[While the repository have so may contributers, the code is quite complicated]
2. It seemed there are several .highlight[hard written parts]<br>
  .subtle[I just quickly checked so might be wrong but it seemed several features are non customizable]
3. .highlight[No test], mean that tests are performed by users in the product<br>
  .subtle[It makes "refactoring" really difficult to perform]
---
layout: true
class: center, middle
---
# Ok
---
# Let's make .highlight[an another one]
---
This was a story why I made a new git manipulation plugin called
# .highlight[vim-gita]
I would like to introduce you about this plugin today.
---
Ok now. Let's start my topic
## "Things I .highlight[actually] desired"
---
class: center, middle
# .highlight[CAUTION]

# UNDER DEVELOPMENT

It is under development and still contains critical bugs.

Any change would be applied without any announcement.

Any feature shown in this slide would not work in future.

Please DO NOT send me pull request while<br>
any contribution on this plugin would be lost in future.
