# 4. 責任共有モデル — 段階4: AWSではどう実現するか

出典: [GCASガイド AWS 技術ガイド「セキュリティ対策(AWS)」「予防的統制」](https://guide.gcas.cloud.go.jp/aws)
カタカナの `/` は息継ぎ。ルールは [linking-rules.md](../../../linking-rules.md)。

## 核心(原文)

> システムにEC2を使用した場合、OS、ミドルウェアなどが利用組織側の責任範囲となり、その部分のセキュリティ対策が必要となる。EC2の代わりにLambda、API Gateway、RDS、DynamoDB、ECS(Fargate)などのマネージドサービスを用いることで責任範囲を狭め、セキュリティリスクを軽減できる。

## 図解: EC2 から マネージドサービスへ

| 構成 | 構成要素 | 利用組織の責任範囲 |
|---|---|---|
| アンマネージド | クライアント → EC2(アプリ) → EC2(DB) | OS / ミドルウェア / 高可用性 / アプリ / データ / サービス設定 の **6つ** |
| マネージド | クライアント → API Gateway → ECS(Fargate) または Lambda → DynamoDB | アプリ / データ / サービス設定 の **3つ** |

OS・ミドルウェア・高可用性の管理が不要になる。

## 4文で言ってみる

### 1
- **原文の要点**: EC2ではOS・ミドルウェアが利用組織の責任。
- **日本語訳**: EC2だと、OSとミドルウェアは自分たちの責任になる。
- **English**: With EC2, the OS and middleware are your responsibility.
- **カタカナ**: ウィズイーシーツー / ジオウエスアンドミドルウェア / アーヨアリスポンスィビリティ

### 2
- **原文の要点**: Lambda・RDS・DynamoDB等なら、責任は アプリ・データ・サービス設定 の3つ。
- **日本語訳**: Lambda、RDS、DynamoDBなら、自分たちの責任はアプリとデータと設定だけ。
- **English**: With Lambda, RDS and DynamoDB, only the app, data and settings are yours.
- **カタカナ**: ウィズラムダ / アールディーエスアンダイナモディービー / オンリジアプ / デイタアンセティングズ / アーヨアズ

### 3
- **原文の要点**: マネージドでも、サービスの設定は利用者の責任(共通ガイド)。
- **日本語訳**: マネージドサービスでも、設定は自分たちの責任のまま。
- **English**: Even with managed services, the settings are still your responsibility.
- **カタカナ**: イーヴンウィズマニジドサーヴィスィズ / ジセティングズ / アースティルヨアリスポンスィビリティ

### 4
- **原文の要点**: 公共分野では、責任がなくても説明責任を問われることがある(共通ガイド)。
- **日本語訳**: 責任範囲は小さくなっても、説明責任は問われるかもしれない。
- **English**: Your responsibility shrinks, but you may still be held accountable.
- **カタカナ**: ヨアリスポンスィビリティシュリンクス / バッチュマイスティルビーヘルドアカウンタブル

### 5 (ガバメントクラウド層の仕事)
- **原文**: ガバメントクラウド(AWS)では、Organizations、SCP、Control Towerを使用し、予防的統制を実現している。
- **日本語訳**: ガバメントクラウドは、SCPとControl Towerで、危ない操作を前もって止めている。
- **English**: The Government Cloud applies guardrails with SCPs and Control Tower.
- **カタカナ**: ザガヴァメントクラウド / アプライズガードレイルズ / ウィズエスシーピーズアンコントロールタワー

## 3層で整理する

| 層 | 担当 | AWSでの例 |
|---|---|---|
| 利用組織 | アプリ・データ・サービス設定・(EC2なら)OS/ミドルウェア | Lambda、RDS、DynamoDB、ECS(Fargate) の設定 |
| ガバメントクラウド | ガードレール、テンプレート/IaC、環境払い出し | Organizations、SCP(例: 東京/大阪リージョン以外は原則使用不可、アクセスキー作成不可)、Control Tower の予防コントロール |
| CSP | 物理基盤、マネージドサービスの基盤 | AWS |

## 語彙

| English | カタカナ | 日本語 |
|---|---|---|
| shared responsibility model | シェアドリスポンスィビリティマダル | 責任共有モデル |
| managed service | マニジドサーヴィス | マネージドサービス |
| middleware | ミドルウェア | ミドルウェア |
| guardrail | ガードレイル | ガードレール |
| preventive control | プリヴェンティヴコントロウル | 予防的統制 |
| accountable | アカウンタブル | 説明責任がある |

[← 責任共有モデルへ戻る](../README.md)
