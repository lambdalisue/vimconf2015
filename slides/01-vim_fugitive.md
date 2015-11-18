class: invert
### Topic 1
# fugitive じゃだめなんだ僕
---
fugitive を使っているとよく目にする
## .highlight[E492: Not an editor command: Gstatus]
とてもイライラしますね
---
layout: true
---
# どういう時に起こるか？
1. git リポジトリ以外で初めて実行した時<br>
  .subtle[これに関しては、まぁ納得できますけどね]
2. カレントディレクトリが git リポジトリだが非ファイルバッファの場合<br>
  .subtle[VimFiler などで git レポジトリに行ってもファイルを開くまでは実行できない]
3. まじよくわからないけど、なぜか出るとき<br>
  .subtle[これが辛い。E429 は出ないにせよ git リポジトリと認識してくれないことが多々]
---
layout: true
class: center, middle
---
これでは仕事にならない
## .highlight[早急に原因を突き止めて修正PRを送ろう]
そう考えていた時期が僕にもありました
---
.w100[![vim-fugitive](img/vim-fugitive-01.png)]

あれ？ `autoload` ディレクトリがない……
---
.w100[![vim-fugitive](img/vim-fugitive-02.png)]

.highlight[嫌な予感……]
---
.w100[![vim-fugitive](img/vim-fugitive-03.png)]

.highlight[3049 ライン……]
---
layout: true
---
# ソースを読んでみて

1. とりあえずよくメンテナンスできるなレベルで.highlight[ごっちゃごちゃ]<br>
  .subtle[コントリビューターが多いので仕方ないですが、今から全貌を理解するのは辛い]
2. 決め打ちが結構多くカスタマイズできない<br>
  .subtle[さらっと読んだ感じですが(上記理由から詳しく読んでない)ハードコーディングが目立ちました]
2. .highlight[一切のテストが無い]のでテストは人海戦術<br>
  .subtle[気軽にリファクタリングもできません。なので全貌把握も困難です]
---
layout: true
class: center, middle
---
# よし
---
# .highlight[新しく]作ろう！
---
このような経緯で誕生した git 操作プラグイン
# .highlight[vim-gita]
本日はこのプラグインの機能紹介を行います。
---
ということで
## ぼくが.highlight[ほんとうに]ほしかったもの
のはっぴょうをさせていただきます
---
class: center, middle
# .highlight[警告]

# 開発中

これは開発中のものです。まだ様々なバグを含んでおります。

機能削除を含むあらゆる仕様変更は一切アナウンスされません。

紹介している機能は将来的に使えなくなる可能性があります。

プルリクエストなどはしないでください<br>
仕様変更により該当コードが失われる可能性があります。
