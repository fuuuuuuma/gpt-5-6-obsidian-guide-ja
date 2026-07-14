# Obsidian × Codex 記憶構造テンプレート

以下は配布フォルダに含まれる実用ファイルです。ファイル見出しのパスに合わせて保存すると、Vaultの土台として使えます。

## .gitignore

```text
.DS_Store
.obsidian/workspace*.json
.trash/
*.env
.env*
secrets/
```

## 00_Inbox/README.md

```markdown
# Inbox

保存先を決める前の一時置き場。週次レビューで次のいずれかへ移す。

- 今日だけの記録 → `01_Daily`
- 長く使う一つの論点 → `02_Knowledge`
- 期限と成果物がある仕事 → `10_Projects`
- 継続領域 → `20_Areas`
- 再利用する判断・指摘・失敗 → `40_Memory`
- 不要 → 削除候補として人へ確認

Inboxを長期保管庫にしない。
```

## 01_Daily/README.md

```markdown
# Daily Notes

`YYYY-MM-DD.md`で作成する。気づき、作業記録、未整理の考えを低い摩擦で残す場所。

Dailyへ書いた内容は、そのまま永続ルールにしない。週次レビューで再利用価値があるものだけProject、Knowledge、Memoryへ昇格する。

テンプレート: [[99_Templates/Daily]]
```

## 02_Knowledge/README.md

```markdown
# Knowledge

1ノート1論点で、自分が理解・判断した内容を置く。

良いタイトルは、本文を開く前に主張や問いが分かる。

- 広すぎる: `AIについて.md`
- 読みやすい: `外部記憶は保存と参照を分けて考える.md`

本文には要点、自分の解釈、使う条件、使わない条件、出典、確認日、関連Projectを置く。

テンプレート: [[99_Templates/Knowledge]]
```

## 03_MOCs/README.md

```markdown
# MOCs

MOC（Map of Content）はテーマ別の判断地図。リンク一覧だけでなく、読む順番、対象者、採用する論点、矛盾、未確認事項を書く。

例:

```markdown
# YouTube制作 MOC

## 初めて読む
- [[視聴者の課題]]
- [[チャンネルの価値提案]]

## 企画時に読む
- [[過去動画の重複チェック]]
- [[一次情報の確認ルール]]

## 現在の論点
- AとBは前提が異なる。今回の動画ではAを採用する。
```
```

## 10_Projects/README.md

```markdown
# Projects

期限、成果物、完了条件がある仕事を置く。Projectノートは人とAIの共通の引き継ぎ書にする。

各Projectに含める項目:

- 目的と対象者
- 成果物と保存先
- やること / やらないこと
- 参照Source / Knowledge / MOC
- 決定済み
- 現在地
- 次の一手
- 確認待ち
- 完了条件

終了したProjectは`90_Archive`へ移し、再利用するDecisionだけMemoryへ残す。

テンプレート: [[99_Templates/Project]]
```

## 20_Areas/README.md

```markdown
# Areas

期限のない継続領域を置く。例: YouTube、X、商品、学習、健康、顧客対応。

Areaには次を置く。

- 維持する基準
- 現在の状態
- 関連するMOCとProject
- 定期レビューの頻度

成果物をArea内へ積み上げず、完成物は`50_Outputs`へ置く。
```

## 30_Rules/Publishing.md

```markdown
# Publishing

外部へ出る台本、スライド、投稿下書きの確認項目。

- [ ] 事実、推測、提案を区別した
- [ ] 最新仕様・料金・規約を公式情報で確認した
- [ ] 出典URLと確認日を残した
- [ ] 効果を保証する表現を避けた
- [ ] 第三者の字幕・記事を長く転載していない
- [ ] 個人情報・秘密情報・内部パスを除いた
- [ ] チャンネルやブランドの方針に合う
- [ ] 公開・投稿は人が最終確認する
```

## 30_Rules/Security.md

```markdown
# Security

## 保存しない情報

- APIキー、トークン、パスワード、秘密鍵
- 契約上保存できない顧客情報
- 公開範囲が不明な個人情報

## AIに読ませる前

- 利用するモデルとサービスのデータ取り扱いを確認する
- 公開情報、社内情報、機密情報を区分する
- 必要な範囲だけを作業フォルダへ置く

## 変更前

- 大量編集はテストVaultまたは小さな範囲で試す
- Git、Sync履歴、外部バックアップなど復元手段を用意する
- 削除と上書きは人へ確認する

## Community Plugins

- Restricted Modeから始める
- 目的、配布元、更新状況、権限を確認する
- 一度に複数導入せず、問題発生時に切り分けられるようにする
```

