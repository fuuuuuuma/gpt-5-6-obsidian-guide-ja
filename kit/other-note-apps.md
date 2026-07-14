# その他の厳選メモ・リサーチアプリ

結論から言うと、Codexがローカルファイルを直接扱う運用ではObsidianが第一候補です。ただし、すべての人に同じ道具が合うわけではありません。目的が「最速の記録」「チーム共同編集」「出典付きリサーチ」「暗号化された個人空間」なら、別のアプリが自然です。

確認日は2026年7月14日。プラン、料金、AI機能は変わりやすいため、導入時に公式情報を確認してください。

## 先に選び方

| 最優先 | 第一候補 | 理由 |
|---|---|---|
| CodexとローカルMarkdownで制作 | **Obsidian** | ファイルを直接読み書きでき、リンク・Properties・Canvasを併用できる |
| Apple製品で思いつきを最速記録 | **Apple Notes** | OS統合、スキャン、検索、ロックが使いやすい |
| チームのWiki、DB、Projectを一つにする | **Notion** | 共同編集と構造化されたワークスペースが中心 |
| チームで短い知識をリンクしながら育てる | **Cosense** | 軽い記述とリンクによる共同ナレッジに向く |
| アウトライナー中心でローカル知識を作る | **Logseq** | ブロックとジャーナルを中心にしたオープンソースの知識基盤 |
| 暗号化・Local-firstの個人空間 | **Anytype** | 鍵を自分で管理する暗号化とLocal-firstを重視 |
| オブジェクト型で美しく整理 | **Capacities** | 人、書籍、会議、Projectなど型を先に決められる |
| 見栄えのよい文書、共有、Apple系の操作感 | **Craft** | 文書、タスク、Daily、Whiteboard、共有をまとめやすい |
| 複数資料を出典付きで横断 | **NotebookLM** | 選んだSourceに基づく回答と引用位置の確認に向く |
| Web・PDF・画像を長期アーカイブして検索 | **Evernote** | Web Clipper、検索、OCRを中心に使いやすい |

## 1. Apple Notes

**向く人**: Apple製品を使い、入力摩擦を最小にしたい人。

タグ、Smart Folders、書類スキャン、添付、ロック、検索などがOSへ統合されています。思いつき、手書き、画像、受領書を素早く残す用途では強力です。

**Obsidianより向く場面**

- iPhoneやiPadから迷わず記録したい
- 複雑な知識構造より、日常のメモと検索を優先する
- Apple ecosystemの共有・スキャン・ロックを使いたい

**注意**

ローカルMarkdownのフォルダをAIエージェントに直接編集させる設計ではありません。長期的なAIワークスペースにするなら、確定したメモだけをObsidianへ移す二段構成も考えられます。

