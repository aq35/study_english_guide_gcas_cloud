# 3. 単純移行で終わらせない — 段階4: AWSではどう実現するか

出典: [GCASガイド ガバメントクラウド概要解説(第4・5・6章)](https://guide.gcas.cloud.go.jp/general) / AWS 技術ガイド
カタカナの `/` は息継ぎ。ルールは [linking-rules.md](../../../linking-rules.md)。

## 核心(原文)

> 旧来のアーキテクチャを単純移行するに留まらず、マネージドサービスやコンテナ、サーバレス、マイクロサービスなどを活用してモダンアプリケーション化を検討すること

## 道筋: R1 から R2 へ

| パターン | 名称 | 位置づけ(原文) |
|---|---|---|
| R1 | Replatform(アプリ一部変更移行) | 「2段階移行における第一段階としての一時的なもの」 |
| R2 | Rebuild(アプリ再構築移行) | 「モダンアプリケーションと考える」。コンピュートは「サーバレス、コンテナを用いることを前提」 |

## AWSサンプル構成(サンプルIaC)

デジタル庁が任意で提供するサンプルIaC。運用は利用組織の責務なので、内容を理解して使う。

| 構成 | 流れ |
|---|---|
| Webアプリ | Route 53 → CloudFront → ELB(WAFv2で保護) → ECS Fargate → Aurora PostgreSQL |
| WebAPI | API Gateway → Lambda → S3 |
| 共通 | CloudWatch(監視・ログ・ダッシュボード)、KMS(暗号鍵管理) |

## 5文で言ってみる

### 1 (移行パターン)
- **日本語訳**: Rebuildが本当のモダン化。Replatformは一時的な第一歩にすぎない。
- **English**: Rebuild is the real modernization; replatform is only a temporary first step.
- **カタカナ**: リビルディズザリアルモダナイゼイション / リプラットフォームイズオンリア / テンポレリファーストステップ

### 2 (R2のコンピュート)
- **日本語訳**: R2では、サーバレスかコンテナを使う。
- **English**: For R2, use serverless or containers.
- **カタカナ**: フォーアールトゥー / ユーズサーバーレスオアコンテイナーズ

### 3 (運用監視)
- **日本語訳**: 監視は、第一段階からマネージドサービスを使う。
- **English**: Monitoring must use managed services, starting from the first step.
- **カタカナ**: マニタリングマスチューズ / マニジドサーヴィスィズ / スターティングフロムザ / ファースステップ

### 4 (バッチ処理)
- **日本語訳**: バッチは、決まった時刻ではなく、イベントで始めよう。
- **English**: Start batch jobs from events, not from a fixed time.
- **カタカナ**: スタートバッチジョブズ / フロムイヴェンツ / ナッフロマフィクスタイム

### 5 (システム間連携)
- **日本語訳**: 密結合な連携より、API連携を選ぼう。
- **English**: Prefer API integration to tightly coupled connections.
- **カタカナ**: プリファーエイピーアイインテグレイション / トゥタイトリカプルドコネクションズ

> 補足(例外): VDI / DaaS は原則使わないが、既存端末がVDI等の場合などは例外。ジョブ管理だけは、AWSならEC2のジョブ管理サーバも可(次期更改時にマネージド化が必須)。

## AWSサービス名の読み

| English | カタカナ | 役割 |
|---|---|---|
| Lambda | ラムダ | サーバレスの計算 |
| Fargate | ファーゲイト | コンテナをサーバ管理なしで実行 |
| API Gateway | エイピーアイゲイトウェイ | API の入口 |
| Aurora | オーロラ | マネージドDB |
| CloudFront | クラウドフロント | CDN |
| CloudWatch | クラウドウォッチ | 監視・ログ |
| KMS | ケーエムエス | 暗号鍵管理 |

## 語彙

| English | カタカナ | 日本語 |
|---|---|---|
| replatform | リプラットフォーム | 一部変更して移行 |
| rebuild | リビルド | 再構築 |
| serverless | サーバーレス | サーバレス |
| event-driven | イヴェントドリヴン | イベントドリブン |
| tightly coupled | タイトリカプルド | 密結合 |
| microservice | マイクロサーヴィス | マイクロサービス |

[← 単純移行で終わらせないへ戻る](../README.md)
