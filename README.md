# DaVinci Resolve × AI編集 スターターキット

YouTubeチャンネル「デイブ」の動画「【DaVinci Resolve 21.2 × AI × Blackmagic Cloud】コーディング不要のAI自動＆リモート編集を徹底解説！」で紹介した、**AIと一緒にDaVinci Resolveで編集するやり方**を、あなたの手元で始めるためのキットです。

> **β版・作者の実践例です**。私（デイブ田中）がDaVinci Resolve Studio 21.2（Build 5）・Mac・Claude Codeで確かめた範囲で書いています。自己責任で、必ず控えを取ってからお使いください

**これは完成品ではありません。あなたのAIと一緒に育てていく「芯（コア）」です。**

DaVinci Resolve公認トレーナーのデイブ田中が、実際の動画づくり（撮影 → AIが粗編集とテロップ → 人が仕上げる）で使っている決まりを、AIに読ませられる形にまとめました。でも、ここにあるのは私の好みです。あなたが使って、直して、その直しをAIに決まりとして書き足してもらう。それを繰り返すうちに、このフォルダが**あなた専属のAI編集マンの「引き継ぎノート**」になっていきます。

```
使う → あなたが直す → AIが「決まりに足す案」を出す → あなたがOK → 次からAIが最初からそうする
```

中身は3つの層に分けてあります。

| 層 | ファイル | 変えるか |
|---|---|---|
| 安全の決まり | AGENTS.md | 変えない（AIにResolveを壊させないための決まり） |
| 作例 | docs/ | 参考にする（私の好み。合わなければ読み替える） |
| **あなたの決まり** | **MY_RULES.md** | **ここを育てる** |

コードは1行も書かなくて大丈夫です。スクリプトが要る作業は、レシピ（docs/10）を渡せば、あなたのAIがあなたの環境に合わせて書きます。育て方の頼み方は[docs/11-grow.md](docs/11-grow.md)にあります。

- 撮った時点の環境：DaVinci Resolve Studio 21.2（Build 5）／Claude Code（ClaudeのMaxプラン）／Mac
- 情報は2026年11月時点のものです

---

## 始め方（4ステップ）

### 1. このキットを、自分の作業用フォルダに置く

- GitHubの使い方が分かる人：このリポジトリをforkかダウンロードして、自分用のリポジトリにする
- 分からない人：右上の「Code ＞ Download ZIP」で落として、好きな場所に解凍する（例：`書類/動画編集AI/`）

> 自分用のフォルダ（リポジトリ）にしておくと、あとでAIと決めた「自分の編集のやり方」を書き足していけます。ここがAI編集マンの「引き継ぎノート」になります。

### 2. DaVinci ResolveとAIをつなぐ

手順は[docs/01-setup.md](docs/01-setup.md)。要点は2つだけです。

- DaVinci Resolve **Studio**（有料版）の21.2以降を使う
- Resolveのメニュー**ファイル ＞ Setup AI Assistants**で、使っているAIを登録する

### 3. そのフォルダでAIを開いて、最初の一言を送る

ターミナルでこのフォルダに移動して、Claude Codeなら`claude`、Codexなら`codex`と打ちます。どちらのAIも、このフォルダの決まり（AGENTS.md）を自動で読みます。そして、次の一言から始めてください。

```
このフォルダのREADME.md・AGENTS.md・MY_RULES.mdと、docs/01-setup.mdを読んでください。
読んだら、DaVinci Resolveにつながっているかを確かめて、
docs/01の「安全な5分テスト」を、練習用のプロジェクトで一緒に進めてください。
まだ本番のプロジェクトやタイムラインは何も変更しないでください。
```

そのあとの会話の進め方は[docs/02-first-conversation.md](docs/02-first-conversation.md)にあります。

### 4. 作業の終わりに、決まりを1つ育てる

AIに頼んで、あなたが直したら、最後にこう送ってください。これが、このキットのいちばん大事な使い方です。

```
今日の作業で、私が直した所を見て、
決まりに書き足すとよさそうなことを、3つまでに絞って案を出してください。
書き足すのは、私がOKと言ってからにしてください。
```

詳しくは[docs/11-grow.md](docs/11-grow.md)。

---

