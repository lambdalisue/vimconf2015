---
layout: true
class: center, middle
---
`git grep` 使ってますか？
---
layout: true
---
## `git grep` の利点

- 必要なソフトは git だけ<br>
  .subtle[近年は (大人の事情を除けば) プロジェクトは git 管理が多いので、とくに何も考えなくても `git grep` を使うための最低条件は揃っている]

- マルチバイト文字の対応<br>
  .subtle[速度を売りにしている grep 系ソフトウェアは結構ありますが、マルチバイト対応をしっかり行っているものは少ない]

- 圧倒的速度<br>
  .subtle[git レポジトリに登録されたものから検索するので他の grep 系コマンドと違い爆速]

---
## Vim と `git grep`

1. ターミナルに戻る or ターミナルを起動する<br>
  .subtle[もしくは VimShell を開く？]

2. `git grep` で検索をかける<br>
  .subtle[結果は普通 less などのページャーで表示されるので `q` 押して終了とかする]

3. 検索結果を元に `vim ほにゃらら` で Vim を起動 もしくは `:e ほにゃらら` で開く<br>
  .subtle[Bash や Zsh の補完大活躍。でも似た名前があると結構面倒]
--
<br>
<br>
.center[普段上の手順を踏んでいるなら<br>.large.highlight[`Unite grep/git`]<br> が貴方に降り注ぐ太陽になります！]
---
## Unite grep/git とは

- Shougo さん作の Unite で `git grep` をするソース<br>
  .subtle[Shougo ウェアは Vimmer の常識]

- `git grep` による一次スクリーニングおよび Unite による二次スクリーニングが可能<br>
  .subtle[大量のソースコードから素早く該当コードを探すのに最適]

- 最近 Unite 本体に取り込まれたので特に何もしなくても使える<br>
  .subtle[以前は `lambdalisue/unite-grep-vcs` として配布していました]
---
# Unite grep/git の動作デモ

.center[<video src="img/unite_grep_git.mp4"></video>]
--
.overrap.center.middle.huge.highlight[
<br>
<br>
<br>
<br>
便利
]
