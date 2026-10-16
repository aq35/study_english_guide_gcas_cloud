# 3. 単純移行で終わらせない — 段階2: 原文を読み解く

出典: [GCASガイド ガバメントクラウド概要解説「6.1 モダンアプリケーション化」「4.2 利用環境を検討する場合のポイント①(モダン化)」](https://guide.gcas.cloud.go.jp/general)
英訳は筆者の訳(公式の英訳ではない)。カタカナの `/` は息継ぎ。ルールは [linking-rules.md](../../../linking-rules.md)。
「ガイド:」はGCASガイドに書かれていること、「推論:」は筆者の推論。

## 原文を1文ずつ読む

| # | 原文 | English(筆者訳) | ポイント |
|---|---|---|---|
| 1 | ガバメントクラウド利用組織は旧来のアーキテクチャを単純移行するに留まらず、マネージドサービスやコンテナ、サーバレス、マイクロサービスなどを活用してモダンアプリケーション化を検討すること。 | Government Cloud user organizations should consider modernizing their applications by using managed services, containers, serverless and microservices, rather than just moving the legacy architecture as it is. | 学習ノートの核心。`rather than ...`(〜ではなく)。活用する技術は4つ |
| 2 | 移行パターンについて、…このうちRebuildをモダンアプリケーションと考え、Replatformは2段階移行における第一段階としての一時的なものと考える。 | Of the migration patterns, Rebuild is regarded as the modern application, and Replatform is regarded as temporary, as the first step of a two-step migration. | `regard A as B`(AをBと考える)。R2 = Rebuild、R1 = Replatform |
| 3 | ガバメントクラウドへの移行時にはR1(Replatform)、R2(Rebuild)ともに、従来型のPCに専用のクライアントソフトウェアをインストールするクライアント・サーバー方式はWebシステム(マイクロサービス型やフロントエンド・バックエンド分離型等)に変更することを原則とする。 | When migrating to the Government Cloud, in both R1 (Replatform) and R2 (Rebuild), the principle is to change the traditional client-server method, where dedicated client software is installed on PCs, to a web system (microservice type, front-end/back-end separated type, etc.). | `as a rule`(原則として)。R1でもR2でも同じ。クライアント・サーバー方式 → Webシステム |
| 4 | Replatformで移行する情報システムであっても、最終的にはRebuild構成を目指す必要がある。(4.2) | Even a system migrated by Replatform must ultimately aim for the Rebuild configuration. | `even ...`(〜であっても)、`ultimately`(最終的には) |

## 3つの移行パターン(4.2)

| パターン | 名称 | 内容(ガイド) |
|---|---|---|
| R3 | Repurchase | SaaSなどを活用し、個別にアプリケーション開発せずにシステムを実現する |
| R2 | Rebuild | アプリケーションのコードを新規で書き起こし、旧データの必要な部分を取り込む。新規システムはこの状態が原則 |
| R1 | Replatform | 一括でのモダン化が難しい場合に、一段階目は部分的(運用監視やデータベース等)にマネージドサービスへ置き換え、二段階目でR2構成にすることも許容される。二段階目の時期は、プロジェクト計画書等に必ず明示する |

## 読み解きのポイント

- ガイド: 「単純移行」で終わらせないこと。マネージドサービス、コンテナ、サーバレス、マイクロサービスなどを活用して、モダンアプリケーション化を検討する(文1)。
- ガイド: モダンアプリケーションと考えるのは Rebuild。Replatform は、2段階移行の「一時的な」第一段階(文2)。
- ガイド: R1・R2のどちらでも、クライアント・サーバー方式はWebシステムに変える(文3)。
- ガイド: Replatform で始めても、最終的に目指すのは Rebuild(文4)。第二段階の時期は、計画書に必ず書く。
- ガイド: シンクライアント、VDI、DaaS は原則使わない。ただし例外がある(既存の標準端末がそれである場合など)。
- マイクロサービスの中身(利点、5つの基準、AWSでの実現)は、[補章](../microservice/README.md)で読む。
- 推論: 文1の「検討すること」は「検討する」ことを求めており、すべてをモダン化しなければならないとまでは言っていない。一方、文4は最終的に Rebuild を目指すことを求める。一時的な Replatform と最終形の Rebuild を、二段構えで読むとつながる。

## 5文で言ってみる

### 1 (文1)
- **日本語訳**: 古いアーキテクチャを、単純に移すだけでは足りない。
- **English**: Simply moving the old architecture is not enough.
- **カタカナ**: シンプリムーヴィングジオウルドアーキテクチャ / イズナットイナフ

### 2 (文1の技術)
- **日本語訳**: マネージドサービス、コンテナ、サーバレスを使う。
- **English**: Use managed services, containers and serverless.
- **カタカナ**: ユーズマニジドサーヴィスィズ / コンテイナーズアンサーバーレス

### 3 (文2)
- **日本語訳**: Rebuildが、モダンアプリケーション。
- **English**: Rebuild is the modern application.
- **カタカナ**: リビルディズザモダンアプリケイション

### 4 (文2・文4)
- **日本語訳**: Replatformは、一時的な第一歩。
- **English**: Replatform is a temporary first step.
- **カタカナ**: リプラットフォームイズアテンポレリ / ファースステップ

### 5 (文3)
- **日本語訳**: クライアント・サーバー方式を、Webシステムに変える。
- **English**: Replace client-server with web systems.
- **カタカナ**: リプレイスクライアントサーバー / ウィズウェブシステムズ

## 語彙

| English | カタカナ | 日本語 | 詳しい説明 |
|---|---|---|---|
| modernization | モダナイゼイション | モダン化 | 旧来の技術から離れて、クラウドの特徴を生かした構成にすること |
| replatform | リプラットフォーム | R1 | アプリの変更を最小限にして、マネージドサービスを使う形に移す |
| rebuild | リビルド | R2 | アプリを新しく書き起こして、クラウドをフルに活用する |
| container | コンテイナー | コンテナ | アプリを、動作に必要なものごとまとめて動かす仕組み |
| serverless | サーバーレス | サーバレス | サーバを自分で管理せず、コードだけを動かす仕組み |
| microservice | マイクロサーヴィス | マイクロサービス | アプリを小さな部品に分けて、独立して作る設計 |

[← 単純移行で終わらせないへ戻る](../README.md)
