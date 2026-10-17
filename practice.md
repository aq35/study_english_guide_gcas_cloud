# 段階5: 自分の言葉で言う練習

8つの考え方を、声に出して、自分の言葉で言えるようにする。カタカナの `/` は息継ぎ。ルールは [linking-rules.md](linking-rules.md)。

## 1. シャドーイング(声に出して続けて言う)

**やり方**: 1つの文につき、次の4ステップ。

1. 日本語訳を読んで、意味をつかむ
2. Englishを読みながら、カタカナを見て、1文ずつ声に出す(ゆっくり)
3. カタカナを隠して、Englishだけ見て言う
4. 速さを上げて、`/` の息継ぎだけ意識して、止まらずに言う

**順番**: 8つを、1から8まで続けて言う。言えない文は、そこだけ繰り返す。

| # | 考え方 | 日本語訳 | English | カタカナ |
|---|---|---|---|---|
| 1 | [目指す姿](principles/01-target-state/README.md) | ガバメントクラウドは、クラウドを賢く使ってコスト最適化を目指す。 | The Government Cloud aims to cut costs by using the cloud smartly. | ザガヴァメンクラウド / エイムズトゥ / カッコスツ / バイユーズィンザクラウド / スマートリー |
| 2 | [ネイティブ利用](principles/02-native-use/README.md) | 独自の共通機能は作らず、クラウドサービスをそのまま(ネイティブに)使う。 | We use cloud services natively and avoid building our own shared features. | ウィユーズ / クラウドサーヴィスィズ / ネイティヴリ / アンダヴォイド / ビルディンガワオウン / シェアドフィーチャーズ |
| 3 | [単純移行で終わらせない](principles/03-modernize/README.md) | 古いシステムをそのまま移すだけでなく、モダン化しよう。 | Don't just move old systems as they are; modernize them. | ドウンッジャスト / ムーヴォウルドシステムズ / アズゼイアー / モダナイズゼム |
| 4 | [責任共有モデル](principles/04-shared-responsibility/README.md) | マネージドサービスを使えば、自分たちの責任範囲とリスクは小さくなる。 | Managed services shrink your responsibility and your risk. | マニジドサーヴィスィズ / シュリンクヨア / リスポンスィビリティ / アンジョアリスク |
| 5 | [SaaSは無条件の正解ではない](principles/05-saas-not-always/README.md) | SaaSが常に正解とは限らない。ライフサイクルコストで比べよう。 | SaaS is not always the answer; compare the lifecycle cost. | サースィズ / ナロールウェイズ / ジアンサー / コンペアザ / ライフサイクルコスト |
| 6 | [マルチクラウドは原則禁止](principles/06-no-multicloud/README.md) | 1つのシステムで複数のクラウドを使うのは、原則すすめない。 | Using multiple clouds in one system is generally not recommended. | ユーズィンマルティプル / クラウズィンワンシステム / イズジェネラリ / ナッレコメンディッド |
| 7 | [データの可搬性](principles/07-data-portability/README.md) | アプリだけでなく、データも持ち運べるようにしよう。 | Make your data portable, not just your applications. | メイキョア / デイタポータブル / ナッジャスチュア / アプリケイションズ |
| 8 | [継続的な見直しとコスト管理](principles/08-continuous-review/README.md) | 見直しを続けよう。見える化し、分析し、最適化する。 | Keep reviewing: visualize, analyze, then optimize. | キープリヴューイング / ヴィジュアライズ / アナライズ / ゼナプティマイズ |

## 2. 言い換え(同じ考え方を、3通りで言う)

同じ考え方を、レベル1(短い文)、レベル2(`because` / `so` で理由をつけた文)、レベル3(自分のシステムに引きつけた文)の順に言う。

- レベル1: 段階1の文
- レベル2: 段階3の文
- レベル3: 下の型の `___` を、自分のシステムの言葉で埋める