## 40_Memory/Business.md

```markdown
# Business

## Purpose

- [誰に、どんな価値を届けるか]

## Products / Channels

- [商品・サービス・チャンネル]

## Audience

- [対象者、困りごと、前提知識]

## Principles

- [継続して守る判断基準]

## Metrics

- [見る指標と、見ない指標]

## Sources

- [公式資料や事業計画へのリンク]
```

## 40_Memory/Decisions.md

```markdown
# Decisions

## 記録形式

### YYYY-MM-DD — [判断]

- Decision:
- Why:
- Alternatives:
- Evidence:
- Owner:
- Revisit when:
- Related project:

## Records

<!-- 新しい判断を上へ追加。前提が変わったら現行状態を明記する。 -->
```

## 40_Memory/Failures.md

```markdown
# Failures

同じ失敗を再発させないための記録。単なるエラーログではなく、原因と再発防止まで書く。

## 記録形式

### YYYY-MM-DD — [失敗パターン]

- Symptom:
- Cause:
- Fix:
- Prevention:
- Scope:
- Verified by:
- Related project:

## Records

<!-- 新しい失敗パターンだけを追加する。既知のものは既存項目を更新する。 -->
```

## 40_Memory/Feedback.md

```markdown
# Feedback

次回も使う具体的な指摘だけを残す。一度の好みや一時的な修正はProjectへ置く。

## 記録形式

### YYYY-MM-DD — [短いルール名]

- Context:
- Feedback:
- Apply when:
- Do not apply when:
- Example:
- Source project:

## Records

<!-- 重複した指摘は統合する。 -->
```

## 40_Memory/MEMORY.md

```markdown
# Memory Index

毎回読む可能性が高い、短い索引。詳細をここへ集約しない。

## 人と事業

- [[User]] — 安定したプロフィールと好み
- [[Business]] — 事業、顧客、商品、継続方針

## 学習履歴

- [[Decisions]] — 重要な判断と再検討条件
- [[Feedback]] — 次回も守る指摘
- [[Failures]] — 再発を防ぐ失敗パターン

## 更新ルール

- 一時的な状況はDailyまたはProjectへ置く
- 新しい情報は出典と確認日を添える
- 矛盾は追記で放置せず、現行内容を更新し履歴を残す
- 月次で重複と期限切れを整理する
```

## 40_Memory/User.md

```markdown
# User

長く変わらない情報だけを書く。

## Profile

- Name: [名前]
- Language: [日本語]
- Timezone: [Asia/Tokyo]
- Role: [役割]

## Preferences

- Communication: [結論先 / 詳細重視など]
- Working style: [朝に深い作業 / レビュー重視など]
- Avoid: [避けたい表現・進め方]

## Notes

- 期限付きの状況や今日の感情はDailyへ置く
- 推測でプロフィールを追加しない
```

## 50_Outputs/README.md

```markdown
# Outputs

人へ渡せる完成物を置く。内部版と公開版を分ける。

推奨Properties:

```yaml
type: output
status: draft
channel:
source_checked: false
approved: false
publish_date:
```

外部公開や投稿は、`30_Rules/Publishing.md`の確認後に人が行う。
```

## 90_Archive/README.md

```markdown
# Archive

終了したProject、無効になったルール、古い前提を置く。

Archiveへ移すときは、次を確認する。

- 現行ファイルから古いリンクが残っていないか
- 再利用するDecision / Feedback / FailureをMemoryへ選別したか
- 公開物と出典の関係が壊れないか
- 廃止日と理由が必要か
```

## 99_Templates/Daily.md

```markdown
---
type: daily
date: {{date:YYYY-MM-DD}}
---

# {{date:YYYY-MM-DD}}

## Focus

- （記入）

## Capture

- （記入）

## Work log

- （記入）

## Decisions made today

- （記入）

## Open loops

- [ ] （記入）

## Candidates for memory

- Decision:
- Feedback:
- Failure:

## End-of-day

- Progress:
- Blocker:
- Next:
```

## 99_Templates/Decision.md

```markdown
---
type: decision
date: {{date:YYYY-MM-DD}}
status: active
owner:
---

# [Decision]

## Context

- （記入）

## Decision

- （記入）

## Why

- （記入）

## Alternatives

- （記入）

## Evidence

- （記入）

## Consequences

- （記入）

## Revisit when

- （記入）

## Related project

- （記入）
```

## 99_Templates/Knowledge.md

