# 1. 目指す姿 — 段階2: 原文を読み解く

出典: [GCASガイド ガバメントクラウド概要解説「2.1 背景と目的」「2.2 目指す姿」](https://guide.gcas.cloud.go.jp/general)
英訳は筆者の訳(公式の英訳ではない)。カタカナの `/` は息継ぎ。ルールは [linking-rules.md](../../../linking-rules.md)。
「ガイド:」はGCASガイドに書かれていること、「推論:」は筆者の推論。

## 原文を1文ずつ読む

### 2.1 背景と目的(「政府情報システムにおけるクラウドサービスの適切な利用に係る基本方針」より抜粋)

| # | 原文 | English(筆者訳) | ポイント |
|---|---|---|---|
| 1 | 旧方針は、クラウド第一原則(クラウド・バイ・デフォルト原則)に基づき政府情報システムのオンプレミスからクラウドへの移行を促すものであった。 | The former policy encouraged moving government information systems from on-premises to the cloud, based on the cloud-first (cloud-by-default) principle. | 「旧方針」の説明。`based on ...`(〜に基づき) |
| 2 | 一方でクラウドへの移行そのものが目的化されてしまい、必ずしもクラウドサービスの利用メリットを十分に享受できていないといった例も散見された。 | On the other hand, there were cases where moving to the cloud itself became the goal, and the benefits of cloud services were not always fully enjoyed. | 反省点。`became the goal`(目的化)、`not always`(必ずしも〜ない) |
| 3 | ガバメントクラウドでは、政府情報システムが単にクラウドに移行するだけではなく、クラウドの利用メリットを十分に得られるようにするための、スマートなクラウド利用を促すことを目的に情報システムの利用環境として用意された。 | The Government Cloud was prepared as a usage environment, to encourage smart cloud use so that systems not only move to the cloud but also fully gain its benefits. | `not only A but also B`(AだけでなくB)。「スマート」の意味はここで説明される |

### 2.2 目指す姿

| # | 原文 | English(筆者訳) | ポイント |
|---|---|---|---|
| 4 | ガバメントクラウドは公共情報システムのスマートなクラウド利用を促すことで、システムや運用のモダン化を通じたクラウド最適化によるコスト最適化…を目指す。 | By encouraging smart cloud use of public information systems, the Government Cloud aims for cost optimization through cloud optimization, via the modernization of systems and operations. | 「コスト最適化」の中身は括弧で5つ列挙される(下の表)。`aim for ...`(〜を目指す) |

## 「コスト最適化」の中身(原文の括弧)

> インフラ構築管理コスト削減、インフラ構築管理工数削減、セキュリティ品質向上、開発スピード向上、継続的改善の実現

| English | 日本語 |
|---|---|
| reduce infrastructure cost | インフラ構築管理コスト削減 |
| reduce infrastructure effort | インフラ構築管理工数削減 |
| improve security quality | セキュリティ品質向上 |
| speed up development | 開発スピード向上 |
| continuous improvement | 継続的改善 |

## 「スマートなクラウド利用」と効果の対応(ガイドの図2-1)

| スマートなクラウド利用 | コスト削減 | 工数削減 | セキュリティ品質向上 | 開発スピード向上 | 継続的改善 |
|---|:-:|:-:|:-:|:-:|:-:|
| マネージドサービス | ○ | ○ | ○ | ○ | |
| IaC | ○ | ○ | ○ | | |
| モダンアプリケーション | | | ○ | ○ | |
| 可視化 | ○ | | ○ | | ○ |

## 読み解きのポイント

- ガイド: 背景は、旧方針の反省。クラウドへの移行が目的になってしまい、利用メリットを十分に得られていない例があった。
- ガイド: ガバメントクラウドの目的は、「単に移行する」ではなく、「利用メリットを十分に得る」ための「スマートなクラウド利用」を促すこと。
- ガイド: 「スマートなクラウド利用」の具体的な要素は、図2-1の4つ(マネージドサービス、IaC、モダンアプリケーション、可視化)。
- ガイド: 「コスト最適化」と書かれているが、括弧の中には、品質(セキュリティ)、速度(開発スピード)、継続的改善も含まれている。
- 学習ノートの段階1の英文は `cut costs`(コストを減らす)。原文の「コスト最適化」は、もっと広い意味なので、段階2で補った。
- 推論: 「スマート」は、クラウドを使うこと自体ではなく、クラウドの特徴(マネージド、自動化、可視化など)を生かした使い方を指すと読める。ガイドはこの括り方を明示していない。

## 5文で言ってみる

### 1 (文2)
- **日本語訳**: クラウドへの移行は、目的ではない。
- **English**: Moving to the cloud is not the goal.
- **カタカナ**: ムーヴィングトゥザクラウドイズナットザゴウル

### 2 (文3)
- **日本語訳**: 目的は、クラウドのメリットを十分に得ること。
- **English**: The goal is to enjoy the benefits of the cloud.
- **カタカナ**: ザゴウルイズトゥインジョイザベネフィッツ / オヴザクラウド

### 3 (文3)
- **日本語訳**: ガバメントクラウドは、スマートなクラウド利用を促す。
- **English**: The Government Cloud encourages smart cloud use.
- **カタカナ**: ザガヴァメンクラウド / インカレッジズスマートクラウドユース

### 4 (文4)
- **日本語訳**: システムと運用をモダン化して、コストを最適化する。
- **English**: Modernizing systems and operations optimizes costs.
- **カタカナ**: モダナイジングシステムザンアペレイションズ / アプティマイズィズコスツ

### 5 (括弧の中身)
- **日本語訳**: コストは下がり、セキュリティと速度は上がる。
- **English**: Cost goes down; security and speed go up.
- **カタカナ**: コストゴウズダウン / スィキュアリティアンスピードゴウアップ

## 語彙

| English | カタカナ | 日本語 | 詳しい説明 |
|---|---|---|---|
| cloud-first (cloud-by-default) | クラウドファースト | クラウド第一(クラウド・バイ・デフォルト) | 新しいシステムは、まずクラウドの利用を考える、という原則 |
| goal | ゴウル | 目的 | その行動で達成したいこと |
| benefit | ベネフィット | メリット、恩恵 | 利用して得られる良い点 |
| optimize | アプティマイズ | 最適化する | 性能を保ったまま、無駄を減らすこと |
| continuous improvement | コンティニュアスインプルーヴメント | 継続的改善 | 一度で終わらず、改善を続けること |
| IaC (Infrastructure as Code) | アイエイシー | IaC | インフラの構築や設定を、コードで書いて自動化すること |

[← 目指す姿へ戻る](../README.md)
