# 01 つなぎ方

## 必要なもの

| もの | 説明 |
|---|---|
| **DaVinci Resolve Studio**（有料版） | 21.1 から、外の AI やスクリプトで Resolve を動かすには Studio が必要になりました。無料版ではできません。このキットは 21.2 で確かめています |
| **AI** | 私は Claude Code を使っています（Claude の Pro プランからでも始められます）。Resolve は Codex、Google Antigravity、Grok などにもつなげられます。特定の AI に決めていないのが、DaVinci Resolve のよい所です |
| パソコン | 私は Mac で使っています。Resolve の動作環境は Blackmagic Design の公式サイトで確かめてください（AI の機能を使うなら、メモリは多めに） |
| 出先から使う場合だけ | スマホの Blackmagic Camera（無料）と Blackmagic Cloud（有料）。→ [06-remote-cloud.md](06-remote-cloud.md) |

## つなぐ手順

1. DaVinci Resolve Studio を最新版（21.2 以降）にする
2. Resolve のメニュー **ファイル ＞ Setup AI Assistants** を開き、使っている AI を選んで登録する
3. AI を起動する（Claude Code なら、このキットを置いたフォルダで `claude`）
4. 「DaVinci Resolve につながってる？ いま開いているプロジェクトの名前を教えて」と聞く。名前が返ってくれば、つながっています

## つながらないとき

- **Resolve が起動しているか**：AI は、起動している Resolve に話しかけます。先に Resolve を開いておく
- **Claude Code の場合**：`/mcp` と打って DaVinci Resolve を選び、接続し直す。それでもだめなら、Claude Code を一度終了して起動し直す
- **Resolve を更新した直後**：Setup AI Assistants の登録を、もう一度やり直す
- **画面にダイアログ（確認の窓）が出ていないか**：Resolve に確認の窓が開いていると、AI からの操作が効かないことがあります。窓を閉じてから頼み直す

## どういう仕組みか（知っておくと会話がうまくいく）

- AI は Resolve の**外**にいます。Resolve の中にチャットの欄が増えたのではありません。Resolve が「外の AI が操作できる入口（MCP という仕組み）」を開けていて、AI はそこから Resolve を動かします
- 21.2 からは、AI が**コマを書き出して、自分で画面を見て確かめられる**ようになりました。「並べた → 本当に思ったとおりに並んだか見る」まで AI ができるので、任せられる範囲が広がりました
- AI は、Resolve に入っている「スクリプトの API の説明」や「新しい機能の説明」を自分で読めます。知らない機能があっても、推測で動かずに調べてから使うよう、CLAUDE.md で頼んであります
