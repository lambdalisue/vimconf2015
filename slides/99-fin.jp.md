layout: true
---
# まとめ
- vim-gita の使い方

--

  - `Gita status` でステージ

--

  - `cc` でコミットメッセージ編集して `:q` でコミット

--

  - `Gita diff-ls` で変更があったファイルを一覧

--

  - `Gita diff`, `Gita file`, `Gita browse`, あと `Gita blame` で git と戯れる

--

.large.center[まだ **vim-fugitive** をおすすめします<br>**全体的な完成度は完全に負けてます**]

---
# じょーほー

NeoBundle を使うと vim-gita が簡単にインストールできます

```vim
NeoBundleLazy 'lambdalisue/vim-gita', {
    \ 'external_command': 'git',
    \ 'autoload': {
    \   'commands': 'Gita',
    \ },
    \}
```

もしくは https://github.com/lambdalisue/vim-gita にあるので頑張ってください

あと今回のスライドは https://lambdalisue.github.io/vimconf2015 で見れます

---
class: center, middle
# Questions?

