# 7. データの可搬性 — 段階2: 原文を読み解く

出典: [GCASガイド ガバメントクラウド概要解説「6.6.3 データ可搬性の確保」](https://guide.gcas.cloud.go.jp/general)
英訳は筆者の訳(公式の英訳ではない)。カタカナの `/` は息継ぎ。ルールは [linking-rules.md](../../../linking-rules.md)。
「ガイド:」はGCASガイドに書かれていること、「推論:」は筆者の推論。

## 原文を1文ずつ読む

| # | 原文 | English(筆者訳) | ポイント |
|---|---|---|---|
| 1 | PJMOの判断にて将来的なCSPの変更の可能性を考慮する必要がある場合は、システムやデータの可搬性について考慮に入れておくことが望ましい。 | If the PJMO needs to consider the possibility of changing CSPs in the future, it is desirable to take the portability of systems and data into account. | 「必須」ではなく「望ましい」。判断するのはPJMO。`it is desirable to ...` |
| 2 | CSPの変更を可能とする構成の検討においては、アプリケーションやシステムの可搬性に加え、データの可搬性の確保も必要である。 | When designing a configuration that makes changing CSPs possible, ensuring data portability is necessary, in addition to application and system portability. | ここは「必要である」。`in addition to ...`(〜に加え) |
| 3 | 逆に、アプリケーションやシステムだけを可搬にしても意味はないため、データの可搬性含めてトータルでの考慮を行う。 | Conversely, making only the applications and systems portable is meaningless, so consider the whole, including data portability. | 学習ノートの核心。`Conversely`(逆に)、`only`(だけ) |
| 4 | CSPの変更は、数カ月から数年かけて行うことになることが想定されるため、その前提での可搬性を検討する。 | Changing CSPs is expected to take months to years, so consider portability on that premise. | `be expected to ...`(想定される)、`on that premise`(その前提で) |

## 「データ」とは何か(原文の定義)

> アプリケーションが利用する業務データ(構造化データ、非構造化データ、設定情報、メタデータ等)を指す。

| English | カタカナ | 日本語 |
|---|---|---|
| structured data | ストラクチャドデイタ | 構造化データ |
| unstructured data | アンストラクチャドデイタ | 非構造化データ |
| configuration information | コンフィギュレイションインフォメイション | 設定情報 |
| metadata | メタデイタ | メタデータ |

## 3つの考慮点(原文の箇条書き)

| # | 原文 | English(筆者訳) |
|---|---|---|
| a | データの可搬性を確保した設計を行うこと | Design with data portability in mind. |
| b | 運用中においてもデータ可搬性を維持できる仕組みを整備すること | Put in place a mechanism to keep data portable during operation as well. |
| c | SaaS利用時においても、契約終了やサービス変更に備え、データのエクスポートや移行手段を確保すること | Even when using SaaS, secure a way to export and migrate data in case the contract ends or the service changes. |

## 読み解きのポイント

- ガイド: 目的は「経済合理性や事業戦略に応じた柔軟な対応を実現するため」。
- ガイド: CSPの変更は「数カ月から数年」かかる前提で考える。
- ガイド: 「望ましい」(文1)と「必要」(文2)は書き分けられている。変更の可能性を考えるか自体はPJMOの判断で、考えるなら、データも含めて考える。
- 推論: 「データも」と強調されているのは、アプリを移せてもデータが移せなければ乗り換えられないから。ガイドの文3を言い換えたもの。

## 5文で言ってみる

### 1 (文3の核心)
- **日本語訳**: アプリだけを可搬にしても、意味がない。
- **English**: Making only the application portable is meaningless.
- **カタカナ**: メイキングオンリジアプリケイションポータブル / イズミーニングレス

### 2 (文4の前提)
- **日本語訳**: CSPの変更には、数か月から数年かかる。
- **English**: Changing CSPs takes months to years.
- **カタカナ**: チェインジングシーエスピーズ / テイクスマンスツーイヤーズ

### 3 (考慮点a)
- **日本語訳**: データの可搬性を考えて設計する。
- **English**: Design for data portability.
- **カタカナ**: ディザインフォーデイタポータビリティ

### 4 (考慮点b)
- **日本語訳**: 運用中も、データを持ち運べる状態を保つ。
- **English**: Keep your data portable during operation, too.
- **カタカナ**: キープヨアデイタポータブル / デュアリングアペレイション / トゥー

### 5 (考慮点c)
- **日本語訳**: SaaSを使うときも、データをエクスポートできる手段を確保する。
- **English**: Even with SaaS, secure a way to export your data.
- **カタカナ**: イーヴンウィズサース / スィキュアラウェイトゥ / イクスポーチョアデイタ

## 語彙

| English | カタカナ | 日本語 | 詳しい説明 |
|---|---|---|---|
| portability | ポータビリティ | 可搬性 | システムやデータを、別の環境に持ち運べること |
| CSP (cloud service provider) | シーエスピー | クラウドサービス事業者 | AWS、Google Cloud などのクラウドを提供する事業者 |
| PJMO | ピージェイエムオー | プロジェクトチーム | 個別の情報システムのプロジェクト単位のグループ(Project Management Office) |
| premise | プレミス | 前提 | 考えるときの出発点になる条件 |
| export | イクスポート | エクスポート | データを外に取り出すこと |
| migrate | マイグレイト | 移行する | データやシステムを別の環境に移すこと |

[← データの可搬性へ戻る](../README.md)