## 中身

| ファイル | 何が書いてあるか |
|---|---|
| [AGENTS.md](AGENTS.md) | **安全の決まり**（既定で禁止の操作・本番の前の控え・作業の進め方）。Codexなどはこのファイルを自動で読みます |
| [CLAUDE.md](CLAUDE.md) | Claude Code用の入口。中身はAGENTS.mdを読み込む1行だけです |
| [MY_RULES.md](MY_RULES.md) | **あなたの決まり**。ここを育てます（最初は空っぽ） |
| [docs/01-setup.md](docs/01-setup.md) | 必要なもの・つなぎ方・つながらないとき |
| [docs/02-first-conversation.md](docs/02-first-conversation.md) | AIとの会話の進め方（調べさせる → 案を見せさせる → 作らせる → 確かめさせる）とプロンプトの例 |
| [docs/03-cut-rules.md](docs/03-cut-rules.md) | カットの決まり（どこで切るか・余韻・言い直し・残すもの） |
| [docs/04-tempo.md](docs/04-tempo.md) | テンポの決まり |
| [docs/05-telop-rules.md](docs/05-telop-rules.md) | テロップの決まり（字数・行数・切る位置・表記の直し） |
| [docs/06-remote-cloud.md](docs/06-remote-cloud.md) | 出先から撮って家のAIに組ませる（Blackmagic Cloud） |
| [docs/07-screen-layout.md](docs/07-screen-layout.md) | 画面の置き方・色・音（縦長の画面、テロップの帯、音の大きさ） |
| [docs/08-transcription.md](docs/08-transcription.md) | 文字起こしの注意（抜け・日英混在・固有名詞） |
| [docs/09-my-setup.md](docs/09-my-setup.md) | 私の環境と、ここまでの道のり・決まりの育て方 |
| [docs/10-recipes.md](docs/10-recipes.md) | **AIにスクリプトを書かせるレシピ**（テロップを自動で置く・粗編集・左上のラベル・図と顔の配置・点検） |
| [docs/11-grow.md](docs/11-grow.md) | **キットを育てる**（作業の終わりの一言・自分の書式を覚えさせる・合わない決まりを直す・月1回の見直し） |
| [docs/12-recovery.md](docs/12-recovery.md) | 失敗したときの戻し方（止め方・控えからの戻し方） |
| [docs/13-glossary.md](docs/13-glossary.md) | 用語集（MCP・DRT・.drp・SRT・Text+・プロキシなど） |

## 大事な考え方

- **AIに全部任せない**。AIは大きく組むのが得意、人は仕上げが得意です。AIが組んだタイムラインを、いつもどおり人が見て直します
- **AIはいつもの編集ソフトの中で働く**。AIが作るのは、あなたが開いて直せるDaVinci Resolveのタイムラインです。完成品の動画ファイルが急に出てくるのではありません
- **決まりは育てるもの（いちばん大事）**。ここに書いたのは私の決まりです。合わないものは書き換え、あなたの編集のやり方（テロップの書式・よく使う素材・切り方の好み）を、AIと話しながらMY_RULES.mdに書き足していってください。使うほど、あなた専属の編集マンになっていきます（docs/11）

## 注意

- 自己責任でお使いください。本番で使う前に、docs/01の「安全な5分テスト」をして、AGENTS.mdの「本番の前の控え」（プロジェクトの複製・.drp・DRT）を取ってください
- DaVinci ResolveやAIの更新で、操作の結果が変わることがあります
- 質問は動画のコメント欄へ。AI活用のご相談は、動画の概要欄の問い合わせ先からどうぞ

---

DaVinci Resolve、Blackmagic Cloud、Blackmagic CameraはBlackmagic Designの商標です。Claude、Claude CodeはAnthropicの商標です。このキットは個人が作ったもので、各社の公式のものではありません。

## ライセンス

このキットの文書は[クリエイティブ・コモンズ 表示4.0国際（CC BY 4.0）](https://creativecommons.org/licenses/by/4.0/deed.ja)で公開しています。出典（デイブ田中／YouTubeチャンネル「デイブ」）を表示すれば、自由に使い回したり、書き換えたりしてかまいません。全文は[LICENSE](LICENSE)にあります。
