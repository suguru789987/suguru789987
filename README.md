# Suguru Tsutsui / 筒井 英

**Vertical SaaS PdM × AI-native Product Engineer**

飲食多店舗向け経営管理SaaSのプロダクトマネジメントを主軸に、要件定義・仕様設計・UIモック・検証プラン・CS運用までを一気通貫で担当。Claude Code をはじめとするAIツールを日常運用し、複数テーマを並列で前進させる開発スタイルです。

---

## 🎯 得意領域

| 領域 | 内容 |
|---|---|
| **Vertical SaaS** | 飲食多店舗経営管理(予算/実績/ROI/ベンチマーク/外部連携) |
| **ドメイン設計** | 会計ロジック(固定費/変動費/CVP分析)、権限階層、マルチテナント境界 |
| **仕様執筆** | DB設計+影響マップ+コード片までを含む実装直前のspec.md |
| **品質保証** | 計算根拠付き検証プラン、先出リリース/切り戻し設計 |
| **CS/UX連携** | 役割別IA再設計、ヘルプページ/FAQ、申し送り文書の一気通貫 |
| **AIネイティブ運用** | Claude Code で17テーマを並列推進、メモリ運用による永続制約管理 |

---

## 🗂 主要ポートフォリオ(テーマ別)

### 📊 経営ダッシュボード / KPI 指標

| リポジトリ | 概要 |
|---|---|
| [dashboard-metrics](https://github.com/suguru789987/dashboard-metrics) | フェーズ別ROI仕様モック(投資回収期間ベース4段階ライフサイクル + 業態×フェーズ×係数の三重決定ロジック) |

### 🏢 会計ドメイン(地代家賃 / 費用実績 / 予算)

| リポジトリ | 概要 |
|---|---|
| [rent-registration](https://github.com/suguru789987/rent-registration) | 地代家賃 仕様/モック/検証プラン18改訂 + 先出/切り戻しリリース設計 + 単月費用設定モック |
| [expense-actual-registration](https://github.com/suguru789987/expense-actual-registration) | **費用実績入力機能**(地代家賃実績モーダル + 検証 + CS申し送り表 v1/v2 + UIロジック/ヘルプ改訂申し送り 計8ファイル) |
| [rakmy-owner-registration-mock](https://github.com/suguru789987/rakmy-owner-registration-mock) | 権限設計 + 従業員画面(下記従業員向け画面系参照) |
| [budget-period-setting](https://github.com/suguru789987/budget-period-setting) | 予算年度機能(DB設計 + 18画面影響マップ + Sorbet型付きRubyコード) |
| [v15_budget_simulator](https://github.com/suguru789987/v15_budget_simulator) | 予算シミュレーター v6.4(実運用ツール、デモデータ/エクスポート機能付き) |
| [rakumy-budget-tools](https://github.com/suguru789987/rakumy-budget-tools) | 顧客予算CSV取込ツール v5.9/v6.1 + 独立仕様書2本 |
| [rakumy-budget-mapping](https://github.com/suguru789987/rakumy-budget-mapping) | 顧客予算 → ラクミー予算フォーマット変換仕様 + **科目コードマスタ** |

### 👥 人事・労務(権限階層 / 従業員 / 勤怠)

| リポジトリ | 概要 |
|---|---|
| [rakmy-owner-registration-mock](https://github.com/suguru789987/rakmy-owner-registration-mock) | **オーナー/管理者/従業員**の3階層権限画面系 + 従業員モバイル打刻UX + ヘルプIA再設計 |
| [rakmy-timerecord-import-spec](https://github.com/suguru789987/rakmy-timerecord-import-spec) | タイムレコードインポート(2テンプレート方式 + KoT/Jobcan列マッピング + 入力ガイド) |

#### 従業員向け画面フロー(見どころ)

rakmy-owner-registration-mock 内に収録:

- 招待メール → PW設定 → ログイン → 打刻開始 の完全フロー
- 出勤/退勤ボタンの打刻画面(モバイル前提UX)
- 招待リンク有効期限 **72時間** の仕様と「招待リンク無効」エラーハンドリング
- 打刻忘れ時の管理者連絡フロー
- 従業員登録/編集モーダル(v1→v5で統一デザイン化)
- 交通費入力時の**赤枠ハイライトUX**(店舗変更時の入力忘れ防止、outline CSS採用)
- 従業員アプリ向けヘルプ「はじめての方へ」「招待メールが届かない」「打刻を忘れた」

### 🔌 外部連携・データマッピング

| リポジトリ | 概要 |
|---|---|
| [rakumy-inventory-mapping](https://github.com/suguru789987/rakumy-inventory-mapping) | インフォマート → ラクミー 棚卸マッピング表 v3(商品マスタ/パイプライン) |
| [rakumy-budget-mapping](https://github.com/suguru789987/rakumy-budget-mapping) | 顧客独自予算CSV → ラクミー予算フォーマット変換ロジック + 科目コードマスタ |
| [rakmy-timerecord-import-spec](https://github.com/suguru789987/rakmy-timerecord-import-spec) | KoT/Jobcan 勤怠サービスCSVの列マッピング |

### 🗺 内部構造マッピング

| リポジトリ | 概要 |
|---|---|
| [rakumy-screen-mapping](https://github.com/suguru789987/rakumy-screen-mapping) | 会社画面/店舗画面 全機能マッピングリスト v21(21回バージョン進化) |

---

## 🧰 利用ツール・スタック

**AI:** Claude Code (Opus 4.7 / Sonnet 4.6) / Claude API  
**言語/FW:** TypeScript / JavaScript / Ruby on Rails / Sorbet / HAML / HTML / CSS  
**DB:** MySQL / Redis  
**SaaS運用:** GitHub / Notion / Linear / Google Workspace  
**モック制作:** 静的HTML/CSS/JS (JS framework非依存、対話型で意思決定スピードを優先)  
**検証/QA:** TSV検証プラン + 計算根拠記述(CVP分析など)

---

## 📊 数字で見る直近4ヶ月(2025/12〜2026/04)

- 並行推進テーマ **17件**(地代家賃/予算/タイムレコ/棚卸/ダッシュボード/権限/費用実績等)
- 検証プラン改訂回数 **18回**(地代家賃単体、2026/03/19〜04/08)
- Git コミット数 **日次5件**を記録する日もあり(UIロジック詰め時)
- 制作ドキュメント種別 **7種**(HTMLモック/Markdown spec/TSV検証/CSVマッピング/HAML/Rubyコード片/ヘルプページ)
- 画面マッピング **v21 到達**(継続的な内部構造整理)

---

## 💼 探している機会

- **Vertical B2B SaaS** の Senior PdM / Staff PdM / Head of Product
- 会計/労務/POS/多店舗管理 領域での プロダクト責任者
- **AIネイティブ運用**を前提としたプロダクト組織のリード
- **副業/アドバイザリー** でのVertical SaaS支援 (週数時間〜)

---

## 📬 Contact

- Email: s.tsutsui@rakmy.jp (業務経由)
- GitHub: [@suguru789987](https://github.com/suguru789987)

> 本ポートフォリオは在職中の学習/共有目的で公開しているものであり、機密情報はマスクまたは除外しています。
