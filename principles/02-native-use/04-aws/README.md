# 2. ネイティブ利用 — 段階4: AWSではどう実現するか

出典: [GCASガイド AWS技術ガイド(ガバナンス・セキュリティ / 予防的統制 / 発見的統制 / ユーザー管理)](https://guide.gcas.cloud.go.jp/aws)
カタカナの `/` は息継ぎ。ルールは [linking-rules.md](../../../linking-rules.md)。

## 核心(原文)

> 原則として独自に共通的な機能・サービスを実装し提供することは行わず、可能な限りクラウドサービスをネイティブに利用することが出来る

AWSでは「ゲート」ではなく「ガードレール」で実現する。

> 従来のゲート型ではなく、予防的統制と発見的統制からなるガードレール型のガバナンス・セキュリティを提供する。
> クラウドサービスの利用にあたって制限となる内容は、ここに記述する予防的統制で設定される内容だけである。

## ガードレールの2種類(AWS)

| 種類 | 役割 | 使うAWSサービス |
|---|---|---|
| 予防的統制 | 不適切な操作を事前に止める | Organizations、SCP、Control Tower(予防コントロール) |
| 発見的統制 | 不正な状態を監視して通知・修正する | Security Hub、GuardDuty、Control Tower(発見コントロール)、Config Rules、環境の自動棚卸し |

## 予防的統制で止められる主なこと(AWS)

- 東京/大阪リージョン以外の使用
- IAMユーザーの永続的なアクセスキー作成(MFAを強制し、権限はIAMロールで管理)
- Adminユーザー以外によるIAM権限の付与
- セキュリティ/監査ログ関連サービスの削除
- AWS Marketplace、Outposts など一部サービス
- 一度の誤操作で高額請求になる購入(リザーブドインスタンス、Savings Plans など)

それ以外は、AWSのサービスをそのまま使える。

## 入口はひとつ: SSO → スイッチロール

1. GCASアカウントでシングルサインオン(IAM Identity Center経由)
2. 管理者以外は `SwitchOnlyRole`(スイッチロール専用)でAWSアカウントに入る
3. 利用システム側で作ったIAMロール(最小権限)へスイッチロール

## 5文で言ってみる

### 1 (ゲートでなくガードレール)
- **日本語訳**: ガバナンスは、ゲートではなくガードレールで行う。
- **English**: Governance uses guardrails, not gates.
- **カタカナ**: ガヴァナンスユーズィズ / ガードレイルズ / ナッゲイツ

### 2 (制限は予防的統制だけ)
- **日本語訳**: AWSを使うときの制限は、予防的統制だけ。
- **English**: The only limits on using AWS are the preventive controls.
- **カタカナ**: ジオウンリリミッツオンユーズィングエイダブリューエス / アーザプリヴェンティヴコントロウルズ

### 3 (リージョン)
- **日本語訳**: 東京か大阪リージョンを使う。ほかは禁止。
- **English**: Use the Tokyo or Osaka region; others are blocked.
- **カタカナ**: ユーズザトウキョウオアオーサカリージョン / アザーズアーブロックト

### 4 (アクセスキー)
- **日本語訳**: アクセスキーは作らず、MFAつきのIAMロールを使う。
- **English**: Don't create access keys; use IAM roles with MFA.
- **カタカナ**: ドウントクリエイトアクセスキーズ / ユーズアイエイエムロウルズ / ウィズエムエフエイ

### 5 (発見的統制)
- **日本語訳**: Security HubとGuardDutyが見張って、通知してくれる。
- **English**: Security Hub and GuardDuty watch your account and notify you.
- **カタカナ**: スィキュリティハバンガードデューティ / ウォチュアアカウント / アンノウティファイユー

> 補足(例外): アクセスキーが必要な外部SaaS連携などは、早い段階でキーを使わない方式を検討する。Marketplaceもマネージドサービスで代替できない場合のみデジタル庁に相談。

## AWSサービス名の読み

| English | カタカナ | 役割 |
|---|---|---|
| Control Tower | コントロールタワー | アカウント管理とコントロール |
| Organizations | オーガナイゼイションズ | 複数アカウントの組織管理 |
| SCP (Service Control Policy) | エスシーピー | 操作を制限するポリシー |
| IAM Identity Center | アイエイエムアイデンティティセンター | SSOの仕組み |
| Security Hub | スィキュリティハブ | セキュリティ検知の集約 |
| GuardDuty | ガードデューティ | 脅威検知 |
| Config | コンフィグ | 構成の記録と評価 |

## 語彙

| English | カタカナ | 日本語 |
|---|---|---|
| guardrail | ガードレイル | ガードレール |
| gate | ゲイト | ゲート |
| preventive control | プリヴェンティヴコントロウル | 予防的統制 |
| detective control | ディテクティヴコントロウル | 発見的統制 |
| least privilege | リーストプリヴィリッジ | 最小権限 |
| switch role | スウィッチロウル | スイッチロール |

[← ネイティブ利用へ戻る](../README.md)
