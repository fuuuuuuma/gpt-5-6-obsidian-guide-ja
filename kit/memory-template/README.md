# Obsidian × Codex 記憶構造テンプレート

CodexがVaultを読み書きし、人もObsidianから同じ内容を確認できる最小テンプレートです。 フォルダを増やすことではなく、**入力 → 根拠 → 判断 → 制作 → 振り返り**を一周させるために使います。

## 最初にすること

1. このフォルダを複製し、ObsidianでVaultとして開く
2. `AGENTS.md`の`[ ]`部分を自分の運用へ合わせる
3. `40_Memory/User.md`と`Business.md`へ、長く変わらない情報だけを書く
4. `99_Templates/Project.md`から、現在進行中の仕事を一つ作る
5. Codexで、このVault直下を作業場所として開く
6. 自動編集前にGit、Sync履歴、外部バックアップなど復元手段を用意する

## 構造

```text
.
├── AGENTS.md
├── HOME.md
├── 00_Inbox/
├── 01_Daily/
├── 02_Knowledge/
├── 03_MOCs/
├── 10_Projects/
├── 20_Areas/
├── 30_Rules/
├── 40_Memory/
├── 50_Outputs/
├── 90_Archive/
└── 99_Templates/
```

## 運用原則

- `AGENTS.md`は短い入口にする
- 詳細な知識は別ノートへ置き、入口からリンクする
- Raw、Source、Knowledge、Outputを区別する
- 事実、推測、提案を区別する
- Projectの進捗を長期Memoryへ混ぜない
- Memoryへの昇格は週次レビューで人が決める
- 自動編集の前に差分と復元手段を確認する

## 最初の一周

1. InboxまたはSourceへ材料を置く
2. Knowledgeへ一つの主張として整理する
3. MOCから関連ノートへ道を作る
4. Projectで目的と完成条件を決める
5. Outputを作る
6. Decision、Feedback、Failure候補を人が選ぶ
7. 週次レビューでArchiveとMemoryを整理する
