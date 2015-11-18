layout: true
---
class: center, middle, invert
### Topic 3
# 混ぜるな危険
---
# けーすすたでぃー

--

「よし、とりあえず出来た部分だけコミットしよう」

--

「WIP な変更もあるからなぁ…… `git status` っと……」

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
このように、たくさん編集した後に.highlight[個別]に `git add` するの
## とてつもなく.highlight[面倒くさくないですか？]
面倒臭すぎて `git add .` でコミット混ぜちゃう人も多いですよね
---
# そこで
---
# .highlight[Gita status]
---
layout: true
---
# Gita status ?

- vim-fugitive の `Gstatus` 相当であるステージング管理バッファ<br>
  .subtle[fugitive と違い Short format で表示されるので慣れると見やすい]
- ステージング管理バッファでは以下のアクションが可能
  - `--` による git add / git reset のトグル
  - `-a` や `-r` による git add / git reset の直接実行
  - `ee` や `dd` など対象ファイルを開くアクション
  - `ss` によるコンフリクト解決用 Diff の起動
  - `cc`, `cA`, `cC` による `Gita commit` の呼び出し<br>
  .subtle[Gita commit バッファと相互に行ったり来たり可能]
---
# Gstatus の辛いところ
.absolute[.center.w100[![fugitive Gstatus](img/fugitive_Gstatus.png)]]
---
# Gstatus の辛いところ
.absolute.transparent[.center.w100[![fugitive Gstatus](img/fugitive_Gstatus.png)]]
- `git status` の出力そのままだから冗長で縦に長い<br>
  .subtle[最初はわかりやすいかもしれないけど、使ってるうちに冗長で辛くなる]

--

- ステージングした際に対象ファイルの位置が大きくずれる<br>
  .subtle[自分がどれをステージングしたのか見失うことが多い]

--

- `git status` のオプションが指定できないので多量の submodule があるレポジトリなどは辛い<br>
  .subtle[僕が知らないだけかもしれませんが、ヘルプなど見た限りではなかった]
---
# Gita status の良いところ
.absolute[.center.w100[![gita status](img/gita_status.png)]]
---
# Gita status の良いところ
.absolute.transparent[.center.w100[![gita status](img/gita_status.png)]]
- `git status -s` の出力を利用しているので慣れると見やすい<br>
  .subtle[慣れてない人用に `?s` でチートシートが表示されます]

--

- ステージングした際に対象ファイルの位置がズレない<br>
  .subtle[最近変えた挙動です。これによりトグルし放題です]

--

- オプションが指定可能なので submodule 多量のレポジトリでは `--ignore-submodules` で高速化<br>
  .subtle[オプションはグローバル変数もしくは実行時オプションで指定可能]
---
layout: true
class: center, middle
---
<video controls style="width: 100%">
  <source src="img/gita_status.webm">
</video>
---
# とても.highlight[便利]
