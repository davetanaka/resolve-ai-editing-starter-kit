# 更新の記録

DaVinci ResolveやAIの更新で、操作の結果が変わることがあります。どの版で、どの環境で確かめたかを、ここに残していきます。GitHubのタグ（v1・v2 …）も同じ区切りです。

## v2.2.1（2026-11-15）
- docs/06：「Blackmagic Cloudが運ぶのは素材だけ」を直した。Cloudはプロジェクトの共有も受け持つ（Blackmagic Cloud の公式の説明に合わせた）
- 確かめた環境：v2と同じ。文書だけの直し

## v2.2（2026-11-15）
- 自分の決まりを書く先を、MY_RULES.mdにそろえた（README・docs/02・03・04・11とAGENTS.mdに、docs/を書き換えさせる書き方が残っていた）
- AGENTS.md：安全の決まりは好みを理由に外さない、と書いた。強い権限のスクリプトを使う前に、コードを読まない人でも判断できる要約を見せる、と書いた
- docs/10：粗編集の確かめ方を、コマではなく音付きで聞く形に直した
- docs/11：新しい版に入れ替えるときの手順を足した（上書きするとMY_RULES.mdが消えるため）
- docs/06：素材の道と指示の道の図と、出かける前のテストを足した
- docs/01：確かめた範囲（21.2 Build 5・Claude Code）を超える書き方を直した
- README：質問のときの書き方を足した
- 確かめた環境：v2と同じ（DaVinci Resolve Studio 21.2 Build 5・Mac・Claude Code）。今回は文書だけの直しで、操作の確認はしていない

## v2.1（2026-11-15）
- READMEに動画のURLを入れた
- 育てたMY_RULES.mdの例を足した（[examples/MY_RULES_example.md](examples/MY_RULES_example.md)）
- docs/06に、スマホから家のAIを動かす「私の例」を書いた
- この更新の記録を足した
- 確かめた環境：v2と同じ（DaVinci Resolve Studio 21.2 Build 5・Mac・Claude Code）

## v2（2026-11-15）
- 安全の決まりを強めた（既定で禁止の操作・本番の前の控え・安全な5分テスト）
- MY_RULES.mdで自分の決まりを育てる形にした（3つの層）
- Codexでも同じ決まりで動くようにした
- 戻し方（docs/12）と用語集（docs/13）を足した
- 確かめた環境：DaVinci Resolve Studio 21.2 Build 5・Mac・Claude Code

## v1（2026-11-14）
- 初版