```markdown
---
type: knowledge
status: draft
verified_on:
---

# [一つの主張または問い]

## Summary

- （記入）

## My interpretation

- （記入）

## Use when

- （記入）

## Do not use when

- （記入）

## Evidence

- [[Source note]]

## Counterpoints / uncertainty

- （記入）

## Related

- MOC:
- Project:
```

## 99_Templates/Output.md

```markdown
---
type: output
status: draft
channel:
source_checked: false
approved: false
publish_date:
---

# [Output title]

## Audience and purpose

- （記入）

## Content


## Source map

- Claim:
  - Source:

## Publication check

- [ ] 最新仕様・料金・規約を確認した
- [ ] 誇張表現を確認した
- [ ] 第三者コンテンツの転載を確認した
- [ ] 個人情報・秘密情報を除いた
- [ ] 人が公開を承認した
```

## 99_Templates/Project.md

```markdown
---
type: project
status: planning
owner:
channel:
due:
source_checked: false
---

# [Project name]

## Goal

- Audience:
- Outcome:
- Why now:

## Deliverables

- [ ] （成果物を記入）

## Scope

- In:
- Out:

## Constraints

- （記入）

## References

- MOC:
- Sources:
- Knowledge:

## Decisions

- （記入）

## Current state

- Completed:
- In progress:
- Blocked:

## Next action

- （記入）

## Waiting for human confirmation

- （記入）

## Done when

- [ ] 成果物が指定場所にある
- [ ] 出典とリンクを確認した
- [ ] 事実と提案を区別した
- [ ] 変更範囲を確認した
- [ ] 次回へ残す学びを選別した

## Handoff

- Summary:
- Changed files:
- Not changed:
- Verification:
- Remaining:
```

## 99_Templates/Source.md

```markdown
---
type: source
source_kind: official
author:
published:
checked: {{date:YYYY-MM-DD}}
url:
---

# [Source title]

## Why this source matters

- （記入）

## Verified facts

- （記入）

## Claims requiring caution

- （記入）

## Relevant locations

- Section / timestamp:

## My notes

- （記入）

## Related knowledge

- （記入）
```

## AGENTS.md

```markdown
# Vault共通ルール

## オーナーと目的

- オーナー: [名前]
- 主な目的: [YouTube制作 / 事業運営 / 学習など]
- 主な成果物: [台本 / スライド / 投稿下書きなど]

## 応答と品質

- 応答は日本語。コード、ファイル名、技術名は英語でもよい
- 結果を先に伝え、説明は必要な分だけ付ける
- 事実、推測、提案を区別する
- 最新仕様、料金、規約は公式の一次情報で確認し、確認日を残す
- 実機で確認していない操作を動作確認済みと表現しない

## 安全

- 削除、上書き、外部送信、公開、課金、自動投稿の前はオーナーへ確認する
- APIキー、トークン、認証情報、秘密情報をVaultへ書かない
- 公開文章は`30_Rules/Publishing.md`を確認する
- 大量編集の前に変更対象を示し、復元手段を確認する

## 編集範囲

- 依頼されたファイルと範囲だけを変更する
- 既存ファイルを大きく変える前に方針を示す
- 中間物はProject配下、完成物は`50_Outputs`へ保存する
- 第三者の字幕・全文コピーは公開用Outputへ含めない

## 記憶

- 安定した事実は`40_Memory/User.md`または`Business.md`へ置く
- 重要な判断は`40_Memory/Decisions.md`へ置く
- 次回も守る指摘は`40_Memory/Feedback.md`へ置く
- 新しい失敗パターンは`40_Memory/Failures.md`へ置く
- 一時的な状況はDailyまたはProjectへ置き、Memoryへ混ぜない
- 週次レビューで重複・期限切れ・矛盾を整理する

## 完了報告

- 変えたファイル
- 触っていない範囲
- 検証したこと
- 人の確認が残ること
```

## HOME.md

```markdown
# HOME

## 現在の焦点

- 最優先Project: [[10_Projects/README]]
- 今日の記録: [[01_Daily/README]]
- 未整理: [[00_Inbox/README]]

## 仕事の入口

- [[03_MOCs/README|MOCs — テーマ別の地図]]
- [[20_Areas/README|Areas — 継続領域]]
- [[40_Memory/MEMORY|Memory — 長期記憶の索引]]
- [[50_Outputs/README|Outputs — 完成物]]

## ルール

- [[30_Rules/Security]]
- [[30_Rules/Publishing]]

## 今週のレビュー

- [ ] Inboxを整理した
- [ ] Projectの現在地を更新した
- [ ] 新しいDecision / Feedback / Failureを選別した
- [ ] 古い情報をArchiveへ移した
- [ ] バックアップから戻せる状態を確認した
```

## README.md

```markdown
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
```
