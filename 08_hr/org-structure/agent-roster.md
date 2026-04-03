# UCHI エージェント ロースター（担当者定義）

> このファイルは各部署エージェントの役割・権限・連携関係を定義する。
> エージェントは `.claude/commands/` のコマンドとして実装されている。

---

## エージェント一覧

| エージェント名 | コマンド | 相当役職 | 主な責任 | 判断権限 |
|---|---|---|---|---|
| Ops Agent | `/ops-agent` | General Manager | 店舗・EC・スタッフ・ライセンス | 通常運営判断 |
| Marketing Agent | `/marketing-agent` | Brand & Marketing Lead | コンテンツ・SNS・PR・イベント | コンテンツ最終判断 |
| Finance Agent | `/finance-agent` | Finance Controller | 財務管理・予算・レポート | 報告のみ（承認はCEO） |
| Product Agent | `/product-agent` | Product & Sourcing Lead | 商品・蔵元・発注・品質管理 | 通常発注判断 |
| B2B Agent | `/b2b-agent` | B2B Sales Lead | 法人営業・クライアント管理 | 提案・交渉（契約はCEO） |
| Weekly Orchestrator | `/weekly-review` | Chief of Staff | 全エージェント統合・CEO報告 | レポートのみ |

---

## エージェント間の連携フロー

```
CEO（Shane）
│
│  毎朝: /daily-schedule（全体把握）
│  毎週月曜: /weekly-review（経営判断）
│
├─► /ops-agent ──────────────────────────────────────────────────┐
│   │                                                             │
│   ├─► 在庫不足 → /product-agent に発注依頼                     │
│   ├─► 売上異常 → /finance-agent に報告・分析依頼              │
│   └─► スタッフ欠員 → /issue-triage でJD作成                   │
│                                                                 │
├─► /marketing-agent ──────────────────────────────────────────  │
│   │                                                             │
│   ├─► 新商品 → /product-agent からストーリーブリーフを取得     │
│   ├─► イベント → /ops-agent と会場・スタッフ調整              │
│   └─► PR実績 → /finance-agent に売上インパクト共有            │
│                                                                 │
├─► /finance-agent ────────────────────────────────────────────  │
│   │                                                             │
│   ├─► 粗利悪化 → /product-agent + /ops-agent にアラート       │
│   └─► 予算超過 → CEOにエスカレーション                         │
│                                                                 │
├─► /product-agent ────────────────────────────────────────────  │
│   │                                                             │
│   ├─► 新商品入荷 → /marketing-agent にストーリーブリーフ提供  │
│   ├─► 価格変動 → /finance-agent に報告                        │
│   └─► 欠品リスク → /ops-agent + CEOに通知                     │
│                                                                 │
└─► /b2b-agent ────────────────────────────────────────────────  │
    │                                                             │
    ├─► 大型案件 → CEOに報告                                     │
    ├─► 在庫確認 → /product-agent に照会                        │
    └─► 成約 → /ops-agent に配送・納品調整依頼                  ─┘
```

---

## エージェントの権限マトリクス

| アクション | Ops | Marketing | Finance | Product | B2B | CEO |
|---|---|---|---|---|---|---|
| 通常発注（〜SGD 1,000） | ✅ | — | — | ✅ | — | — |
| 大口発注（SGD 1,000〜） | 承認要 | — | — | 承認要 | — | ✅ |
| コンテンツ投稿 | — | ✅ | — | — | — | — |
| 価格変更 | — | — | 確認 | 提案 | 提案 | ✅ |
| 契約締結 | — | — | — | — | 準備 | ✅ |
| 採用決定 | 面接参加 | 面接参加 | — | — | — | ✅ |
| ライセンス対応 | 監視 | — | — | — | — | ✅ |

---

## エージェント起動のトリガーワード（CLAUDE.mdと連動）

```
/ops-agent      ← 「オペレーション」「店舗」「在庫」「シフト」「EC運営」
/marketing-agent ← 「マーケティング」「SNS」「コンテンツ」「キャンペーン」「投稿」
/finance-agent  ← 「売上」「財務」「P&L」「粗利」「キャッシュ」「予算」
/product-agent  ← 「商品」「仕入れ」「蔵元」「在庫発注」「ソーシング」
/b2b-agent      ← 「B2B」「法人」「提案書」「クライアント」「卸」
/weekly-review  ← 「振り返り」「レトロ」「先週どうだった」「週次レビュー」
/daily-schedule ← 「おはよう」「今日の予定」「今日何する」
/issue-triage   ← 「Issueにして」「タスク登録」「GitHubに上げて」
/agent-memory   ← 「覚えておいて」「メモして」「保存して」
```

---

*作成日: 2026-04-03 | 参照: `.claude/commands/` | 連携: `01_company/org-chart/current.md`*
