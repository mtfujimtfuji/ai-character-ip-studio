# Claire 制作事例ノート

Claire（`ai-girlfriend-01`）の制作から、次のキャラクターIPに使える手順を引き出すための参照ノート。Claire の本文・画像はコピーせず、パスと決定番号（D-n）で参照する。

## 参照元

| 項目 | 値 |
|---|---|
| リポジトリ | `mtfujimtfuji/ai-os-projects`（ローカル: `C:\Users\hiro1\AI-OS\projects`） |
| 参照コミット | `67e9fddc57b2ea8644769758f5522c2103996ac5`（`67e9fdd`, 2026-10-15） |
| 対象ディレクトリ | `ai-girlfriend-01/` |
| 参照の書式 | `ai-os-projects@67e9fdd:ai-girlfriend-01/<パス>` |

**この版には未反映**: 参照コミット以降の作業と、作業ツリー上の未コミット変更（C1 r3 以降のビジュアル制作、C2〜C4 など）は分析対象に含めていない。

## 参照コミット時点の状況

- Character Canon: `claire` v1.4.0（CANONICAL）
- Identity 参照セット A1〜A3 完成、Everyday 層 B1〜B4 完成
- Attractive 層 C1 は修正ラウンド中（r2 の生成承認待ち）
- Business 化済み（D-25/D-26）。運用サイクルは試行段階で、20指標のうち実測できるのは1指標のみ（外部データ未接続）

## 確定した判断

| 判断 | 決定 |
|---|---|
| ポジショニング | Option E（Hybrid）。CORE=Everyday Companion、SUPPORTING=継続する物語。依存型の関係性は禁止（D-3） |
| キャラクター設定 | 14項目を一括確定し Canon 化（D-5） |
| ビジュアル方向 | Direction A（Soft Natural Artisan）（D-6） |
| 魅力表現 | Attraction Ladder 3段階（Everyday / Attractive / Intimate・Rare）と比率運用（D-7）。Level 3 は RED（D-26） |
| 参照画像の構造 | 4層 Reference Architecture（Identity / Everyday / Attractive / Ceiling）（D-8） |
| Identity の正本 | A1 正面・A2 3/4 笑顔・A3 全身の3枚のみ。B/C 層は Identity に昇格させない（D-12, D-15） |
| 制作の役割分担 | Codex＝生成、Claude Code＝QA・状態管理、ユーザー＝最終承認・公開判断（D-13） |
| 髪のドリフト対策 | 非生成の Hair Control Reference H1 を作成し、顔を除いた v2 に更新（D-21, D-24） |
| 事業方針 | Audience-led AI Character IP Business、Primary KPI＝`monthly_contribution_profit_jpy`（D-26） |

## 制作で得た学び

1. **推奨と決定を分けたことで、判断の経緯を追える。** Option・推奨は `PROPOSED`、ユーザー承認後だけ `APPROVED`。不採用案も削除せず残している。
2. **Identity 参照とスタイル参照を分けたことで、Canon が安定した。** B 層を何枚承認しても Canon は v1.4.0 のまま。
3. **文章のガードレールでは髪のドリフトを止められなかった。** B2〜B4 で色・長さのずれが繰り返し、文言を厳しくしても再発した。C1 r1 では H1 v1 の効果も「NO」と判定されている。v2 の効果はこの版では未検証。
4. **1ラウンド2候補 → 正式QA → ユーザー選定、の型が回った。** 失敗ラウンドも QA の証拠として保持している（C1 r1）。
5. **事業と計測の設計がビジュアル制作の後になった。** Business 化（D-25）はビジュアル制作の途中で、販売先・アカウントの状態は未確定のまま。

## 次のキャラクターに使えそうな点

- **段階承認の順序**: Research → Positioning → Concept → Canon → Visual Direction → Identity 参照セット → スタイル層
- **4層 Reference Architecture と、A1〜A3 の最小 Identity セットの定義**
- **ドリフトしやすい属性（髪など）は早めに非生成のコントロール参照を用意する**（文章だけに頼らない）
- **記述ルール**: 民族ラベルを使わず見た目の属性だけで書く、身体を性的な数値で記述しない
- **事業前提の早期確定**: 販売先・KPI・計測方法を、ビジュアル制作の前に最低限決めておく（学び5からの示唆）

Portland・陶芸・髪色などの Claire 固有の値は流用しない。

## 主要な参照先

| パス（`ai-girlfriend-01/` 配下） | 内容 |
|---|---|
| `.project-os/DECISIONS.md` | 決定ログ D-1〜D-26 |
| `.project-os/STATE.md` | フェーズ履歴と現状 |
| `characters/claire.md` | Character Canon v1.4.0 |
| `research/cross-rq-synthesis.md` | リサーチ6件の横断統合 |
| `strategy/attraction-ladder.md` | 魅力表現の3段階運用 |
| `visual/reference-architecture.md` | 4層 Reference Architecture |
| `visual/visual-canon-formal.md` | Visual Canon の正式記述 |
| `visual/codex-visual-production-layer.md` | Codex を使った制作フロー |
| `visual/production-control/h1-hair/` | H1 の来歴（provenance）記録 |
| `foundation/business.md`, `foundation/compliance.md` | 事業方針・コンプライアンス |
| `operations/data-connection-plan.md` | 外部データ接続の計画（未接続） |
