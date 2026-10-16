# GCASガイド 大事な考え方 8選(大括り)

CSPは **AWS** に特化して深掘りする。形式は1考え方につき4行(原文 / 日本語訳 / English / カタカナ)。

> カタカナ表記: 空白は息継ぎの切れ目。空白なしでつながっている部分がリンキング(例: `エイムズトゥ`, `アンダヴォイド`)。

出典: [GCASガイド](https://guide.gcas.cloud.go.jp/)(ガバメントクラウド概要解説 / セキュリティ / コスト管理)

## 1. 目指す姿

- **原文**: スマートなクラウド利用を促すことで、システムや運用のモダン化を通じたクラウド最適化によるコスト最適化…を目指す
- **日本語訳**: ガバメントクラウドは、クラウドを賢く使ってコスト最適化を目指す。
- **English**: The Government Cloud aims to cut costs by using the cloud smartly.
- **カタカナ**: ザ ガヴァメント クラウド エイムズトゥ カッ コスツ バイ ユーズィング ザ クラウド スマートリー
- 深掘り → [`principles/01-target-state/`](principles/01-target-state/README.md)

## 2. ネイティブ利用

- **原文**: 原則として独自に共通的な機能・サービスを実装し提供することは行わず、可能な限りクラウドサービスをネイティブに利用することが出来る
- **日本語訳**: 独自の共通機能は作らず、クラウドサービスをそのまま(ネイティブに)使う。
- **English**: We use cloud services natively and avoid building our own shared features.
- **カタカナ**: ウィ ユーズ クラウドサーヴィスィズ ネイティヴリ アンダヴォイド ビルディング アワオウン シェアド フィーチャーズ
- 深掘り → [`principles/02-native-use/`](principles/02-native-use/README.md)

## 3. 単純移行で終わらせない

- **原文**: 旧来のアーキテクチャを単純移行するに留まらず、マネージドサービスやコンテナ、サーバレス、マイクロサービスなどを活用してモダンアプリケーション化を検討すること
- **日本語訳**: 古いシステムをそのまま移すだけでなく、モダン化しよう。
- **English**: Don't just move old systems as they are; modernize them.
- **カタカナ**: ドウンッ ジャスト ムーヴ オウルド システムズ アズゼイアー モダナイズ ゼム
- 深掘り → [`principles/03-modernize/`](principles/03-modernize/README.md)

## 4. 責任共有モデル

- **原文**: 利用組織の責任範囲はマネージドサービスを利用することで狭めることができ、セキュリティリスクを軽減することができる
- **日本語訳**: マネージドサービスを使えば、自分たちの責任範囲とリスクは小さくなる。
- **English**: Managed services shrink your responsibility and your risk.
- **カタカナ**: マニジド サーヴィスィズ シュリンク ヨア リスポンスィビリティ アンジョア リスク
- 深掘り → [`principles/04-shared-responsibility/`](principles/04-shared-responsibility/README.md)

## 5. SaaSは無条件の正解ではない

- **原文**: SaaS利用が無条件に推奨されるわけではない…ライフサイクルコストの観点から真にコスト削減効果が発現するかを慎重に評価する必要がある
- **日本語訳**: SaaSが常に正解とは限らない。ライフサイクルコストで比べよう。
- **English**: SaaS is not always the answer; compare the lifecycle cost.
- **カタカナ**: サース イズ ナッ オールウェイズ ジ アンサー コンペア ザ ライフサイクル コスト
- 深掘り → [`principles/05-saas-not-always/`](principles/05-saas-not-always/README.md)

## 6. マルチクラウドは原則禁止

- **原文**: 1つのシステムで複数のCSPを利用するマルチクラウド構成は、コスト増加や運用の複雑化を招くため推奨しない
- **日本語訳**: 1つのシステムで複数のクラウドを使うのは、原則すすめない。
- **English**: Using multiple clouds in one system is generally not recommended.
- **カタカナ**: ユーズィング マルティプル クラウズィン ワン システム イズ ジェネラリ ナッ レコメンディッド
- 深掘り → [`principles/06-no-multicloud/`](principles/06-no-multicloud/README.md)

## 7. データの可搬性

- **原文**: アプリケーションやシステムだけを可搬にしても意味はないため、データの可搬性含めてトータルでの考慮を行う
- **日本語訳**: アプリだけでなく、データも持ち運べるようにしよう。
- **English**: Make your data portable, not just your applications.
- **カタカナ**: メイキョア デイタ ポータブル ナッ ジャスチュア アプリケイションズ
- 深掘り → [`principles/07-data-portability/`](principles/07-data-portability/README.md)

## 8. 継続的な見直しとコスト管理

- **原文**: 恒常的に適切なサイジングとなっているかを見直し / 月次で「可視化」「分析」「コストの最適化」の順に実施
- **日本語訳**: 見直しを続けよう。見える化し、分析し、最適化する。
- **English**: Keep reviewing: visualize, analyze, then optimize.
- **カタカナ**: キープ リヴューイング ヴィジュアライズ アナライズ ゼン アプティマイズ
- 深掘り → [`principles/08-continuous-review/`](principles/08-continuous-review/README.md)
