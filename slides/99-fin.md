layout: true
---
# まとめ
- vim-gita の流れ

--

  - `Gita status` でステージング

--

  - `cc` でコミット編集

--

  - `:q` でコミット

--

  - `Gita diff-ls` で変更ファイルの確認

--

  - `Gita diff`, `Gita file`, `Gita browse` や `Gita blame` で git と戯れる

--

.center[まだまだ開発中ですが fugitive に疲れた方は<br>.highlight[自己責任]でお試しください]

---
# 雑多なこと

NeoBundle でインストールする場合は以下のようにしてください (Lazy でインストール可能！）

```vim
NeoBundleLazy 'lambdalisue/vim-gita', {
    \ 'external_command': 'git',
    \ 'autoload': {
    \   'commands': 'Gita',
    \ },
    \}
```

もしくは https://github.com/lambdalisue/vim-gita を見てみてください。

あと、このスライドは https://lambdalisue.github.io/vimconf2015 で見ることができます
---
class: center, middle
# しつもん、ある？
