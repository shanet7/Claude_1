# UCHI Agent Memory

> このファイルはセッションをまたいで記憶を保持するための永続メモリ。
> 「覚えておいて」「メモして」で自動更新される。
> Claude Codeはセッション開始時にこのファイルを読み込む。

---

## 📌 今すぐやること
<!-- /daily-schedule で優先表示される。完了したら ~~取り消し線~~ またはDeleteで削除 -->

> ⚠️ **【2026-03-13までに対応】Google Calendar トークン再認証**
> リフレッシュトークンの有効期限: **2026-03-14 16:38 JST**
> 前日（3/13）までに以下を実行: `npx @cocal/google-calendar-mcp auth`
> → 完了後このメモを削除してください


---

## 🗂️ 記憶ログ

<!-- 以下のフォーマットで追記していく:
### YYYY-MM-DD | #カテゴリ
内容
→ 関連: フォルダ / Issue #XX
-->

### 2026-03-07 | #プロジェクト #数字
SGバー昼間活用：日本茶×かき氷カフェ事業計画完成。
- 事業計画書: `10_projects/active/202603_SG_BAR_日本茶かき氷カフェ.md`
- GitHub Issue #3: https://github.com/shanet7/Claude_1/issues/3（Q2 2026 マイルストーン）
- 初期投資: SGD 27,000〜45,000（中央値 SGD 35,000）
- 損益分岐点: 1日28名 / 投資回収: BASEケース5.6ヶ月 / 年間ROI: 約114%
- 開業ロードマップ: 12週間（Week 1〜2: URA/Licence申請→Week 12: グランドオープン）
- 次のアクション: Liquor Licence種別確認・URA事前相談・FHO資格者確保

### 2026-03-07 | #決定事項
Google Calendar MCP 連携完了。
- パッケージ: @cocal/google-calendar-mcp
- 接続カレンダー: shane.takakura@gmail.com（メイン）
- 認証情報: ~/.config/google-calendar-mcp/（gcp-oauth.keys.json + tokens.json）
- GCPプロジェクトID: 124007224141（UCHI-Calendar）
- トークン保存先: ~/.claude/settings.json（グローバル・Git管理外）
- 読み取りテスト: ✅ 成功

### 2026-03-07 | #決定事項
Notion MCP 連携完了。
- Bot名: UCHI Claude_test_Mar2026
- ワークスペース: shunさんのNotion
- トークン保存先: ~/.claude/settings.json（グローバル・Git管理外）
- 連携済みページ: クイックメモ / サブページ（追加は各ページの「コネクト」から）
- 読み書きテスト: ✅ 成功

### 2026-03-07 | #決定事項
GitHub連携完了（shanet7/Claude_1）。
- gh CLI認証済み（shanet7）
- ラベル23種・マイルストーン4期（Q1〜Q4 2026）作成済み
- Issueテンプレート4種: general-task / market-entry / b2b-lead / creative-brief
- Issue #1 作成済み: 🇲🇾 Malaysia 参入戦略の調査開始

### 2026-03-06 | #決定事項
UCHIのClaude Code作業環境を UCHI/ ディレクトリとして整備。
CLAUDE.md, スラッシュコマンド3種, MCP設定テンプレートを作成。

---

## 🤝 パートナー・人物メモ
<!-- 蔵元・B2Bクライアント・パートナーの担当者情報など -->

| 名前/会社 | 役割 | 連絡先メモ | 最終接触 |
|---|---|---|---|
| — | — | — | — |

---

## 🏷️ 重要な決定事項サマリー
<!-- #決定事項 の中で特に重要なものをピックアップ -->


---

## 🔢 重要な数字
<!-- #数字 カテゴリのサマリー。KPI等 -->

| 指標 | 数値 | 期間 | 備考 |
|---|---|---|---|
| SGカフェ BEP | 28名/日 | 2026 | SGバー昼間カフェ 損益分岐点 |
| SGカフェ 初期投資 | SGD 35,000 | 2026 | 中央値。最小SGD 27K・最大SGD 45K |
| SGカフェ 投資回収 | 5.6ヶ月 | BASEケース | 月次営業利益 SGD 6,250前提 |
| SGカフェ 目標客単価 | SGD 22〜28 | 2026 | ドリンク+スイーツ組み合わせ |

---

*最終更新: 2026-03-07 | 管理コマンド: `/agent-memory`*
