---
marp: true
theme: default
paginate: true
backgroundColor: "#FFFFFF"
style: |
  /* ================================================================
     UCHI STRATEGIC DECK  —  Professional Consulting Theme
     McKinsey-inspired: action titles, pyramid logic, clean data viz
     ================================================================ */

  section {
    font-family: -apple-system, 'Hiragino Kaku Gothic ProN', 'Helvetica Neue', Arial, sans-serif;
    font-size: 18px;
    padding: 52px 72px 52px;
    background: #FFFFFF;
    color: #1C1C1E;
    position: relative;
  }

  /* ── GOLD-NAVY TOP RULE ── */
  section::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 5px;
    background: linear-gradient(90deg, #1B3A5C 60%, #C8A951 100%);
  }

  /* ── ACTION TITLE ── */
  h1 {
    font-size: 25px;
    font-weight: 700;
    color: #1B3A5C;
    line-height: 1.3;
    margin: 0 0 22px 0;
    padding-bottom: 12px;
    border-bottom: 2.5px solid #C8A951;
    letter-spacing: -0.2px;
  }

  h2 {
    font-size: 17px;
    font-weight: 600;
    color: #2E6DA4;
    margin: 16px 0 8px 0;
  }

  h3 {
    font-size: 15px;
    font-weight: 600;
    color: #1B3A5C;
    margin: 12px 0 5px 0;
  }

  /* ── TABLES ── */
  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 15px;
    margin: 8px 0;
  }
  th {
    background: #1B3A5C;
    color: #FFFFFF;
    padding: 9px 14px;
    font-weight: 600;
    font-size: 14px;
    text-align: left;
    letter-spacing: 0.2px;
  }
  td {
    padding: 8px 14px;
    border-bottom: 1px solid #EBEBEB;
    vertical-align: middle;
  }
  tr:nth-child(even) td { background: #F7F8FA; }

  /* ── INSIGHT BOX (blockquote) ── */
  blockquote {
    border-left: 4px solid #C8A951;
    background: #FDFBF2;
    margin: 14px 0 0 0;
    padding: 11px 18px;
    border-radius: 0 4px 4px 0;
    font-size: 16px;
    font-weight: 500;
    color: #1B3A5C;
    line-height: 1.5;
  }

  /* ── LISTS ── */
  ul { margin: 4px 0; padding-left: 18px; }
  ul li { margin-bottom: 7px; line-height: 1.6; }
  ul li::marker { color: #C8A951; }

  /* ── DATA VIZ (pre/code blocks) ── */
  pre {
    background: #F4F6F9;
    border-left: 3px solid #2E6DA4;
    padding: 13px 18px;
    border-radius: 0 5px 5px 0;
    font-size: 13.5px;
    line-height: 1.85;
    color: #1C1C1E;
    margin: 10px 0;
  }
  pre code { background: none; padding: 0; }
  code {
    background: #F0F4F8;
    padding: 2px 6px;
    border-radius: 3px;
    font-size: 14px;
    color: #1B3A5C;
  }

  /* ── STRONG / EM ── */
  strong { color: #1B3A5C; font-weight: 700; }
  em { color: #9B6B00; font-style: normal; font-weight: 600; }

  /* ── COVER SLIDE ── */
  section.cover {
    background: linear-gradient(145deg, #0B1E30 0%, #1B3A5C 55%, #2C5880 100%);
    color: #FFFFFF;
    padding: 80px 90px;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
  }
  section.cover::before {
    background: linear-gradient(90deg, #C8A951 0%, rgba(200,169,81,0.25) 100%);
    height: 4px;
  }
  section.cover h1 {
    font-size: 46px;
    color: #FFFFFF;
    border: none;
    padding: 0;
    margin: 0 0 14px 0;
    letter-spacing: -0.8px;
    line-height: 1.15;
  }
  section.cover p { color: rgba(255,255,255,0.55); font-size: 13.5px; margin: 0; }

  /* ── SECTION DIVIDER ── */
  section.section {
    background: #1B3A5C;
    color: #FFFFFF;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    padding: 72px 96px;
  }
  section.section::before {
    background: linear-gradient(90deg, #C8A951 0%, rgba(200,169,81,0.12) 100%);
  }
  section.section h2 {
    font-size: 13px;
    color: #C8A951;
    letter-spacing: 4px;
    text-transform: uppercase;
    font-weight: 500;
    margin: 0 0 18px 0;
  }
  section.section h1 {
    font-size: 50px;
    color: #FFFFFF;
    border: none;
    padding: 0;
    margin: 0 0 22px 0;
    line-height: 1.12;
    font-weight: 700;
    letter-spacing: -0.8px;
  }
  section.section p {
    color: rgba(255,255,255,0.60);
    font-size: 16px;
    max-width: 580px;
    line-height: 1.65;
    margin: 0;
  }

  /* ── EXEC SUMMARY ── */
  section.exec {
    background: #F7F9FC;
    padding: 44px 68px;
  }

  /* ── CLOSING ── */
  section.closing {
    background: linear-gradient(145deg, #0B1E30 0%, #1B3A5C 100%);
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 80px;
  }
  section.closing::before {
    background: linear-gradient(90deg, #C8A951 0%, rgba(200,169,81,0.3) 100%);
  }
  section.closing h1 {
    color: #C8A951;
    border: none;
    font-size: 42px;
    padding: 0;
    margin-bottom: 20px;
    letter-spacing: -0.5px;
  }
  section.closing p {
    color: rgba(255,255,255,0.68);
    font-size: 18px;
    max-width: 680px;
    line-height: 1.7;
    margin: 0;
  }

---

<!-- _class: cover -->

# 🍵 UCHI Daytime Café
## 遊休6時間を年間SGD 75,000の利益エンジンへ転換する

<br><br><br><br>

**シンガポール バー昼間活用 戦略的事業評価**
UCHI Singapore &nbsp;｜&nbsp; 2026年3月 &nbsp;｜&nbsp; Confidential

---

<!-- _class: exec -->

# 今すぐ承認すべき理由：市場・オペレーション・財務の3軸が全て揃っている

<div style="display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-top:4px">

<div style="background:#1B3A5C;border-radius:8px;padding:20px 22px;color:white">

**🔍 SITUATION**
既存バースペースは毎日11:00〜17:00の**6時間が未活用**。
設備・立地・ブランドという高価値資産が日中に眠っている。

</div>

<div style="background:#7B4000;border-radius:8px;padding:20px 22px;color:white">

**⚡ COMPLICATION**
シンガポールのかき氷市場は**年+17%成長中**。
競合はいずれも「日本酒文化の深度」を持てず、プレミアムポジションが空白のまま。

</div>

<div style="background:#27AE60;border-radius:8px;padding:20px 22px;color:white">

**✅ RESOLUTION**
昼間を**日本茶×本格かき氷カフェ**に転換。
追加家賃ゼロ・追加設備投資SGD 35,000のみで即時開業可能。

</div>

<div style="background:#2E6DA4;border-radius:8px;padding:20px 22px;color:white">

**💰 IMPACT**
月次営業利益 **SGD 6,250**（BASEシナリオ）
投資回収 **5.6ヶ月**  ／  年間ROI **114%**

</div>

</div>

> **推奨：本週中に事業承認し、12週間の開業クリティカルパスを起動せよ。**

---

# アジェンダ

<br>

<div style="display:grid;grid-template-columns:48px 1fr;gap:12px 20px;align-items:start;font-size:17px;line-height:1.7">

<div style="background:#1B3A5C;color:#C8A951;border-radius:50%;width:40px;height:40px;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:18px">1</div>
<div><strong>市場機会</strong>　— シンガポール特殊環境と成長トレンドの検証</div>

<div style="background:#1B3A5C;color:#C8A951;border-radius:50%;width:40px;height:40px;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:18px">2</div>
<div><strong>競合ポジショニング</strong>　— 誰も埋められていない空白地帯の特定</div>

<div style="background:#1B3A5C;color:#C8A951;border-radius:50%;width:40px;height:40px;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:18px">3</div>
<div><strong>オペレーションモデル</strong>　— メニュー・チーム・空間転換の設計</div>

<div style="background:#1B3A5C;color:#C8A951;border-radius:50%;width:40px;height:40px;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:18px">4</div>
<div><strong>財務ケース</strong>　— 投資・損益・ROIの詳細試算</div>

<div style="background:#1B3A5C;color:#C8A951;border-radius:50%;width:40px;height:40px;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:18px">5</div>
<div><strong>実行計画</strong>　— 12週間クリティカルパスと意思決定事項</div>

</div>

---

<!-- _class: section -->

## SECTION 1 OF 5

# 市場機会

シンガポール特有の構造的需要と
かき氷市場の成長トレンドを検証する

---

# シンガポールのスペシャルティカフェ市場は拡大を続け、かき氷は最速成長セグメントである

<div style="display:grid;grid-template-columns:1fr 1fr;gap:28px">

<div>

**市場規模と成長**

| セグメント | 規模 | 成長率 |
|-----------|------|--------|
| SG F&B 全体 | ~SGD 40B | +4% YoY |
| スペシャルティカフェ | ~SGD 3.6B | **+7–9%** |
| 日本茶・抹茶 | 成熟・安定 | **+5%** |
| かき氷（Kakigori） | 急成長期 | **+17%** |

*かき氷だけが他セグメントを大幅に上回る成長を維持している*

</div>

<div>

**Kakigori 検索量インデックス（2022=100）**

```
2022  ████████████████████  100
2023  ████████████████████████████████  157  ▲57%
2024  ████████████████████████████████████████  203  ▲29%
2025  ████████████████████████████████████████████████  238  ▲17%
```

*3年間で累計+138%。まだ成熟に達していない*

</div>

</div>

> **示唆：かき氷市場は成長フェーズの中盤。あと2〜3年は参入優位が保てる窓が開いている。**

---

# SGミレニアル女性はカフェ市場で最高のLTV（年間顧客生涯価値）を持つセグメントである

<div style="display:grid;grid-template-columns:1fr 1fr;gap:28px">

<div>

**セグメント別 顧客生涯価値（LTV）試算**

| セグメント | 来店頻度 | 客単価 | 年間LTV |
|-----------|---------|--------|--------|
| **SG在住ミレニアル女性** | **2.5回/月** | **SGD 25** | **SGD 750** |
| Z世代（18-24歳） | 1.2回/月 | SGD 18 | SGD 259 |
| 日本人駐在員 | 1.8回/月 | SGD 30 | SGD 648 |
| 観光客 | 1.0回/訪問 | SGD 27 | SGD 27 |
| 中国系富裕層 | 1.0回/月 | SGD 35 | SGD 420 |

</div>

<div>

**なぜミレニアル女性が最優先か**

- 🇯🇵 日本旅行経験率 **60%以上**。本物志向が強い
- 📸 Instagramでの食体験シェアが活発 → **UGC生成でゼロコスト獲得**
- 🔄 一度ファン化すると月複数回のリピーター（解約率が低い）
- 👥 グループ来店で**1訪問あたり複数席**を占有

> **10人の忠実なミレニアル女性 = 年間 SGD 7,500 の安定収益源**

</div>

</div>

---

# 気候と文化という2つの構造的優位が、シンガポールの通年かき氷需要を保証する

<div style="display:grid;grid-template-columns:1fr 1fr;gap:28px">

<div>

**気候要因（他市場にない優位性）**

```
平均気温  28–32°C  ──通年──▶  冷たいデザート需要が絶えない
相対湿度  75–85%   ──通年──▶  清涼感への恒常的ニーズ
季節変動  最小限           ▶  売上の季節ブレが±15%以内
```

日本・韓国のかき氷は「夏の風物詩」に過ぎないが、
**シンガポールは1年365日が「かき氷の季節」**。

</div>

<div>

**文化要因（参入障壁が低い理由）**

- 🍧 地元伝統「アイスカチャン」がかき氷文化の素地を形成
- 🌸 日本文化リテラシーが高い（日本アニメ・旅行・J-pop）
- 💻 SNS起点のグルメ探索行動が定着
- 🥢 「本物の日本体験」への支払い意欲が高い（Hvalaの成功が証明）

> **UCHIへの示唆：カテゴリー教育不要。「本格×大人」の差別化だけに集中できる。**

</div>

</div>

---

<!-- _class: section -->

## SECTION 2 OF 5

# 競合ポジショニング

4社の競合はすべて同じ弱点を持ち、
UCHIだけが埋められるポジションが存在する

---

# 4社の競合はいずれも「日本酒文化の深度」を欠いており、UCHIが独占できる空白が存在する

| | Hvala | Matchaya | Tsujiri | Uji Tokiwa | **UCHI（目標）** |
|--|--|--|--|--|--|
| 日本茶品質 | ★★★★★ | ★★★★★ | ★★★ | ★★★★★ | **★★★★★** |
| かき氷品質 | ★★★ | ★★ | ★★★★ | ★★★★★ | **★★★★★** |
| 大人の演出 | ★★★ | ★★★ | ★ | ★★★ | **★★★★★** |
| 日本酒文化との接続 | ✗ | ✗ | ✗ | ✗ | **✓ 独占** |
| 産地ストーリーテリング | △ | ★★ | ✗ | ★★★ | **★★★★★** |
| 価格帯 | SGD 15–22 | SGD 18–28 | SGD 12–18 | SGD 16–22 | **SGD 18–32** |
| 主な弱点 | かき氷弱い | 価格最高・狭い | チェーン感・体験薄 | 認知度低い | — |

> **UCHIの独自ポジション：「精神性を伴う日本の飲食文化の総体」を体現する唯一の店舗**

---

# UCHIの競合優位は既存資産に根ざしており、資金では買えないモートである

<div style="display:grid;grid-template-columns:1fr 1fr;gap:24px">

<div>

**UCHI固有の資産（競合が模倣不可）**

### 🍶 日本酒の知識・ネットワーク
茶と酒は同じ「産地×作り手」の語り口で話せる。
日本の蔵元・農家との関係が「茶農家ネットワーク」へ転用可能。

### 🏠 バーの内装・雰囲気
既存の「大人の日本空間」は再現コスト数百万円。
競合がゼロから構築しようとしても5年かかる。

### 📖 ブランドの文化的信頼性
「日本のお酒を知っているUCHI」が「日本のお茶を勧める」— 顧客は信じる。

</div>

<div>

**5つの持続的差別化レバー**

| レバー | 競合の対応難易度 |
|--------|---------------|
| 産地ストーリー（テロワール） | 🔴 高（知識・仕入先が必要） |
| かき氷×日本酒ペアリング演出 | 🔴 高（酒の知識がない） |
| 季節限定メニューの速度 | 🟡 中（在庫管理が複雑） |
| 夜バーとのクロスセル設計 | 🔴 高（昼夜両業態が必要） |
| 本格製氷クオリティ | 🟡 中（設備投資で対応可能） |

</div>

</div>

> **示唆：UCHIが3年で確立すれば、競合が追いつくまでさらに3年かかる。早期参入の価値は大きい。**

---

<!-- _class: section -->

## SECTION 3 OF 5

# オペレーションモデル

自然な客単価 SGD 25 を生む4階層メニューと、
3名体制の精鋭チームの設計

---

# 4カテゴリのメニューアーキテクチャが、顧客を自然にSGD 25の支出へと誘導する

<div style="display:grid;grid-template-columns:1fr 1fr;gap:24px">

<div>

**購買経路の設計（アップセルラダー）**

```
顧客の購買決定プロセス:

STEP 1  エントリー（必ず注文）
        茶ラテ / ほうじ茶ラテ
        SGD 8–10  →  来店障壁を下げる

STEP 2  メイン購入（85%が追加）
        かき氷（スタンダード）
        SGD 16–20  →  利益の中核

STEP 3  アップグレード（40%が選択）
        かき氷（プレミアム）or ティーセット
        SGD 24–32  →  高利益商品

STEP 4  アドオン（55%が追加）
        上生菓子・わらび餅
        SGD 6–10  →  高マージン補完

  ─────────────────────────────────
  平均客単価：SGD 8 + SGD 17 = SGD 25
```

</div>

<div>

**主要メニューと利益構造**

| 商品 | 価格 | 原価率 | 貢献利益 |
|------|------|--------|--------|
| 抹茶・ほうじ茶ラテ | SGD 8–10 | 28% | SGD 6–7 |
| かき氷（定番） | SGD 16–20 | 30% | SGD 11–14 |
| かき氷（プレミアム） | SGD 24–32 | 25% | SGD 18–24 |
| ティーセット | SGD 28–36 | 22% | SGD 22–28 |
| 和菓子（アドオン） | SGD 6–10 | 20% | SGD 5–8 |

**ポートフォリオ平均原価率：28%**
（業界標準30-35%を下回る高利益構造）

</div>

</div>

---

# 3名の精鋭チームと30分の空間転換プロトコルで昼夜二毛作を実現する

<div style="display:grid;grid-template-columns:1fr 1fr;gap:24px">

<div>

**昼間シフト体制（11:00〜17:00）**

| 役割 | コア責任 | 採用要件 |
|------|---------|---------|
| **Tea Bar Lead** | 抹茶点前・茶ラテ・品質統括 | 日本茶知識 or 意欲 |
| **Kakigori Spec.** | かき氷製造・スピード管理 | 業務経験優遇 |
| **Floor Lead** | オーダー・会計・体験管理 | 英語必須 |

**14日間トレーニングプログラム**

```
Week 1（座学）: 茶産地・グレード・淹れ方・
                ストーリーテリング英語表現
Week 2（実技）: 茶ラテ・かき氷・盛り付け・
                HACCP・衛生管理
```

</div>

<div>

**空間転換：30分で昼夜を切り替える**

```
10:00〜10:30（開店準備）
  ■ 照明  → 3,500K 白昼光に切替
  ■ BGM   → 尺八・琴・和の音楽
  ■ 棚    → 日本酒 → 茶缶・急須に転換
  ■ 卓上  → 麻リネン、茶道具セット

17:00〜17:30（夜の準備）
  ■ かき氷機 分解・洗浄（15分）
  ■ 照明  → 2,200K 電球色に復帰
  ■ 棚    → 日本酒ディスプレイに戻す
  ■ 発注リスト → 夜バースタッフへ引継ぎ
```

> **追加固定コスト：家賃ゼロ、設備共用。唯一の追加固定費は人件費SGD 9,000/月**

</div>

</div>

---

<!-- _class: section -->

## SECTION 4 OF 5

# 財務ケース

SGD 35,000の投資が
年間SGD 75,000を生み出す根拠

---

# SGD 35,000の初期投資は詳細積み上げに基づく保守的試算であり、回収は確実に見込める

<div style="display:grid;grid-template-columns:1fr 1fr;gap:28px">

<div>

**投資内訳（ボトムアップ積み上げ）**

| カテゴリ | 金額（SGD） | 備考 |
|---------|-----------|------|
| かき氷機（HC-8E + バックアップ） | 5,000 | 業務用・2台体制 |
| 業務用製氷機（Hoshizaki） | 6,000 | 純氷品質の核心 |
| 茶道具・冷蔵ショーケース | 5,500 | 品質演出の必須投資 |
| 空間改装（照明・フォトスポット） | 6,000 | 昼夜切替の基盤 |
| 和の食器・器（益子焼等） | 3,500 | ブランド体験を構成 |
| スタッフトレーニング | 2,000 | 14日間プログラム |
| 初回食材・備品在庫 | 4,000 | 1ヶ月分 |
| 許認可・マーケティング | 3,000 | SFA申請 + 開業PR |
| **合計（中央値）** | **35,000** | 保守的試算 |

</div>

<div>

**投資と収益のバランス**

```
INVESTMENT WATERFALL

  初期投資       月次コスト     月次利益

  SGD 35,000
       │          SGD 17,500   SGD 6,250
       │          ／月（BASE）  ／月（BASE）
       │
       ▼
  ──────────────────────────────────
  ÷ 6,250 = 5.6ヶ月で投資回収完了

  残り6.4ヶ月で稼ぐ純利益（Year 1）:
  6,250 × 6.4 = SGD 40,000

  Year 1 合計リターン:
  75,000 - 35,000 = SGD 40,000 純増
  ROI = 114%
```

</div>

</div>

---

# 3つのシナリオはすべて保守的仮定に基づき、BASEケースでも極めて健全な収益性を示す

<div style="margin-top:8px">

| | **保守的** | **BASE（目標）** | **楽観的** |
|--|--|--|--|
| 1日来客数 | 20名 | **38名** | 55名 |
| 座席稼働率 | 54% | **73%** | 85%+ |
| 客単価 | SGD 22 | **SGD 25** | SGD 28 |
| **月次売上** | SGD 11,000 | **SGD 23,750** | SGD 38,500 |
| 月次総コスト | SGD 14,700 | **SGD 17,500** | SGD 21,000 |
| **月次営業利益** | **▲SGD 3,700** | **+SGD 6,250** | **+SGD 17,500** |
| **年間営業利益** | 損益分岐まで3ヶ月 | **SGD 75,000** | **SGD 210,000** |
| **投資回収期間** | 8ヶ月 | **5.6ヶ月** | **2ヶ月** |

</div>

> **重要：保守シナリオでも3ヶ月以内に黒字転換。Year 1で必ず投資回収できる事業構造。**

---

# 1日28名という損益分岐点は、既存キャパシティの76%以下であり到達難易度は低い

<div style="display:grid;grid-template-columns:1fr 1fr;gap:28px">

<div>

**損益分岐点の論理**

```
月次総コスト（固定・変動込み）
= SGD 17,500

BEP来客数
= 17,500 ÷ (25 × 25日)
= 700名/月
= 28名/日

─────────────────────────────────
稼働キャパシティ
= 25席 × 1.5回転 × 6時間
= 37名/日

BEP余裕
= 37 - 28 = +9名/日（24%の安全マージン）
```

</div>

<div>

**競合の実績から見た達成可能性**

```
1日あたり来客数のベンチマーク

HvalaのMBFC店    ████████████████ 60–80名
Tsujiriのモール店  ████████████ 45–60名
Uji Tokiwa       ████████ 30–50名
                  ─────────────────────
UCHIのBEP水準     ████████ 28名/日  ← 業界最低水準

Hvala BEP比       28 ÷ 70 = 40%の集客で黒字化
```

> **UCHIは業界最高の競合の40%の来客数で黒字。ハードルは業界で最も低い。**

</div>

</div>

---

<!-- _class: section -->

## SECTION 5 OF 5

# 実行計画

今週から動けば、12週間後に
グランドオープンを迎えられる

---

# 12週間の開業は3本の独立したワークストリームが並行して進む精密なクリティカルパスである

| ストリーム | Week 1–2 | Week 3–5 | Week 6–8 | Week 9–10 | Week 11 | **Week 12** |
|-----------|---------|---------|---------|---------|---------|------------|
| 🏛️ **法務・許認可** | URA相談・SPF確認 🔴 | Food Shop Licence 申請提出 | ← 審査中（4–6週） | **Licence 取得** | 店内掲示 | ✅ |
| 🔨 **設備・改装** | 施工業者選定 | 改装着工・かき氷機発注 | 機材納品・設置 | 試運転・微調整 | ✅ | ✅ |
| 👥 **人材・仕入れ** | FHO確認・採用要件確定 | サプライヤー選定・RFQ | 採用確定・仕入契約 | **14日間トレーニング** | ソフトオープン🎊 | **GRAND OPEN** 🎉 |

<div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:14px;margin-top:16px;font-size:15px">

<div style="background:#FEF3E2;border-left:4px solid #E67E22;padding:10px 14px;border-radius:0 4px 4px 0">
🔴 <strong>Week 1 必須</strong><br>URA相談 + SPF問い合わせ<br>この2件を今週予約しないと<br>全体が最大8週間遅延する
</div>

<div style="background:#E8F5E9;border-left:4px solid #27AE60;padding:10px 14px;border-radius:0 4px 4px 0">
🟢 <strong>並行実行可能</strong><br>設備・人材は法務と独立<br>Week 2から同時進行で<br>クリティカルパスを短縮
</div>

<div style="background:#E8F4FD;border-left:4px solid #2E6DA4;padding:10px 14px;border-radius:0 4px 4px 0">
🔵 <strong>Week 11 ソフトオープン</strong><br>インフルエンサー招待・<br>SNS先行告知・<br>口コミ種まきを実施
</div>

</div>

---

# 3つのリスクは事前対処で影響を最小化できる。うち2つは今週中に行動開始が必要だ

| リスク | 確率 | 影響 | 今週中の対処アクション |
|-------|------|------|----------------------|
| **URA 用途変更が必要と判定される** | 中 | 高（4〜8週間の遅延） | **今週中にURA Pre-application Consultation予約** |
| **Liquor Licenceがカフェ業態を制限** | 低〜中 | 高（業態変更不可） | **今週中にSPFへ条件確認の問い合わせ** |
| かき氷機の故障 | 中 | 中（日次売上損失） | バックアップ機常備 + メンテナンス契約 |
| 日本食材の輸入遅延 | 低〜中 | 低（代替品で対応可） | 複数サプライヤー確保・3ヶ月先行発注 |
| 開業初期の低集客 | 中 | 中（回収期間延長） | 開業6ヶ月の運転資金SGD 22,200を確保 |
| 主要スタッフの離職 | 低 | 中 | マニュアル化・補欠採用の並行実施 |

> **「今週始めれば12週でオープン」— 逆に言えば、今週動かない1日が開業を1日遅らせる。**

---

# 今週中に3つの意思決定を行うことで、SGD 75,000/年の収益ストリームが動き出す

<div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:18px;margin-top:12px">

<div style="border:2px solid #C8A951;border-radius:8px;padding:20px 18px">

### Decision 1
**事業の承認**

- 開業可否の最終判断
- 予算上限の設定
  （推奨：SGD 35,000〜45,000）
- 開業目標日の確定
  （推奨：12週後）

*期限：今週中*

</div>

<div style="border:2px solid #2E6DA4;border-radius:8px;padding:20px 18px">

### Decision 2
**法務2件の起動**

- URA事前相談の予約
  → 用途変更の要否判定
- SPFへの問い合わせ
  → 既存Liquor Licenceの
    昼間カフェ業態への適用確認

*期限：今週中*

</div>

<div style="border:2px solid #27AE60;border-radius:8px;padding:20px 18px">

### Decision 3
**スタッフ方針の決定**

- 昼間スタッフの採用方針
  （新規採用 or 夜バーとの兼務）
- Food Hygiene Officer
  の資格保有者確認
- 採用予算・スケジュール

*期限：Week 2末*

</div>

</div>

> **この3決定がないと、クリティカルパスは動かない。承認から最速12週でオープン可能。**

---

<!-- _class: closing -->

# 推奨：本事業を承認し、今週から12週間のクリティカルパスを起動せよ

<br>

<div style="display:grid;grid-template-columns:1fr 1fr 1fr 1fr;gap:16px;margin:20px 0">

<div style="background:rgba(255,255,255,0.1);border:1px solid rgba(200,169,81,0.5);border-radius:8px;padding:18px 12px;text-align:center">
<div style="font-size:38px;font-weight:700;color:#C8A951">SGD<br>35K</div>
<div style="font-size:12px;color:rgba(255,255,255,0.6);margin-top:6px">初期投資<br>（中央値）</div>
</div>

<div style="background:rgba(255,255,255,0.1);border:1px solid rgba(200,169,81,0.5);border-radius:8px;padding:18px 12px;text-align:center">
<div style="font-size:38px;font-weight:700;color:#C8A951">28名</div>
<div style="font-size:12px;color:rgba(255,255,255,0.6);margin-top:6px">損益分岐点<br>（1日あたり）</div>
</div>

<div style="background:rgba(255,255,255,0.1);border:1px solid rgba(200,169,81,0.5);border-radius:8px;padding:18px 12px;text-align:center">
<div style="font-size:38px;font-weight:700;color:#C8A951">5.6ヶ月</div>
<div style="font-size:12px;color:rgba(255,255,255,0.6);margin-top:6px">投資回収期間<br>（BASEケース）</div>
</div>

<div style="background:rgba(255,255,255,0.1);border:1px solid rgba(200,169,81,0.5);border-radius:8px;padding:18px 12px;text-align:center">
<div style="font-size:38px;font-weight:700;color:#C8A951">114%</div>
<div style="font-size:12px;color:rgba(255,255,255,0.6);margin-top:6px">Year 1 ROI<br>（BASEケース）</div>
</div>

</div>

遊休資産の転換 × 市場の成長 × 競合の空白地帯 — この3条件が同時に揃う機会は長くは続かない

---

<!-- _class: cover -->

# Appendix

## 参考資料・詳細データ

<br><br><br><br>

UCHI Singapore &nbsp;｜&nbsp; 2026年3月

---

# 競合プロファイル詳細：4社の強み・弱み・価格帯

| | Hvala | Matchaya | Tsujiri | Uji Tokiwa |
|--|--|--|--|--|
| **拠点数** | 3店舗（CBD等） | 1店舗（Ion） | 3店舗（モール） | 1店舗（Robertson） |
| **主力商品** | 煎茶・茶ラテ・パフェ | 有機抹茶ラテ・パフェ | 抹茶ソフト・パフェ | 宇治抹茶かき氷 |
| **価格帯** | SGD 8–22 | SGD 9–28 | SGD 5–20 | SGD 16–28 |
| **主な客層** | SG在住ミレニアル | 富裕層・有機志向 | 観光客・ファミリー | 日本文化ファン |
| **強み** | ブランド力・品質・店舗数 | 有機認証・高品質 | 老舗ブランド・立地 | かき氷専門・本格品質 |
| **最大の弱み** | かき氷少・SNS演出弱 | 高価格・スペース狭い | ファストフード感 | 認知度低・立地限定 |
| **UCHI対比** | 茶品質同等・かき氷で優位 | 価格帯近い・差別化可能 | 価格上位で共存可 | 直接競合に最も近い |

---

# シンガポール食品関連ライセンス取得の標準プロセス

| ライセンス | 申請先 | 処理期間 | 費用（SGD） | 優先度 |
|-----------|--------|---------|-----------|--------|
| **Food Shop Licence** | SFA / GoBusiness | 4〜6週間 | 400/年 | 🔴 必須・最優先 |
| **Food Hygiene Officer 配置** | SFA | 採用次第 | — | 🔴 必須（申請要件） |
| **Basic Food Hygiene（全員）** | SFA認定機関 | 1日 | 15–30/人 | 🔴 必須 |
| **URA Change of Use** | URA | 4〜8週間 | 200〜 | 🟡 要確認 |
| **Liquor Licence 条件確認** | SPF | 即時（照会） | — | 🟡 要確認（今週） |
| TradeNet 輸入申請（日本食材） | Singapore Customs | 3〜7営業日 | 微額 | 🟡 Week 3開始 |
| Halal Certification | MUIS | 3〜6ヶ月 | — | ⚪ 任意 |
