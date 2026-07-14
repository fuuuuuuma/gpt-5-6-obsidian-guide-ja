# GPT-5.6 × Obsidian 最強活用

[スライドを見る](https://fuuuuuuma.github.io/gpt-5-6-obsidian-guide-ja/slides.html) ｜ [1枚まとめを見る](https://fuuuuuuma.github.io/gpt-5-6-obsidian-guide-ja/onepager.html) ｜ [プレゼント4点を受け取る](https://fuuuuuuma.github.io/gpt-5-6-obsidian-guide-ja/present.html)

高速な実行力を、育ち続けるローカル記憶につなぐための実践ガイドです。Obsidianの基本説明は短く終え、後半では記憶構造、Source管理、MOC、Bases、Canvas、CLI、週次レビュー、Decision・Failure・Feedbackまで進みます。

## TL;DR

- Obsidianはノートを増やす道具ではなく、Rules・Project・Knowledge・Memory・OutputをローカルMarkdownで持つ「仕事の正本」にできます。
- Codexは、その正本から必要な文脈を読み、調査・整理・制作・検証を進め、結果をVaultへ戻せます。
- 最初から全メモを移行せず、配布テンプレートへ現在進行中のProjectを一つ入れ、SourceからOutputまで一周させるのが導入の近道です。

![OpenAI公式 GPT-5.6 発表ページ](img/openai_gpt56.jpg)

## このガイドで持ち帰れるもの

- Obsidianの基本を短時間で押さえ、その先の「AIが再利用できる記憶構造」へ進めます。
- Codexが何を読み、どこへ判断を戻すかを、Rules・Project・Source・Knowledge・Memoryの順で設計できます。
- YouTube企画、週次レビュー、意思決定、失敗の再発防止まで、一つのVaultでつなぐ考え方が分かります。
- 4つのプレゼントを使い、空のVaultから始めずに実務の一周目へ進めます。

## 目次

1. Obsidianを短く理解する
2. なぜGPT-5.6との連携が強いのか
3. AIの記憶を4層へ分ける
4. Source・Knowledge・MOC・Projectをつなぐ
5. Bases・Canvas・CLIを使い分ける
6. Codexと実務を一周させる
7. 週次レビューと安全設計
8. 7日・30日の導入ロードマップ
9. プレゼント4点

## Obsidianを60秒で理解する

Obsidianは、Markdownファイルを手元のフォルダへ保存し、ノート同士をリンクできるアプリです。一般的なクラウド型メモと違い、文章の正本が自分のファイルとして残ります。フォルダ、検索、Properties、Backlinks、Canvas、Basesなどを使えます。

この「普通のファイルであること」がAIエージェント連携では大きな意味を持ちます。CodexはVaultを作業フォルダとして開き、Markdownを読み、必要なファイルだけを更新できます。人はObsidianの画面から同じ内容を確認できます。AI専用の記憶と人間用のメモを別々に持つのではなく、同じ正本を共有できます。

基本を押さえたら、次に大切なのは、Obsidianを「思いつきを保存する場所」から「仕事の状態を保存する場所」へ変えることです。

## なぜGPT-5.6との連携が強いのか

GPT-5.6は、用途に応じて推論・日常作業・大量処理を分けやすく、Codexからローカルファイルを読み書きできます。企画のSource Mapを作る、複数ファイルを更新する、差分と検証結果を残す、といった「考えて終わりではない仕事」と相性がよいモデルです。Obsidian側にProject Homeと完了条件があると、Codexは必要な範囲だけを読み、長い仕事でも現在地をファイルへ戻せます。

ただし、モデルが長い文脈を読めることと、必要な記憶を毎回正しく参照できることは別です。Vault全体を毎回渡すと、古いProject、未確認の要約、重複したMemoryまで混ざります。そこで、人が監査できるファイル構造と読む順番を用意します。

役割は次のように分かれます。

| 担当 | 役割 |
|---|---|
| Obsidian | Rules・Project・Source・Knowledge・Memory・Outputの正本 |
| Codex | 必要な文脈を読み、調査・整理・制作・検証を進める |
| 人 | 目的、正本、公開・削除・課金などの最終判断を担う |

AIの回答を会話の中で消費せず、根拠・判断・成果物・学びを適切な場所へ戻す。ここまで一周して初めて、ノートが増えるほど次の仕事が始めやすくなります。

### GPT-5.6側で強くなる部分

GPT-5.6とCodexの組み合わせでは、調査結果を読むだけでなく、Project Homeの更新、Source Mapの整備、複数Markdownの編集、リンク切れや表記揺れの確認まで同じ作業単位にできます。人が毎回「前回の続き」を説明する代わりに、Projectへ現在地と完了条件を残し、Codexはそこから必要なSourceへ進みます。

実務では、速さだけを求めるより、変更したファイル、採用した根拠、残った確認事項を同時にVaultへ戻す設計が重要です。これにより、次のタスクが会話履歴ではなく監査できるファイルから再開できます。

### Codexに向く運用

- 複数ファイルへ同じPropertiesを追加し、Basesで一覧化する
- 調査メモから採用SourceだけをProjectへ接続する
- 長尺動画からnote・X・短尺の論点を別Outputへ展開する
- 週次レビューで重複Memory、期限切れ情報、未完了Projectを洗い出す
- 公開・削除・課金の直前で止まり、人の確認を待つ

ここでObsidianは「保存場所」、Codexは「実行役」、人は「目的と最終判断」という役割になります。3者の責任を混ぜないほど、自動化の範囲を広げても安全性を保ちやすくなります。

## AIの記憶は4層に分ける

### 1. Rules

言語、安全、保存先、編集範囲、品質基準、完了報告など、毎回守る契約です。AGENTS.mdは入口として短く保ち、長い手順や事業知識は別ノートへ分けます。

### 2. Project

現在の目的、対象者、完成条件、やらないこと、読むSource、現在地、次の一手を持ちます。一時的な進捗は長期Memoryではなく、ProjectかDailyへ置きます。

### 3. Knowledge

Sourceを要約しただけの文章ではなく、一つの主張、自分の解釈、使える条件、使わない条件、反対意見、確認日を持つ再利用可能なノートです。タイトルを「AIメモ」のような箱ではなく、「外部記憶は保存と参照を分ける」のような主張にします。

### 4. Memory

次回以降も使う人物・事業・重要なDecision・繰り返すFeedback・再発防止のFailureを置きます。AIが推測したプロフィールや、その日の進捗を長期Memoryへ混ぜません。週次レビューで人が昇格を決めます。

## 推奨Vault構造

```text
.
├── AGENTS.md
├── CLAUDE.md
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

フォルダはライフサイクルを表します。未整理はInbox、期限と成果物がある仕事はProject、完成物はOutput、終了したものはArchiveです。リンクは意味の関係に使います。Projectから根拠のKnowledgeへ、Knowledgeから元Sourceへ戻れるようにします。

この構造は[Nano0nFire/my-obsidian-template](https://github.com/Nano0nFire/my-obsidian-template)のMOC、Pages、Refs、Templates、衝突しにくい命名という考え方を参考にし、AIエージェントとコンテンツ制作向けに独自設計しています。参照先は2026年7月14日の確認時点でライセンス表示が見当たらなかったため、設定やコードは複製していません。

## Sourceを混ぜない

一つのノートへ文字起こし、AI要約、自分の判断、公開文章を混ぜると、どこまでが事実か分からなくなります。次の4段階へ分けます。

| 層 | 内容 | 使い方 |
|---|---|---|
| Raw | 文字起こし、走り書き、未整理データ | 非公開の材料として保持 |
| Source | URL、著者、公開日、取得日、該当箇所 | 主張の根拠へ戻る |
| Knowledge | 自分の解釈、採用条件、反対意見 | 別Projectで再利用 |
| Output | 台本、スライド、note、投稿下書き | 対象者と媒体に合わせて制作 |

YouTubeなら、動画URLだけでなく採用した時刻を残します。公式仕様、第三者の評価、Xの体験談には異なる`source_kind`を付けます。仕様・料金・提供条件には`checked_at`を置き、古くなった前提を判断できます。

## MOCは読む順番の地図

MOCはリンクを集めただけの目次ではありません。初心者、実務者、撮影者など、読む人ごとの入口と順番を示します。今回採用する論点と見送る論点、その理由も書きます。

AIには、Rules → Project → MOC → 必要なKnowledge → Sourceの順に進ませます。Vault全体を総当たりさせず、Projectに関係する文脈へ絞ることで、古い情報や別案件のルールが混ざるのを減らせます。

## Codex × Obsidianの実践フロー

1. **企画を始める** — Project Homeと完了条件を作り、読むSourceを限定する
2. **調査する** — 公式情報・動画・体験談をSourceへ分け、確認日を残す
3. **制作する** — 台本・スライド・横展開を同じProjectから作る
4. **検証する** — 差分・リンク・事実を確認し、人の判断待ちを止める

### YouTube企画から横展開まで

1. 公式情報、参考動画、Xの投稿をSourceへ分ける
2. 主張ごとにKnowledgeを作り、採用理由と反対意見を残す
3. Projectで視聴者の悩み、結論、根拠、実演、結果を並べる
4. Canvasでスライド順を確認してから文章化する
5. 長尺動画からショートは一論点ずつ、noteは根拠を深掘り、Xは判断基準へ再構成する
6. 公開後の反応、誤解、質問をFeedbackと次のProjectへ戻す

同じ文章を各媒体へコピーするのではなく、同じSource Mapから媒体別に作るのがポイントです。字幕全文や第三者文章を公開Outputへ入れず、必要な範囲を要約し、元Sourceへリンクします。

### 週次レビュー

AIに候補を出させ、人が残す場所を決めます。

- Inboxを整理する
- Projectの現在地と次の一手を更新する
- 繰り返したDecision、Feedback、Failureを候補化する
- 期限切れ・重複・矛盾したMemoryを統合またはArchiveする
- 完了Outputを再利用できるKnowledgeへ戻す
- バックアップから復元できる状態を確認する

### 意思決定ログ

Decisionには、Context、Options、Decision、Reason、Owner、Date、Review conditionを残します。次のAIは結論だけでなく、「なぜその選択をしたか」を読めます。状況が変わったときも、前回と違う答えを突然出すのではなく、どの前提が変わったかを説明できます。

### FailureとFeedback

Failureは、失敗した操作、再現条件、原因、解消方法、再発防止を残します。Feedbackは、視聴者向けにする、誇張を避ける、スライドだけで理解できるようにする、といった次回も守る品質指摘です。同じ詰まり方が繰り返されたら、個別Projectのメモから共通Rulesへ昇格します。

## Bases・Canvas・CLIの使いどころ

### Bases

BasesはCore Pluginで、MarkdownとPropertiesから表・カードなどのデータベース風ビューを作れます。企画ノートへ`status`、`channel`、`publish_at`、`source_checked`を持たせると、制作ダッシュボードになります。見た目はデータベースでも、正本はローカルMarkdownです。

### Canvas

Canvasは、ノート、添付、Webページを2次元に並べるCore Pluginです。動画なら悩み→主張→根拠→実演→結果→CTAをカード化し、話の飛躍を見つけます。Project開始前のプレモーテムにも使えます。失敗した未来、原因、初期兆候、防衛策を分けて並べ、結果をProjectとRulesへ戻します。

### Obsidian CLI

Obsidian CLIを使える環境では、Codexから対象Vaultやファイルを明示し、検索・作成・Properties更新などのアプリ操作を加えられます。利用には対応するObsidianのバージョンや設定が必要です。導入時は[Obsidian CLI公式ヘルプ](https://obsidian.md/help/cli)で現在の条件を確認してください。

## 仕事別の活用例

### 顧客・商品ナレッジ

顧客の発言、問い合わせ、商談、アンケートをSourceとして保存し、繰り返す悩みを一問一ノートのKnowledgeへ変えます。商品ノートには対象者、解決する問題、向かない条件、証拠、よくある反論を持たせます。Codexへ企画や文章を依頼するときは、人物・商品・過去の反応をVaultから読み、一般論ではなく現在の事業に合う案を作れます。

顧客の発言をそのままMemoryへ入れず、個人情報や機密区分を確認します。複数の発言から作った仮説には「推測」、確認済みの事実には出典と確認日を付けます。商品仕様が変わったときは古いノートへ追記して打ち消すのではなく、変更日と旧条件を履歴へ残します。

### 会議とプロジェクト管理

会議メモを時系列のまま置かず、事実、決定、宿題、未解決へ分けます。決定事項はDecisionへリンクし、誰が、いつまでに、何を確認するかをProjectへ戻します。次回の会議前にCodexが前回Decisionと未解決をまとめるため、「前回どこまで話したか」の確認時間を減らせます。

Project Homeには、長い議事録を貼るのではなく、現在の結論、残る論点、次の一手を一行ずつ残します。会議が終了しても使う判断はMemory、案件固有の経緯はProject、再利用できる考え方はKnowledgeへ分けます。

### 学習・研究

書籍、論文、動画、公式ドキュメントをSourceへ分け、一つの主張に複数Sourceをつなぎます。Knowledgeには要約だけでなく、自分の言葉での説明、反対意見、現場で試す方法を書きます。MOCには初心者が読む順番と、実務で参照する順番を分けておくと、学び直しと実務利用の両方に使えます。

CodexにはProjectの問いと採用済みSourceを読ませ、分かっていること、割れていること、まだ調べることを分けさせます。結論が出なかった点も未確認として残すと、次の調査が同じ場所を回りません。

### 日次・週次の振り返り

Dailyには出来事、感情、作業ログ、気づきを軽く残します。週次レビューで、成果につながった行動、繰り返した問題、重要な判断、次週の焦点を抽出します。毎日の感想すべてをMemoryへ上げず、複数回現れた傾向や、次回の判断に影響するものだけを候補にします。

振り返りの成果は「きれいな日報」ではありません。Rulesが一つ改善された、Projectの完了条件が明確になった、Failureに再発防止が入った、不要なMemoryをArchiveした、という状態変化で確認します。

### 公開コンテンツのファクトチェック

台本や資料の主張からSourceまで戻れるようにし、公開前に事実、推測、提案、体験談を分類します。最新仕様、料金、規約、提供地域は公式情報で再確認します。ベンチマークやSNSの評判は条件を添え、環境によって変わる体感速度を一般化しません。

公開するOutputには、読者が理解と行動に使える情報だけを残します。第三者の文字起こし全文や非公開メモを混ぜず、根拠は確認できる一次情報へリンクします。

## 設計できているか確認する10項目

- [ ] HOMEから現在の最優先Projectへ移動できる
- [ ] Projectに目的、対象者、完成条件、やらないことがある
- [ ] Projectから採用Sourceへ戻れる
- [ ] Raw、Source、Knowledge、Outputが分かれている
- [ ] AGENTS.mdが長い事業知識で膨らんでいない
- [ ] 一時的な進捗が長期Memoryへ混ざっていない
- [ ] Decisionに選択肢と採用理由が残っている
- [ ] Failureに再現条件と再発防止がある
- [ ] 削除・上書き・公開・課金で人が確認できる
- [ ] バックアップから戻す手順を説明できる

すべてを一日で満たす必要はありません。現在のProjectを一周した後、詰まった項目だけを整えます。テンプレートの空欄が多く残るなら、項目を増やすのではなく減らします。

## プラグインの考え方

最初はDaily Notes、Templates、Properties view、Bases、Backlinks、Canvas、File recoveryなどCore Pluginで一つのProjectを完了します。標準機能で不足した課題を一文で説明できるようになってから、Community Pluginを追加します。

- 検索：Omnisearch
- 定型入力：QuickAdd、Templater
- 表記統一：Linter
- タスク集計：Tasks
- 高度なProperties集計：Dataview
- 図解：Excalidraw
- バックアップ：Obsidian Git、Local Backupなど
- AI関連：Smart Connections、Copilot for Obsidian、Claudian

AI関連Pluginは、Vaultの内容や入力、ツール出力を外部プロバイダーへ送る場合があります。配布元、更新状況、ライセンス、ファイル・ネットワーク・Shellの権限、料金、保持条件を確認し、機密を含まない小さなVaultで試します。

## 安全とバックアップ

- APIキー、トークン、認証情報をVaultへ保存しない
- 公開Vaultと機密Vaultを分け、フォルダ名だけを権限境界にしない
- 削除、上書き、大量編集、外部送信、公開、課金の前に人が確認する
- Git、Obsidian SyncのVersion History、OSバックアップ、外部ストレージなど役割の違う復元手段を持つ
- File Recoveryだけを完全なバックアップと見なさない
- バックアップが存在するだけでなく、復元操作も試す
- AIが編集した差分を人が確認する

## 最初の7日

### Day 1

配布テンプレートを複製し、ObsidianでVaultとして開きます。既存メモを全部移さず、新しいProject用の小さなVaultとして始めても構いません。

### Day 2

AGENTS.mdの名前、目的、成果物、安全、保存先をCodexの運用へ合わせます。User.mdとBusiness.mdには長く変わらない情報だけを数項目書きます。

### Day 3

現在進行中のProjectを一つ作り、目的、対象者、完成条件、やらないこと、Source、現在地、次の一手を書きます。

### Day 4–5

Sourceを集め、Knowledgeへ変換し、Outputを一つ作ります。ノート整理だけで終わらず、成果物まで一周させます。

### Day 6–7

InboxとProjectを整理し、次回も使うDecision・Feedback・FailureだけをMemoryへ上げます。不要な項目や使わなかったPluginを減らし、復元操作を確認します。

## 30日後の確認

ノート数やGraphの密度ではなく、仕事への再利用を見ます。

- 前提を再説明せずProjectを再開できたか
- 過去のSourceとKnowledgeを新しい制作に使えたか
- Decisionにより判断の理由を説明できたか
- FailureとFeedbackで同じ問題の再発を減らせたか
- 公開や大量編集の前に人が確認できたか
- 終了Projectと古いMemoryを整理できたか

## よくある質問

### 既存の大量メモを最初に移行した方がよいですか？

最初から全件を移す必要はありません。現在進行中のProjectと、それに必要なSource・Rules・Memoryだけで小さく始めます。運用が固まってから、再利用価値のある過去メモを順に移します。古いメモを大量に入れると、重複・期限切れ・表記揺れまでAIが読み込むため、導入時の判断が難しくなります。

### フォルダとリンクはどちらを優先しますか？

フォルダは仕事の状態、リンクは意味の関係に使います。Inbox、Project、Output、Archiveのようなライフサイクルはフォルダで表し、原因、反証、事例、派生、根拠は本文のリンクで説明します。どちらか一方へ統一する必要はありません。

### AIのAuto Memoryだけでは足りませんか？

Auto Memoryは操作上の学びや環境固有の補助には便利ですが、安全ルール、Projectの進捗、公開基準、事業の正本を任せきりにしません。人がObsidianで確認でき、Codexから同じ内容を読めるMarkdownを正本にします。

### Obsidian SyncとGitはどちらを使いますか？

目的が違います。Syncは端末間同期とVersion History、Gitは差分と履歴、外部バックアップは端末故障やアカウント問題への備えになります。自分の端末構成、機密性、復元方法を基準に組み合わせます。どの方法でも、実際に戻せるかを試します。

### Community Pluginは危険ですか？

一律に危険とは言えませんが、Core Pluginとは異なり第三者コードが動きます。公式レジストリ、配布元、更新状況、Issue、ライセンス、ファイル・ネットワーク・Shellへの影響を確認します。AI関連Pluginは入力やVault内容の外部送信も確認します。

### どこまでAIへ自動化させますか？

読み取り、整理、下書き、ローカル保存、検証は自動化しやすい領域です。削除、既存原本の大幅な上書き、外部送信、公開、課金、自動投稿は人の確認で止めます。長い自動タスクでも、完了条件、変更対象、復元手段、確認待ちの条件をProjectへ書きます。

## よくある失敗

### Vault全体を毎回読ませる

情報量が増えるほど、古い案件と現在の案件が混ざります。Project Homeから読む範囲を指定します。

### Memoryへ何でも入れる

一時的な状況、AIの推測、今日の進捗で長期記憶が埋まります。Daily・Project・Knowledgeと役割を分けます。

### AIの要約を事実にする

SourceとKnowledgeを分離し、重要な主張にはURL、該当箇所、確認日を残します。

### Pluginを一度に増やす

問題発生時に原因が分かりません。Core Pluginで一周してから、一つずつ追加します。

### ノートを増やすことが目的になる

保存量ではなく、制作時間、判断、引き継ぎ、再発防止への再利用で測ります。

## プレゼント4点

1. [Obsidianに入れておく記憶構造テンプレート](https://fuuuuuuma.github.io/gpt-5-6-obsidian-guide-ja/memory-template.html)
2. [Obsidian活用術100選](https://fuuuuuuma.github.io/gpt-5-6-obsidian-guide-ja/ideas100.html)
3. [入れておくべきプラグイン集](https://fuuuuuuma.github.io/gpt-5-6-obsidian-guide-ja/plugins.html)
4. [その他の厳選メモアプリ](https://fuuuuuuma.github.io/gpt-5-6-obsidian-guide-ja/note-apps.html)

プレゼントページでは各資料をHTMLで読み、全文コピーまたはMarkdown保存できます。100選は1項目ずつカード化しているため、今の課題に近いものだけを選べます。

## 公式情報・参考資料

- [OpenAI GPT-5.6](https://openai.com/index/gpt-5-6/)
- [Obsidian CLI](https://obsidian.md/help/cli)
- [Obsidian Bases](https://obsidian.md/help/bases)
- [Obsidian Canvas](https://obsidian.md/help/plugins/canvas)
- [Obsidian Community Pluginsの安全性](https://obsidian.md/help/plugin-security)
- [Obsidian File Recovery](https://obsidian.md/help/plugins/file-recovery)
- [Obsidian Syncの暗号化](https://obsidian.md/help/sync/security)
- [Obsidian Sync Version History](https://obsidian.md/help/sync/version-history)
- [Nano0nFire/my-obsidian-template](https://github.com/Nano0nFire/my-obsidian-template)
- [関連動画：j54h67o7q6w](https://youtu.be/j54h67o7q6w)
- [関連動画：boQuaTAW7qU](https://youtu.be/boQuaTAW7qU)
- [関連動画：jTK7h3cfcCM](https://youtu.be/jTK7h3cfcCM)
- [hiroya.obsidian YouTubeチャンネル](https://www.youtube.com/@hiroya.obsidian/videos)

仕様・料金・提供条件は変わるため、導入時は各公式ページの最新情報をご確認ください。
