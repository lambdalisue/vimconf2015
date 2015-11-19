layout: true
---
# Summary
- Flow of using vim-gita

--

  - Stage files via `Gita status`

--

  - Edit a commit message via `cc`

--

  - Commit via `:q`

--

  - Confirm changed files via `Gita diff-ls`

--

  - Play git with `Gita diff`, `Gita file`, `Gita browse`, or `Gita blame`

--

.large.center[Try it with **your own responsibility** :-)]

---
# Information

You can install vim-gita via NeoBundle as

```vim
NeoBundleLazy 'lambdalisue/vim-gita', {
    \ 'external_command': 'git',
    \ 'autoload': {
    \   'commands': 'Gita',
    \ },
    \}
```

Or visit https://github.com/lambdalisue/vim-gita

And you can read this slide in https://lambdalisue.github.io/vimconf2015

---
class: center, middle
# Questions?

