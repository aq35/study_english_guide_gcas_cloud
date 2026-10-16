# 4. 責任共有モデル — 段階2: 原文を読み解く

出典: [GCASガイド ガバメントクラウド概要解説「ガバメントクラウド利用システムにおけるセキュリティ対策(共通)」の「責任共有モデル」](https://guide.gcas.cloud.go.jp/general)
英訳は筆者の訳(公式の英訳ではない)。カタカナの `/` は息継ぎ。ルールは [linking-rules.md](../../../linking-rules.md)。
「ガイド:」はGCASガイドに書かれていること、「推論:」は筆者の推論。

## 原文を1文ずつ読む

| # | 原文 | English(筆者訳) | ポイント |
|---|---|---|---|
| 1 | 責任共有モデルとは、クラウドサービスを利用する上で、CSPと利用者がセキュリティとコンプライアンスの責任を負う範囲を定めたものである。 | The shared responsibility model defines the scope of security and compliance responsibility that the CSP and the user each bear when using cloud services. | 定義の文。`define the scope of ...`(〜の範囲を定める) |
| 2 | 一般的には物理サーバ、物理ストレージ、ネットワーク、マネージドサービスなどがCSPの責任範囲となり、OS、ミドルウェア、CSPが提供するサービスの設定、アンマネージドサービス上のデータなどが利用者の責任範囲となる。 | Generally, physical servers, physical storage, the network and managed services fall within the CSP's scope, while the OS, middleware, the settings of CSP-provided services and data on unmanaged services fall within the user's scope. | `fall within ...`(〜の範囲に入る)。「サービスの設定」は利用者側 |
| 3 | ただし、公共分野のシステムにおいては実際の責任の有無に関わらず、説明責任を問われる場合があることを想定しておかれたい。 | However, for public-sector systems, please assume that you may be held accountable regardless of whether you are actually responsible. | `regardless of ...`(〜に関わらず)、`accountable`(説明責任がある) |
| 4 | ガバメントクラウドにおける責任範囲は、以下の三つの範囲に分割される。 | In the Government Cloud, responsibility is divided into the following three scopes. | 利用組織 / ガバメントクラウド / CSP の3つ |
| 5 | このうち、利用組織の責任範囲はマネージドサービスを利用することで狭めることができ、セキュリティリスクを軽減することができる。 | Of these, the user organization's scope can be narrowed by using managed services, which reduces security risk. | 学習ノートの核心。`narrow`(狭める)、`reduce`(軽減する) |
| 6 | ただし、マネージドサービスであっても、サービスの設定内容は利用者側の責任となることには留意する。 | Note, however, that even with managed services, the service settings remain the user's responsibility. | `even with ...`(〜であっても)、`remain`(〜のままである) |

## 3つの範囲(ガバメントクラウドでの責任共有モデル)

| 範囲 | 担当する内容(ガイド) |
|---|---|
| 利用組織 | クラウドサービスを含めたインフラ構成、クラウドサービスの設定、OS、ミドルウェア、アプリケーション、データの管理など |
| ガバメントクラウド | ガードレール設定、テンプレート/IaCファイル、環境払い出しなど(図では、アプリ推奨構成ガイド、コンサルテーション、トレーニング、平日9時から17時対応の窓口も含む) |
| CSP | クラウド基盤(ハードウェア、ソフトウェア、ネットワーク)、マネージドサービスなど(図では、24時間365日対応のCSPサポートも含む) |

## 読み解きのポイント

- ガイド: 責任共有モデルは、CSPと利用者の「責任の範囲」を決めたもの(文1)。
- ガイド: 一般には、基盤はCSP、OS・ミドルウェア・サービスの設定・データは利用者(文2)。
- ガイド: ガバメントクラウドでは、範囲が「三つ」に分かれる(文4)。ガバメントクラウドが、利用組織とCSPの間に入る。
- ガイド: 利用組織の責任範囲は、マネージドサービスを使うと狭められる(文5)。ただし、サービスの設定は利用者の責任のまま(文6)。
- ガイド: 公共分野では、責任がなくても説明責任を問われる場合がある(文3)。
- 推論: 文5と文6は、組み合わせて読む。「狭められる」のは、OSやミドルウェアなどの運用の責任で、「設定」の責任は残る。文3の説明責任は、さらに別の話で、責任範囲の外側にも及ぶ。ガイドはこの3つを並べて書いていて、関係の整理は筆者による。

## 5文で言ってみる

### 1 (文1)
- **日本語訳**: このモデルは、誰が何に責任を持つかを決める。
- **English**: The model defines who is responsible for what.
- **カタカナ**: ザモデルディファインズ / フーイズリスポンスィブル / フォーワット

### 2 (文2)
- **日本語訳**: 基盤はCSPのもの。設定は、利用者のもの。
- **English**: The CSP owns the infrastructure; you own the settings.
- **カタカナ**: ザシーエスピーオウンズ / ジインフラストラクチャ / ユーオウンザセティングズ

### 3 (文4)
- **日本語訳**: 層は3つ。利用組織、ガバメントクラウド、CSP。
- **English**: There are three layers: you, the Government Cloud and the CSP.
- **カタカナ**: ゼアアースリーレイヤーズ / ユーザガヴァメントクラウドアンザシーエスピー

### 4 (文5)
- **日本語訳**: マネージドサービスで、責任範囲を狭める。
- **English**: Narrow your scope with managed services.
- **カタカナ**: ナロウヨアスコウプ / ウィズマニジドサーヴィスィズ

### 5 (文3)
- **日本語訳**: 実際の責任の有無に関わらず、説明責任を問われることがある。
- **English**: You may be held accountable regardless of actual responsibility.
- **カタカナ**: ユーメイビーヘルドアカウンタブル / リガードレスオヴァクチュアルリスポンスィビリティ

## 語彙

| English | カタカナ | 日本語 | 詳しい説明 |
|---|---|---|---|
| shared responsibility model | シェアドリスポンスィビリティマダル | 責任共有モデル | CSPと利用者が、責任を分け合う範囲を示した考え方 |
| scope | スコウプ | 範囲 | 責任や作業が及ぶ、境目で区切られた領域 |
| compliance | コンプライアンス | コンプライアンス | 法令やルールを守ること |
| accountable | アカウンタブル | 説明責任がある | 起きたことについて、説明して応える立場にあること |
| unmanaged service | アンマニジドサーヴィス | アンマネージドサービス | 利用者がOSなどを管理する必要がある、仮想サーバなどのサービス |
| guardrail | ガードレイル | ガードレール | 危険な操作だけを止める、ガバメントクラウド側の仕組み |

[← 責任共有モデルへ戻る](../README.md)