| # | レベル1(短い) | レベル2(理由つき) | レベル3(自分の言葉の型) |
|---|---|---|---|
| 1 | The Government Cloud aims to cut costs by using the cloud smartly. | We use the cloud smartly because moving is not enough. | `In my system, we ___ the cloud smartly, so that ___.` |
| 2 | We use cloud services natively and avoid building our own shared features. | We use cloud services natively to get the full benefits. | `In my system, we use ___ natively, and we do not build our own ___.` |
| 3 | Don't just move old systems as they are; modernize them. | Modernizing lowers cost, speeds development and improves security. | `In my system, we moved from ___ to ___, instead of just moving it as it is.` |
| 4 | Managed services shrink your responsibility and your risk. | Managed services reduce risk, but you may still be held accountable. | `In my system, the CSP is responsible for ___, and we are responsible for ___.` |
| 5 | SaaS is not always the answer; compare the lifecycle cost. | SaaS saves development, but fees can grow. | `For ___, we compared SaaS and ___ by lifecycle cost.` |
| 6 | Using multiple clouds in one system is generally not recommended. | Multi-cloud costs more and makes operations complex. | `In my system, we use only ___, because ___.` |
| 7 | Make your data portable, not just your applications. | Changing CSPs takes years, so data must be portable. | `In my system, we can export ___ in ___ format.` |
| 8 | Keep reviewing: visualize, analyze, then optimize. | Fees change every month, so we keep reviewing. | `Every ___, we check ___ and optimize ___.` |

レベル3の `___` は、ここに書き込んでよい。自分の言葉で埋めた文は、声に出して、リンキングを意識して言う。

## 3. 確認(日本語だけ見て、英語で言う)

日本語だけを見て、英語で言ってみる。言えたら、答えを開いて確かめる。

| # | 日本語 | 答え |
|---|---|---|
| 1 | ガバメントクラウドは、クラウドを賢く使ってコスト最適化を目指す。 | <details><summary>答え</summary>The Government Cloud aims to cut costs by using the cloud smartly.<br>ザガヴァメンクラウド / エイムズトゥ / カッコスツ / バイユーズィンザクラウド / スマートリー</details> |
| 2 | 独自の共通機能は作らず、クラウドサービスをそのまま(ネイティブに)使う。 | <details><summary>答え</summary>We use cloud services natively and avoid building our own shared features.<br>ウィユーズ / クラウドサーヴィスィズ / ネイティヴリ / アンダヴォイド / ビルディンガワオウン / シェアドフィーチャーズ</details> |
| 3 | 古いシステムをそのまま移すだけでなく、モダン化しよう。 | <details><summary>答え</summary>Don't just move old systems as they are; modernize them.<br>ドウンッジャスト / ムーヴォウルドシステムズ / アズゼイアー / モダナイズゼム</details> |
| 4 | マネージドサービスを使えば、自分たちの責任範囲とリスクは小さくなる。 | <details><summary>答え</summary>Managed services shrink your responsibility and your risk.<br>マニジドサーヴィスィズ / シュリンクヨア / リスポンスィビリティ / アンジョアリスク</details> |
| 5 | SaaSが常に正解とは限らない。ライフサイクルコストで比べよう。 | <details><summary>答え</summary>SaaS is not always the answer; compare the lifecycle cost.<br>サースィズ / ナロールウェイズ / ジアンサー / コンペアザ / ライフサイクルコスト</details> |
| 6 | 1つのシステムで複数のクラウドを使うのは、原則すすめない。 | <details><summary>答え</summary>Using multiple clouds in one system is generally not recommended.<br>ユーズィンマルティプル / クラウズィンワンシステム / イズジェネラリ / ナッレコメンディッド</details> |
| 7 | アプリだけでなく、データも持ち運べるようにしよう。 | <details><summary>答え</summary>Make your data portable, not just your applications.<br>メイキョア / デイタポータブル / ナッジャスチュア / アプリケイションズ</details> |
| 8 | 見直しを続けよう。見える化し、分析し、最適化する。 | <details><summary>答え</summary>Keep reviewing: visualize, analyze, then optimize.<br>キープリヴューイング / ヴィジュアライズ / アナライズ / ゼナプティマイズ</details> |

[← 大括り(overview.md)へ戻る](overview.md)
