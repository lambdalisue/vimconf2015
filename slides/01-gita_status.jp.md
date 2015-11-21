layout: true
---
class: center, middle, invert
### Topic 3
# ステージ or アンステージ
---
# けーすすたでぃー

--

「うし、終わった。えーっとどれをステージすればいいんだっけか……」

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
        modified:   foo/bar/hoge/……/piyo/puyo/myo.pl
        modified:   foo/bar/hoge/……/piyo/puyo/eyo.pl
        ...
```
--

.center.middle.huge[**So many! So long!**]

---
layout: true
class: center, middle
---
たくさんファイルを修正して**個別**に `git add` するの
## とてつもなく面倒くさくないですか？
面倒臭すぎて `git add .` やる方も多いかと思います
---
# そこで
---
# **Gita status**
---
layout: true
---
# Gita status ?

- fugitive の `Gstatus` みたいなやつです<br>
  *Gstatus は Normal format で表示しますが、こいつは Short format で表示します。プロには嬉しい仕様*

- 下記のアクションが有効になってます
  - `--` - 状態トグル
  - `-a`, `-r` - git add とか git reset
  - `ee`, `dd` - 編集とか diff とか
  - `ss` - Conflict 解決用 diff の表示とか
  - `cc`, `cA`, `cC` - コミットバッファ開く

---
# Gstatus の辛いところ
.center[![fugitive Gstatus](img/fugitive_Gstatus.png)]

---
# Gstatus の辛いところ
.left-column[.center[![fugitive Gstatus](img/fugitive_Gstatus.png)]]
.right-column[
- `git status` 出力そのままなので冗長<br>
  *初心者にはいいですが、初心者は成長するので……*
]

--

.right-column[
- ステージしたりするとファイルの順番が変わる<br>
  *どれステージしたか全然わからなくなる*
]

--

.right-column[
- オプション指定不可？サブモジュール地獄のリポジトリだととても辛い<br>
*ちゃらっとヘルプ見ただけなので指定可能だったらごめんなさい*
]

---
# Gita status の利点
.center[![gita status](img/gita_status.png)]]

---
# Gita status の利点
.left-column[.center[![gita status](img/gita_status.png)]]
.right-column[
- Short format を使うのでプロにやさしい
  *初心者のためにチートシートも用意してます。`?s` でおｋ*
]

--
.right-column[
- ステージしてもファイルの順番は変わらない<br>
  *トグルし放題ですね*
]

--

.right-column[
- いくつかのオプションをサポートしてます。例えば `--ignore-submodules` でサブモジュール地獄でも快適<br>
  *オプションはグローバル変数かコマンド引数で指定可能*
]

---
layout: true
class: center, middle
---
<video controls src="img/gita_status_50k.webm"></video>
---
# Very **benri**

.footnote[benri &#8776; useful]
