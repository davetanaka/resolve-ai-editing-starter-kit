# DaVinci Resolve × AI 編集 スターターキット

YouTube チャンネル「デイブ」の動画「【DaVinci Resolve 21.2 × AI × Blackmagic Cloud】コーディング不要のAI自動＆リモート編集を徹底解説！」で紹介した、**AI と一緒に DaVinci Resolve で編集するやり方**を、あなたの手元で始めるためのキットです。

DaVinci Resolve 公認トレーナーのデイブ田中が、実際の動画づくり（撮影 → AI が粗編集とテロップ → 人が仕上げる）で使っている決まりを、AI に読ませられる形にまとめました。コードは1行も書かなくて大丈夫です。スクリプトが要る作業は、レシピ（docs/10）を渡せば、あなたのAIがあなたの環境に合わせて書きます。

- 撮った時点の環境：DaVinci Resolve Studio 21.2（Build 5）／Claude Code（Claude の Max プラン）／Mac
- 情報は 2026年11月時点のものです

---

## 始め方（3ステップ）

### 1. このキットを、自分の作業用フォルダに置く

- GitHub の使い方が分かる人：このリポジトリを fork かダウンロードして、自分用のリポジトリにする
- 分からない人：右上の「Code ＞ Download ZIP」で落として、好きな場所に解凍する（例：`書類/動画編集AI/`）

> 自分用のフォルダ（リポジトリ）にしておくと、あとで AI と決めた「自分の編集のやり方」を書き足していけます。ここが AI 編集マンの「引き継ぎノート」になります。

### 2. DaVinci Resolve と AI をつなぐ

手順は [docs/01-setup.md](docs/01-setup.md)。要点は2つだけです。

- DaVinci Resolve **Studio**（有料版）の 21.2 以降を使う
- Resolve のメニュー **ファイル ＞ Setup AI Assistants** で、使っている AI を登録する

### 3. そのフォルダで AI を開いて、最初の一言を送る

Claude Code なら、ターミナルでこのフォルダに移動して `claude` と打ちます。そして、次の一言から始めてください。

```
このフォルダの README.md と CLAUDE.md と docs/ を全部読んでください。
読んだら、DaVinci Resolve につながっているかを確かめて、
私がこれから何をすればいいかを、3つまでに絞って教えてください。
まだ Resolve のプロジェクトやタイムラインは何も変更しないでください。
```

そのあとの会話の進め方は [docs/02-first-conversation.md](docs/02-first-conversation.md) にあります。

---

## 中身

| ファイル | 何が書いてあるか |
|---|---|
| [CLAUDE.md](CLAUDE.md) | AI が毎回最初に読む決まり（Resolve を安全に操作するための決まり・作業の進め方）。Claude Code はこのファイルを自動で読みます |
| [AGENTS.md](AGENTS.md) | Codex など、ほかの AI 向け（中身は CLAUDE.md と同じ） |
| [docs/01-setup.md](docs/01-setup.md) | 必要なもの・つなぎ方・つながらないとき |
| [docs/02-first-conversation.md](docs/02-first-conversation.md) | AI との会話の進め方（調べさせる → 案を見せさせる → 作らせる → 確かめさせる）とプロンプトの例 |
| [docs/03-cut-rules.md](docs/03-cut-rules.md) | カットの決まり（どこで切るか・余韻・言い直し・残すもの） |
| [docs/04-tempo.md](docs/04-tempo.md) | テンポの決まり |
| [docs/05-telop-rules.md](docs/05-telop-rules.md) | テロップの決まり（字数・行数・切る位置・表記の直し） |
| [docs/06-remote-cloud.md](docs/06-remote-cloud.md) | 出先から撮って家の AI に組ませる（Blackmagic Cloud） |
| [docs/07-screen-layout.md](docs/07-screen-layout.md) | 画面の置き方・色・音（縦長の画面、テロップの帯、音の大きさ） |
| [docs/08-transcription.md](docs/08-transcription.md) | 文字起こしの注意（抜け・日英混在・固有名詞） |
| [docs/09-my-setup.md](docs/09-my-setup.md) | 私の環境と、ここまでの道のり・決まりの育て方 |
| [docs/10-recipes.md](docs/10-recipes.md) | **AIにスクリプトを書かせるレシピ**（テロップを自動で置く・粗編集・左上のラベル・図と顔の配置・点検） |

## 大事な考え方

- **AI に全部任せない**。AI は大きく組むのが得意、人は仕上げが得意です。AI が組んだタイムラインを、いつもどおり人が見て直します
- **AI はいつもの編集ソフトの中で働く**。AI が作るのは、あなたが開いて直せる DaVinci Resolve のタイムラインです。完成品の動画ファイルが急に出てくるのではありません
- **決まりは育てるもの**。ここに書いたのは私の決まりです。あなたの編集のやり方（テロップの書式・よく使う素材・切り方の好み）を、AI と話しながら CLAUDE.md や docs/ に書き足していってください。使うほど、あなた専属の編集マンになっていきます

## 注意

- 自己責任でお使いください。作業の前に、プロジェクトのバックアップを取ってください
- DaVinci Resolve や AI の更新で、操作の結果が変わることがあります
- 質問は動画のコメント欄へ。AI 活用のご相談は、動画の概要欄の問い合わせ先からどうぞ

---

DaVinci Resolve、Blackmagic Cloud、Blackmagic Camera は Blackmagic Design の商標です。Claude、Claude Code は Anthropic の商標です。このキットは個人が作ったもので、各社の公式のものではありません。

## ライセンス

このキットの文書は [クリエイティブ・コモンズ 表示 4.0 国際（CC BY 4.0）](https://creativecommons.org/licenses/by/4.0/deed.ja) で公開しています。出典（デイブ田中／YouTube チャンネル「デイブ」）を表示すれば、自由に使い回したり、書き換えたりしてかまいません。全文は [LICENSE](LICENSE) にあります。
