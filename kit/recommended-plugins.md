# Obsidian 推奨プラグイン集

最初から全部を入れないでください。まずCore Pluginsで一つのProjectを完了し、不足が明確になった順にCommunity Pluginsを追加します。確認日は2026年7月14日です。

## 最初はCore Pluginsだけでよい

| Plugin | 用途 | AIエージェントとの使い方 |
|---|---|---|
| **Daily Notes** | 日次の受信箱 | 作業ログと記憶候補を集め、週次で選別する |
| **Templates** | ノート形式を統一 | Project、Source、Decisionの項目を固定する |
| **Properties view** | メタデータ管理 | `status`や`source_checked`の表記揺れを減らす |
| **Bases** | ローカルMarkdownの一覧・カード・表 | 企画、進捗、横展開をPropertiesから表示する |
| **Backlinks** | 参照元の確認 | 主張がどの台本・企画で使われたか追う |
| **Outgoing links** | リンク先の確認 | SourceやKnowledgeへの接続漏れを見つける |
| **Canvas** | 構成・関係の検討 | 悩み、主張、根拠、実演、CTAを並べる |
| **File recovery** | ローカルスナップショット | 誤編集から戻る補助。完全なバックアップにはしない |

## 段階1：検索・入力・品質

| Plugin | 向く人 | 主な用途 | 導入判断 |
|---|---|---|---|
| [Omnisearch](https://github.com/scambier/obsidian-omnisearch) | Vault内検索を強化したい | ノートと添付の全文検索 | 標準検索で不足したら入れる |
| [QuickAdd](https://github.com/chhoumann/quickadd) | 定型ノートを素早く作りたい | Capture、Template、Macro | InboxやSourceの入力が定型化してから |
| [Templater](https://github.com/SilentVoid13/Templater) | 標準Templates以上の自動化が必要 | 動的テンプレート、スクリプト | テンプレート項目が安定してから |
| [Linter](https://github.com/platers/obsidian-linter) | MarkdownとPropertiesを統一したい | 見出し、空白、YAMLの整形 | 既存ルールと競合しない設定で小さく試す |
| [Homepage](https://github.com/mirnovov/obsidian-homepage) | 起動時の入口を固定したい | HOMEやDashboardを開く | HOME運用が定着したら |

## 段階2：タスク・データ・制作

| Plugin | 向く人 | 主な用途 | 注意 |
|---|---|---|---|
| [Tasks](https://github.com/obsidian-tasks-group/obsidian-tasks) | 複数ノートのタスクを横断したい | 期限、繰り返し、クエリ | Project管理が複雑な場合に限定する |
| [Dataview](https://github.com/blacksmithgu/obsidian-dataview) | Propertiesを高度に集計したい | クエリ、表、計算 | まずBasesで足りるか確認する |
| [Meta Bind](https://github.com/mProjectsCode/obsidian-meta-bind-plugin) | ノート内からPropertiesを操作したい | 入力UI、ボタン、表示 | 自動変更の範囲が見える設計にする |
| [Excalidraw](https://github.com/zsviczian/obsidian-excalidraw-plugin) | 手描き図と説明資料を作りたい | 図解、注釈、構成検討 | Canvasとの役割を分ける |
| [Calendar](https://github.com/liamcain/obsidian-calendar-plugin) | Daily Notesを日付から開きたい | カレンダー導線 | 日次運用をしている場合に有効 |
| [Spaced Repetition](https://github.com/st3v3nmw/obsidian-spaced-repetition) | 暗記が必要な学習をする | フラッシュカード、復習 | 全ノートをカード化しない |

## 段階3：同期・バックアップ

| Plugin / 方法 | 用途 | 注意 |
|---|---|---|
| [Obsidian Git](https://github.com/Vinzent03/obsidian-git) | Gitで履歴と差分を残す | コンフリクト、秘密情報、リポジトリ容量を理解して使う |
| [Local Backup](https://github.com/cgcel/obsidian-local-backup) | ローカルへ定期コピー | 同じ端末だけでは故障対策にならない |
| Obsidian Sync | 端末間同期とVersion History | E2EEのパスワード管理とプランを公式で確認する |
| OS / 外部ストレージのバックアップ | 端末故障や誤削除から復元 | 復元テストまで実施する |

`File recovery`、Git、Sync、外部バックアップは役割が違います。一つだけで全リスクをカバーする前提にしません。

## AI関連は目的を決めてから

| Plugin | 概要 | 推奨度 |
|---|---|---|
| [Smart Connections](https://github.com/brianpetro/obsidian-smart-connections) | ローカル埋め込みを使った意味検索と関連ノート | 大きなVaultで通常検索が不足した場合に検討 |
| [Copilot for Obsidian](https://github.com/logancyang/obsidian-copilot) | Vault内チャット、モデル接続 | 送信先、API費用、対象データを確認できる人向け |
| [Claudian](https://github.com/YishenTu/claudian) | Obsidian内でCodexを動かし、Vaultを作業場所にする | 上級者向け。小さなテストVaultから |

### Claudianを「入れておくべき」に含めない理由

ClaudianはMITライセンスで公開され、CodexをVault内で扱える選択肢です。一方、Obsidian公式Community Pluginレジストリの説明には、Obsidianスタッフによる手動レビュー未実施と明記されています。また、設定したAIプロバイダーへ入力、ファイル内容、ツール出力が送られる場合があります。

使う場合は次を先に確認します。

- 個人情報や機密情報を含まないテストVaultで試す
- 読み取り・書き込み・Shellの許可範囲を理解する
- 利用するAIプロバイダーと保持条件を確認する
- 自動編集前にGitまたはバックアップを作る
- 変更差分を人がレビューする

## 参考テンプレートにあっても一律採用しないもの

参考リポジトリにはGit、Dataview、Excalidraw、Tasks、Templater、Meta Bindなど多数のプラグインが含まれます。しかし、同じ構成を複製すると、目的不明の設定、更新負担、権限リスクまで引き継ぎます。本資料では構造上の考え方だけを参考にし、プラグインは用途別に再選定しています。

## 導入チェック

- [ ] このPluginが解く具体的な問題を一文で言える
- [ ] Core Pluginや標準機能では不足している
- [ ] 公式Community Pluginレジストリで配布元を確認した
- [ ] 更新状況、Issue、ライセンスを確認した
- [ ] ファイル、ネットワーク、外部コマンドへの影響を理解した
- [ ] 小さなVaultで試した
- [ ] 無効化・復元の手順がある

## 公式情報

- [Obsidian Community Pluginsの安全性](https://obsidian.md/help/plugin-security)
- [Obsidian Community Plugin registry](https://github.com/obsidianmd/obsidian-releases/blob/master/community-plugins.json)
- [File recovery](https://obsidian.md/help/plugins/file-recovery)
- [Obsidian Syncの暗号化](https://obsidian.md/help/sync/security)
- [Sync Version History](https://obsidian.md/help/sync/version-history)
