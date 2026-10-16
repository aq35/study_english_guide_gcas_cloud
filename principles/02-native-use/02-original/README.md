# 2. ネイティブ利用 — 段階2: 原文を読み解く

出典: [GCASガイド ガバメントクラウド概要解説「3.1 ガバメントクラウドとは」](https://guide.gcas.cloud.go.jp/general)
英訳は筆者の訳(公式の英訳ではない)。カタカナの `/` は息継ぎ。ルールは [linking-rules.md](../../../linking-rules.md)。
「ガイド:」はGCASガイドに書かれていること、「推論:」は筆者の推論。

## 原文を1文ずつ読む

| # | 原文 | English(筆者訳) | ポイント |
|---|---|---|---|
| 1 | ガバメントクラウドとは、…デジタル庁が整備したクラウド環境であり、選定するCSPがサービス機能やリファレンスアーキテクチャとして提供するセキュリティ対策に加え、ガバメントクラウドとして必要と考えられるセキュリティ対策やガバナンス機能が適用されるクラウド環境である。(中略あり) | The Government Cloud is a cloud environment prepared by the Digital Agency, to which the security measures and governance functions it considers necessary are applied, in addition to the security measures the selected CSPs provide as service functions and reference architectures. | CSPの機能 + ガバメントクラウドの追加分、の二層。`in addition to ...`(〜に加え) |
| 2 | ガバメントクラウドでは、選定するCSPが提供するクラウドサービスのメリットを最大限享受できるよう、必要最小限のガバナンスおよびセキュリティ設定の適用を除き、原則として独自に共通的な機能・サービスを実装し提供することは行わず、可能な限りクラウドサービスをネイティブに利用することが出来る。 | In the Government Cloud, so that the benefits of the cloud services provided by the selected CSPs can be enjoyed to the fullest, no common features or services of its own are built or offered in principle, except for the minimum necessary governance and security settings, and cloud services can be used natively as far as possible. | 学習ノートの核心。`except for ...`(〜を除き)、`in principle`(原則として)、`as far as possible`(可能な限り) |
| 3 | なお、情報システムの構築や運用は、独自にクラウドを調達する場合と同様、利用機関のポリシーや利用システムの要件を踏まえ、利用システムの責任において行う必要がある。 | Note that building and operating the information system must be done under the responsibility of the system, based on the user organization's policies and the system's requirements, just as when procuring a cloud independently. | `under the responsibility of ...`(〜の責任において) |
| 4 | 令和8年度において、ガバメントクラウドとして利用できるクラウドサービスは…AWS、Google Cloud、Microsoft Azure、OCI、さくらのクラウド…となる。 | In fiscal year Reiwa 8, the cloud services available as the Government Cloud are AWS, Google Cloud, Microsoft Azure, OCI and Sakura Cloud. | 利用できるのは5つ(令和8年度の時点) |

## 読み解きのポイント

- ガイド: ガバメントクラウドは「CSPの機能 + ガバメントクラウドが追加するセキュリティ対策とガバナンス機能」の二層(文1)。
- ガイド: 追加するのは「必要最小限」のガバナンスとセキュリティ設定だけ。独自の共通機能・サービスは、原則として作らない(文2)。
- ガイド: 目的は「CSPが提供するクラウドサービスのメリットを最大限享受できる」ようにすること。
- ガイド: 文2は「ネイティブに利用することが出来る」で終わる。「しなければならない」ではなく、「できる」という書き方。
- ガイド: ネイティブに使えても、構築や運用の責任は利用システムにある(文3)。独自にクラウドを調達する場合と同じ。
- 推論: 文2の「できる」と文3の「責任は利用システム」は、組み合わせて読む。自由に使える代わりに、システムの責任も利用側にある、という関係だと読める。学習ノート 04(責任共有モデル)とつながる。

## 5文で言ってみる

### 1 (文2の前半)
- **日本語訳**: 必要最小限のガバナンスとセキュリティ設定だけを適用する。
- **English**: It applies only the minimum governance and security settings.
- **カタカナ**: イットアプライズオンリ / ミニマムガヴァナンスアンスィキュアリティセティングズ

### 2 (文2の中盤)
- **日本語訳**: 独自の共通機能は、原則として作らない。
- **English**: It does not build its own common features, in principle.
- **カタカナ**: イットダズナットビルド / イッツオウンコモンフィーチャーズ / インプリンスィプル

### 3 (文2の後半)
- **日本語訳**: 可能な限り、クラウドサービスをネイティブに使う。
- **English**: Use cloud services natively, as much as possible.
- **カタカナ**: ユーズクラウドサーヴィスィズネイティヴリ / アズマチャズポスィブル

### 4 (文3)
- **日本語訳**: システムの構築と運用は、利用システムの責任。
- **English**: Building and operating the system is your responsibility.
- **カタカナ**: ビルディンガンオペレイティング / ザシステムイズヨアリスポンスィビリティ

### 5 (文4)
- **日本語訳**: AWSは、利用できる5つのCSPのうちの1つ。
- **English**: AWS is one of the five available CSPs.
- **カタカナ**: エイダブリューエスイズワンオヴザファイヴ / アヴェイラブルシーエスピーズ

## 語彙

| English | カタカナ | 日本語 | 詳しい説明 |
|---|---|---|---|
| native / natively | ネイティヴ / ネイティヴリ | ネイティブに | クラウドの機能をそのまま、手を加えずに使うこと |
| governance | ガヴァナンス | ガバナンス | 組織やシステムを、ルールに沿って適切に管理すること |
| minimum | ミニマム | 必要最小限 | 必要な範囲の中で、もっとも少ないこと |
| common feature | コモンフィーチャー | 共通的な機能 | 複数のシステムが共通して使う機能 |
| reference architecture | レファレンスアーキテクチャ | リファレンスアーキテクチャ | 構成の参考にできる、模範となる設計例 |
| responsibility | リスポンスィビリティ | 責任 | 自分で担い、結果に対して応える義務 |

[← ネイティブ利用へ戻る](../README.md)