[Apple公式: NotesのタグとSmart Folders](https://support.apple.com/en-us/102288)

## 2. Notion

**向く人**: チームの文書、Wiki、Project、Databaseを一つのCloud workspaceで管理したい人。

共同編集、権限、Database、Project、検索、AI機能がまとまっています。個人の思考より、チームが同じ状態を見る業務に向きます。

**Obsidianより向く場面**

- 複数人がブラウザから同時編集する
- 顧客向けページや社内Wikiを共有する
- DatabaseとProject管理をすぐ使いたい

**注意**

ローカルMarkdownを正本にする設計とは異なります。Export、API、権限、オフライン要件を確認します。個人の知識はObsidian、チームの公開状態はNotionという分担もできます。

[Notion公式](https://www.notion.com/product)

## 3. Cosense

**向く人**: チームで短いページを気軽に書き、リンクから文脈を育てたい人。

旧Scrapboxで、Helpfeelは「書くこととリンクを容易にし、経験を知識へ変える」サービスとして説明しています。厳密な階層を先に決めず、ページ同士のつながりから共同知を作る文化に向きます。

**Obsidianより向く場面**

- チーム全員の入力摩擦を下げたい
- 短いメモとリンクをリアルタイムで共有したい
- ローカルファイル管理より共同の場を優先する

**注意**

Cloud serviceであり、ローカルMarkdown Vaultとは運用が異なります。AIエージェント連携、Export、公開範囲、料金は導入前に現在の公式仕様を確認します。

[Cosense公式](https://cosen.se/product)

## 4. Logseq

**向く人**: Journalとアウトライナーを中心に、ローカルで知識をつなげたい人。

Privacy-first、open-sourceのknowledge baseとして提供され、DesktopとMobile、Whiteboards、Syncなどを展開しています。文章ファイル単位より、ブロック単位で考え、日々のJournalからリンクを作る人に合います。

**Obsidianより向く場面**

- 箇条書きで考えることが多い
- Daily Journalを知識の中心にしたい
- ブロック参照を多用したい

**注意**

Obsidianと似て見えても、ブロック中心の操作感とデータモデルが異なります。既存Vaultの移行を急がず、一週間のJournalで試します。

[Logseq公式](https://logseq.com/downloads)

## 5. Anytype

**向く人**: 暗号化、Local-first、オフライン、データ主権を重視する人。

公式Docsは、暗号化されたLocal-firstのCloud代替としてAnytypeを説明しています。鍵を利用者が管理し、ローカルネットワークでpeer-to-peer同期できる設計です。ノートだけでなく、型を持つオブジェクトや共有Spaceを扱います。

**Obsidianより向く場面**

- 暗号化と鍵の自己管理を優先する
- ノート、メディア、Chatを一つのprivate spaceで扱いたい
- オブジェクト型の構造が合う

**注意**

暗号鍵を自分で管理する責任があります。Markdownフォルダを外部エージェントが直接編集するObsidianと同じ前提では選べません。ExportとAI連携要件を試して判断します。

[Anytype公式Docs](https://doc.anytype.io/anytype-docs)

## 6. Capacities

**向く人**: ファイルやフォルダより、Person、Book、Meeting、Projectなど「何の情報か」で整理したい人。

CapacitiesはすべてをObjectとObject Typeとして扱い、Properties、Templates、複数View、backlinks、Daily Notesを提供します。複雑なPlugin設定をせず、構造化された個人知識を作りたい場合に向きます。

**Obsidianより向く場面**

- フォルダ設計をしたくない
- 書籍、人物、会議など同じ型のノートが多い
- 見た目と構造を早く整えたい

**注意**

Obsidianのようなファイルベースの自由度とは交換関係があります。外部AIがどこまで読み書きできるか、Export後に構造が保たれるかを試します。

[Capacities公式](https://capacities.io/product)

## 7. Craft

**向く人**: 見栄えのよい文書、タスク、Daily、Whiteboard、共有を滑らかに使いたい人。

Craftは文書、タスク、Calendar、Whiteboards、Daily Notesを一つにまとめ、共同編集とoffline利用を提供しています。2026年時点の公式サイトではMCP接続やCodex CLIなどとの連携も案内されています。

**Obsidianより向く場面**

- そのまま共有できる美しい文書を作りたい
- Apple系のnative appらしい操作感を重視する
- 個人メモと小規模チームの文書を近づけたい

**注意**

AI連携は魅力的ですが、ローカルMarkdown Vaultを正本にする方式とは異なります。MCPやAPIの権限、同期、Export、料金を現在の仕様で確認します。

[Craft公式](https://www.craft.do/)

## 8. NotebookLM

**向く人**: PDF、Web、YouTube、音声、Google Docsなど、選んだ資料を出典付きで横断したい人。

NotebookLMはSourceに基づいて回答し、引用位置へ戻れるResearch assistantです。Study Guide、Briefing、Audio Overview、Mind Mapなどへ変換できます。YouTubeは公開動画かつ字幕がある場合、字幕テキストがSourceとして使われます。

**Obsidianより向く場面**

- 複数資料の内容を出典付きで比較する
- 長いPDFやYouTubeの論点を先に把握する
- 学習用の音声・ガイド・Mind Mapを作る

**注意**

NotebookLMは自分の長期記憶とProject管理の正本ではなく、調査補助として使うと整理しやすいです。権利のない資料をアップロードせず、重要な結論は元Sourceで確認します。

[NotebookLM公式ヘルプ](https://support.google.com/notebooklm/answer/16164461)

## 9. Evernote

**向く人**: Web、PDF、画像、書類を長期アーカイブし、検索で取り出したい人。

Web Clipper、添付、OCRを含む検索、タスクなどを一つにまとめやすく、過去資料を「保管して後から探す」用途に向きます。

**Obsidianより向く場面**

- Webページや受領資料の保存が中心
- フォルダやリンクを設計せず検索で取り出したい
- 過去の画像や文書をOCRで探したい

**注意**

Cloud serviceとSubscriptionを前提に検討します。AIエージェントの作業ディレクトリというより、資料アーカイブとしての役割が自然です。

[Evernote公式](https://evernote.com/features)

## 組み合わせるなら

### 制作者向け

```text
Apple Notes: 外出中の最速キャプチャ
NotebookLM: 選んだ資料の出典付き横断
Obsidian: 自分の判断・Project・Source・完成物
Notion: チームへ共有する進捗と公開Wiki
```

アプリ間ですべてを双方向同期しようとすると、重複と競合が増えます。各アプリの正本を決めます。例えば「思いつきの正本はDailyへ移した時点」「制作の正本はObsidian」「チーム公開状態の正本はNotion」と定義します。

## 乗り換え判断の5問

1. データの正本はローカルかCloudか
2. 一人で使うか、チームで同時編集するか
3. ファイル、ブロック、オブジェクトのどれで考えやすいか
4. AIに読ませるデータ範囲と保持条件を説明できるか
5. Export後に、リンク・Properties・添付をどこまで再利用できるか

新しいアプリの機能数ではなく、現在の仕事が一周するかで選びます。
