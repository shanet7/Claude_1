# /daily-schedule — 朝のブリーフィング

このコマンドは「おはよう」「今日の予定は?」「今日何する?」で自動発動する。

## 実行手順

以下を順番に収集・整理して、朝のブリーフィングを日本語で提示する。

### Step 0: 🔑 トークン期限チェック（毎回必ず実行）
以下のBashを実行してGoogle Calendarトークンの残り日数を確認する:

```bash
python3 << 'PYEOF'
import json, os
from datetime import datetime, timezone, timedelta
token_file = os.path.expanduser("~/.config/google-calendar-mcp/tokens.json")
try:
    with open(token_file) as f:
        tokens = json.load(f)["normal"]
    refresh_expires_in = tokens.get("refresh_token_expires_in", 604799)
    # トークンファイルの更新日時から期限を推定
    mtime = os.path.getmtime(token_file)
    created = datetime.fromtimestamp(mtime, tz=timezone.utc)
    expiry = created + timedelta(seconds=refresh_expires_in)
    now = datetime.now(timezone.utc)
    days_left = (expiry - now).days
    jst = timezone(timedelta(hours=9))
    if days_left <= 1:
        print(f"🚨 CRITICAL: Google Calendarトークンが本日期限切れです！今すぐ再認証してください。")
        print(f"   実行コマンド: npx @cocal/google-calendar-mcp auth")
    elif days_left <= 3:
        print(f"⚠️  WARNING: Google Calendarトークンあと{days_left}日で期限切れ（{expiry.astimezone(jst).strftime('%m/%d %H:%M')} JST）")
        print(f"   今日中に再認証推奨: npx @cocal/google-calendar-mcp auth")
    else:
        print(f"✅ Google Calendarトークン: あと{days_left}日有効（{expiry.astimezone(jst).strftime('%m/%d')} JST期限）")
except Exception as e:
    print(f"⚠️  トークンファイルが見つかりません。Google Calendar未接続。")
PYEOF
```

- 残り3日以内の場合: ブリーフィングの冒頭に **⚠️ 再認証アラート** として目立つ形で表示する
- 残り1日以内の場合: **🚨** で最優先タスクの1番に追加する

### Step 1: カレンダー確認
- Google Calendar MCPが接続済みの場合: 今日の予定を取得
- 未接続の場合: 「カレンダーを確認するには、Google Calendar MCPの設定が必要です。代わりに手動で今日の予定を教えてください。」と案内

### Step 2: アクティブプロジェクト確認
`10_projects/active/` フォルダ内の最新ファイルを読み込み、
各プロジェクトの現状と次のアクションを把握する。

### Step 3: メモリ確認
`memory/MEMORY.md` の「📌 今すぐやること」セクションを確認する。

### Step 4: GitHub Issues確認（設定済みの場合）
```bash
gh issue list --assignee @me --state open --limit 5
```

### Step 5: ブリーフィングを出力

以下の形式で整理して提示する:

---

## 🌅 今日のブリーフィング — YYYY年MM月DD日（曜日）

### 📅 今日の予定
（カレンダーから取得、または空欄）

### 🔥 今日の最優先タスク（3つ以内）
1.
2.
3.

### 📁 進行中プロジェクト
（active/フォルダから抽出）

### 📌 持ち越しメモ
（memory/MEMORY.mdから抽出）

### 💬 ひと言
（今日の事業状況に関連した短いインサイトや問いかけ）

---

## オプション引数
- `/daily-schedule week` — 今週の予定概要を提示
- `/daily-schedule focus` — 今日のタスクだけに絞ってシンプルに提示
