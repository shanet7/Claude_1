# /issue-triage — GitHub Issue 自動作成

このコマンドは「Issueにして」「タスク登録して」「GitHubに上げて」で自動発動する。

## 前提条件
- `gh auth login` でGitHub認証済みであること
- リポジトリが `git remote` で設定済みであること
- ラベルが `CLAUDE.md` の「ラベル設計」に従って作成済みであること

## 実行手順

### Step 1: コンテキスト把握
直前の会話から以下を自動抽出する:
- **何をするタスクか**（動詞+目的語で簡潔に）
- **なぜ必要か**（背景・目的）
- **どの市場か**（SG/MY/ID/HK/IN/ALL）
- **どのチャネルか**（ec/b2b/bar/ALL）
- **タイプ**（strategy/ops/legal/creative/research/finance/hr）
- **優先度**（P0/P1/P2/P3）
- **関連するフォルダ**（例: `02_markets/malaysia/`）

不明な場合は最低限の情報だけ聞き返す（1回のやりとりで完結させる）。

### Step 2: Issue ドラフト提示

以下の形式でユーザーに確認を求める:

---
**作成するIssue（確認）**

**タイトル:** （簡潔・動詞始まり）

**ラベル:** `mkt/XX` `ch/XX` `type/XX` `P2-medium`

**本文:**
```
## 目的・背景
（1-2文）

## やること
- [ ] アクション1
- [ ] アクション2

## 完了条件
（何ができたらDone）

## 関連フォルダ
`UCHI/XX_XXX/`

## 期限
YYYY-MM-DD（未定の場合は「未定」）
```

→ このままで作成しますか?（修正点があれば教えてください）

---

### Step 3: Issue 作成

ユーザーが「OK」「作って」「はい」と言ったら実行:

```bash
gh issue create \
  --title "タイトル" \
  --body "$(cat <<'EOF'
## 目的・背景
...

## やること
- [ ] ...

## 完了条件
...

## 関連フォルダ
`UCHI/XX_XXX/`

## 期限
...
EOF
)" \
  --label "mkt/SG,type/ops,P2-medium"
```

### Step 4: 完了通知

```
✅ Issue #XX を作成しました。
タイトル: 「〇〇」
URL: https://github.com/xxx/xxx/issues/XX

関連ファイルに Issue 番号を記載しておきますか?
```

## オプション引数
- `/issue-triage list` — 現在のオープンIssue一覧を表示
- `/issue-triage close #XX` — Issue #XX をクローズ
- `/issue-triage weekly` — 今週完了したIssueの週次サマリー
