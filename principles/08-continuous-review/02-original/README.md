# 8. 継続的な見直しとコスト管理 — 段階2: 原文を読み解く

出典: [GCASガイド ガバメントクラウド概要解説「5.5 恒常的なアーキテクチャ見直し」](https://guide.gcas.cloud.go.jp/general) / [AWS技術ガイド「クラウド利用料の予実管理と最適化」の「コスト管理運用の基本方針」](https://guide.gcas.cloud.go.jp/aws)
英訳は筆者の訳(公式の英訳ではない)。カタカナの `/` は息継ぎ。ルールは [linking-rules.md](../../../linking-rules.md)。
「ガイド:」はGCASガイドに書かれていること、「推論:」は筆者の推論。

## 原文を1文ずつ読む

### 5.5 恒常的なアーキテクチャ見直し

| # | 原文 | English(筆者訳) | ポイント |
|---|---|---|---|
| 1 | ガバメントクラウド利用組織は、クラウドサービスの利用料が毎月変動するため、恒常的に適切なサイジングとなっているかを見直し、必要であれば適切なサイズや数に変更を行う。 | Because cloud service fees fluctuate every month, Government Cloud user organizations continuously review whether the sizing is appropriate and, if necessary, change the size or number accordingly. | 学習ノートの核心。理由は「毎月変動する」。`sizing`(サイジング) |
| 2 | また、常に稼働する必要のないものは必要なときだけ起動する等の改善も行う。 | They also make improvements, such as starting anything that does not need to run all the time only when it is needed. | `such as ...`(〜など)、`only when ...`(〜のときだけ) |
| 3 | 年度毎にアーキテクチャの見直し及びコスト試算を行い、モダンアーキテクチャ化の推進やコスト削減を図る必要がある。 | Each fiscal year, they need to review the architecture and estimate costs, in order to promote modern architecture and reduce costs. | `each fiscal year`(年度ごとに) |
| 4 | 見直したコスト試算はデジタル庁にて確認、承認を行う。 | The revised cost estimate is checked and approved by the Digital Agency. | 受け身(`is checked and approved`)。確認・承認するのはデジタル庁 |

### AWS技術ガイド「コスト管理運用の基本方針」

| # | 原文 | English(筆者訳) | ポイント |
|---|---|---|---|
| 5 | 「定常的なコスト管理運用フロー」に従い、月次でコストを最適化するためのサイクルを実施する。 | Follow the "regular cost management flow" and carry out the cycle for optimizing costs every month. | `follow ...`(〜に従う)。月次 |
| 6 | …コストの継続的な改善を目的としているため、設定した予算よりコスト実績が下回っているかに関わらず、月次での実施を推奨する。 | Because the aim is continuous improvement of costs, monthly implementation is recommended regardless of whether actual costs are below the budget. | `regardless of whether ...`(〜かどうかに関わらず) |
| 7 | 管理工数削減・リアルタイム性の観点より運用報告などの形式で資料を別途作成することは極力せず、分析含めダッシュボード化することを推奨する。 | From the viewpoint of reducing management effort and keeping it real-time, avoid creating separate documents such as operation reports as far as possible, and make dashboards, including the analysis. | `as far as possible`(極力)。理由は「管理工数削減」と「リアルタイム性」 |

## 見直しの周期(ガイド)

| 周期 | 内容 |
|---|---|
| 月次 | 「可視化」「分析」「コストの最適化」の順に実施 |
| 半期に一度 | 利用システムで使う全サービスに対して、コスト最適化の基準の確認と対策を実施(推奨) |
| 年度ごと | アーキテクチャの見直しとコスト試算。デジタル庁が確認・承認 |
| 随時 | 予算アラートで超過を検知したとき、利用システム側が判断して実施 |

## 読み解きのポイント

- ガイド: 見直しの理由は、クラウドの利用料が「毎月変動する」こと(文1)。
- ガイド: 見直す観点は2つ。サイズや数が適切か(文1)、常に稼働する必要がないものを必要なときだけ起動できないか(文2)。
- ガイド: 周期は3段階。月次のコスト最適化、半期の全サービス確認、年度のアーキテクチャ見直しとコスト試算。
- ガイド: 月次の実施は、予算を下回っていても行う(文6)。目的が、継続的な改善だから。
- ガイド: 報告用の資料は別に作らず、ダッシュボードにする(文7)。
- ガイド: 年度のコスト試算は、デジタル庁が確認・承認する(文4)。月次の最適化は、利用システム側が行う。
- 推論: 「恒常的」(文1)は、月次・半期・年度と周期を重ねて続ける、という意味に読める。ガイドは「恒常的」の周期を1つに決めてはいない。

## 5文で言ってみる

### 1 (文1)
- **日本語訳**: 料金は毎月変わるので、サイズを定期的に確認する。
- **English**: Fees change every month, so check the size regularly.
- **カタカナ**: フィーズチェインジェヴリマンス / ソウチェックザサイズレギュラリ

### 2 (文3)
- **日本語訳**: アーキテクチャとコスト試算を、毎年見直す。
- **English**: Review the architecture and the cost estimate every year.
- **カタカナ**: リヴュージアーキテクチャアンザコストエスティメイト / エヴリイヤー

### 3 (文4)
- **日本語訳**: 見直した試算は、デジタル庁が承認する。
- **English**: The Digital Agency approves the revised estimate.
- **カタカナ**: ザデジタルエイジェンスィアプルーヴズ / ザリヴァイズドエスティメイト

### 4 (文6)
- **日本語訳**: 予算内でも、毎月コストを最適化する。
- **English**: Optimize costs monthly, even under budget.
- **カタカナ**: アプティマイズコスツマンスリ / イーヴンアンダーバジェット

### 5 (文7)
- **日本語訳**: 別の報告書ではなく、ダッシュボードを使う。
- **English**: Use a dashboard instead of a separate report.
- **カタカナ**: ユーザダッシュボード / インステッドオヴァセパレットリポート

## 語彙

| English | カタカナ | 日本語 | 詳しい説明 |
|---|---|---|---|
| sizing | サイジング | サイジング | 使う量に合わせて、サーバなどの大きさや台数を決めること |
| fluctuate | フラクチュエイト | 変動する | 一定ではなく、上がったり下がったりすること |
| fiscal year | フィスカルイヤー | 年度 | 予算の単位になる、会計上の1年間 |
| cost estimate | コストエスティメイト | コスト試算 | これからかかる費用を、見積もって計算すること |
| continuous improvement | コンティニュアスインプルーヴメント | 継続的な改善 | 一度で終わらず、改善を続けること |
| dashboard | ダッシュボード | ダッシュボード | 数値やグラフを1つの画面にまとめて、いつでも見られるようにしたもの |

[← 継続的な見直しとコスト管理へ戻る](../README.md)
