# リンキングの反復ドリル(つまずきやすい音から)

このリポジトリにある英文 **147 組**(overview 8 / principles 85 / topics 54)から、**音のつながりだけ**を抜き出して並べ直したもの。英語は新しく作っていない。各行に出どころを書く。

カタカナの `/` は息継ぎ。決まりは [linking-rules.md](linking-rules.md)。

- 「ガイド:」: GCASガイドの原文、またはこのリポジトリに書かれていること
- 「推論:」: ここに書かれていない、筆者(Claude Code)の推論

## 使い方(1 日 5 分、1 ドリル)

同じ音を**続けて何度も**出すのが目的。文は後回しでよい。

1. **チャンクだけ**: カタカナを見ながら 5 回 → 見ないで 5 回。切らずに一息で。
2. **チャンク + 前後**: その息継ぎの前後だけをつなげて 3 回。
3. **文を通す**: 日本語だけ見て、英語で言う。止まった所が、まだつながっていない所。

つまずきやすい順に 1 → 6。1 日 1 つでよい。

---

## ドリル 1: 止める t(子音の前)

**決まり**: [linking-rules.md](linking-rules.md) の 3

推論: 日本語は t をはっきり出す。「ノット」と言うと、そこで息が切れて、**後ろの語が聞き取れなくなる**。t は**止めるだけ**にして、息を切らずに次の語へ渡す。

### チャンクだけ

| カタカナ | 英語 | 出どころ |
|---|---|---|
| カッコスツ | cut costs | [overview.md](overview.md) 1 |
| ドウンッジャスト | Don't just | [overview.md](overview.md) 3 |
| ナッジャスチュア | not just your | [overview.md](overview.md) 7 |
| ナッゲイツ | not gates | [principles/02-native-use/04-aws/](principles/02-native-use/04-aws/README.md) |
| ナットバイハンド | not by hand | [topics/app-dos-and-donts.md](topics/app-dos-and-donts.md) |
| ナットフーワズロング | not who was wrong | [topics/operations-modernization.md](topics/operations-modernization.md) |
| ナットジャストザスィーピーユー | not just the CPU | [topics/managed-service-practice.md](topics/managed-service-practice.md) |

### 文を通す

| 日本語 | English | カタカナ |
|---|---|---|
| ガバメントクラウドは、クラウドを賢く使ってコスト最適化を目指す。 | The Government Cloud aims to cut costs by using the cloud smartly. | ザガヴァメンクラウド / エイムズトゥ / カッコスツ / バイユーズィンザクラウド / スマートリー |
| 「誰が悪いか」ではなく、「何が悪かったか」を問う。 | Ask what went wrong, not who was wrong. | アスクワットウェントロング / ナットフーワズロング |
| インフラは、手作業ではなく、コードで作る。 | Build infrastructure with code, not by hand. | ビルドインフラストラクチャウィズコウド / ナットバイハンド |
| CPUだけでなく、サービスの品質を監視する。 | Monitor service quality, not just the CPU. | マニタサーヴィスクウォリティ / ナットジャストザスィーピーユー |

---

## ドリル 2: ラ行になる t(母音の前)

**決まり**: [linking-rules.md](linking-rules.md) の 10(2026-10-17 に足した)

推論: **同じ `not` でも、次が母音ならラ行**になる。`not by hand` は「ナット」、`not always` は「ナロー…」。ここが一番つまずく。聞き取れないのも、たいていこの形。

### チャンクだけ

| カタカナ | 英語 | 出どころ |
|---|---|---|
| ナロールウェイズ | not always | [overview.md](overview.md) 5 |
| ナリナフ | not enough | [principles/01-target-state/03-reasons/](principles/01-target-state/03-reasons/README.md) |
| ナロンイーシーツー | not on EC2 | [topics/aws-db-and-donts.md](topics/aws-db-and-donts.md) |
| ナラバックアップ | not a backup | [topics/managed-service-practice.md](topics/managed-service-practice.md) |
| ゲラジーキャスアカウント | get a GCAS account | [topics/gcas-user-guide.md](topics/gcas-user-guide.md) |
| ソウイリズ | so it is | [principles/05-saas-not-always/02-original/](principles/05-saas-not-always/02-original/README.md) |
| ワリズトゥルーリーアージェント | what is truly urgent | [topics/system-migration-aws.md](topics/system-migration-aws.md) |
| ウィザウラスーミング | without assuming | [topics/system-migration-aws.md](topics/system-migration-aws.md) |

### 文を通す

| 日本語 | English | カタカナ |
|---|---|---|
| SaaSが常に正解とは限らない。ライフサイクルコストで比べよう。 | SaaS is not always the answer; compare the lifecycle cost. | サースィズ / ナロールウェイズ / ジアンサー / コンペアザ / ライフサイクルコスト |
| 私たちは、移行するだけでは足りないから、クラウドを賢く使う。 | We use the cloud smartly because moving is not enough. | ウィユーズザクラウドスマートリー / ビコーズムーヴィングイズナリナフ |
| データベースは、EC2ではなくマネージドサービスで動かす。 | Run the database as a managed service, not on EC2. | ランザデイタベイスアザマニジドサーヴィス / ナロンイーシーツー |
| 耐久性のあるストレージは、バックアップではない。 | Durable storage is not a backup. | デュアラブルストレージ / イズナラバックアップ |

---

## ドリル 3: `-ing` + 母音(g が次へ渡る)

**決まり**: [linking-rules.md](linking-rules.md) の 9

推論: `-ing` のあとに母音が来ると、g が次の語の頭に移る。日本語の「ビルディング」「ユージング」で止めると、ここが切れる。**グ を次の語にくっつける**と直る。

### チャンクだけ

| カタカナ | 英語 | 出どころ |
|---|---|---|
| ビルディンガワオウン | building our own | [overview.md](overview.md) 2 |
| ビルディンガンオペレイティング | Building and operating | [principles/02-native-use/02-original/](principles/02-native-use/02-original/README.md) |
| ユーズィンゲイダブリューエス | using AWS | [principles/02-native-use/04-aws/](principles/02-native-use/04-aws/README.md) |
| メイキンゴウンリ | making only | [principles/07-data-portability/02-original/](principles/07-data-portability/02-original/README.md) |
| デュアリンガペレイション | during operation | [principles/07-data-portability/02-original/](principles/07-data-portability/02-original/README.md) |

※ 出どころの文は、2026-10-17 にこの形へそろえた。下の「そろえたこと」を見る。

### 文を通す

| 日本語 | English | カタカナ |
|---|---|---|
| 独自の共通機能は作らず、クラウドサービスをそのまま(ネイティブに)使う。 | We use cloud services natively and avoid building our own shared features. | ウィユーズ / クラウドサーヴィスィズ / ネイティヴリ / アンダヴォイド / ビルディンガワオウン / シェアドフィーチャーズ |
| システムの構築と運用は、利用システムの責任。 | Building and operating the system is your responsibility. | ビルディンガンオペレイティング / ザシステムイズヨアリスポンスィビリティ |
| アプリだけを可搬にしても、意味がない。 | Making only the application portable is meaningless. | メイキンゴウンリジアプリケイションポータブル / イズミーニングレス |
| 運用中も、データを持ち運べる状態を保つ。 | Keep your data portable during operation, too. | キープヨアデイタポータブル / デュアリンガペレイション / トゥー |

---

## ドリル 4: t / d + you(チュ・ジョ)

**決まり**: [linking-rules.md](linking-rules.md) の 4 と 5

推論: `your` `you` は会話でよく出るので、ここが固いと一番目立つ。「ト ユア」ではなく **チュア**、「ド ユア」ではなく **ジョア**。

### チャンクだけ

| カタカナ | 英語 | 出どころ |
|---|---|---|
| ナッジャスチュア | not just your | [overview.md](overview.md) 7 |
| ウォチュアアカウント | watch your account | [principles/02-native-use/04-aws/](principles/02-native-use/04-aws/README.md) |
| バッチュメイスティルビーヘルドアカウンタブル | but you may still be held accountable | [principles/04-shared-responsibility/03-reasons/](principles/04-shared-responsibility/03-reasons/README.md) |
| アンジョアリスク | and your risk | [overview.md](overview.md) 4 |
| シュリンクヨア | shrink your（k + your はそのまま。決まり 6） | [overview.md](overview.md) 4 |
| メイキョア | Make your（k + your） | [overview.md](overview.md) 7 |

### 文を通す

| 日本語 | English | カタカナ |
|---|---|---|
| アプリだけでなく、データも持ち運べるようにしよう。 | Make your data portable, not just your applications. | メイキョア / デイタポータブル / ナッジャスチュア / アプリケイションズ |
| マネージドサービスを使えば、自分たちの責任範囲とリスクは小さくなる。 | Managed services shrink your responsibility and your risk. | マニジドサーヴィスィズ / シュリンクヨア / リスポンスィビリティ / アンジョアリスク |
| マネージドサービスはリスクを減らすが、説明責任は問われうる。 | Managed services reduce risk, but you may still be held accountable. | マニジドサーヴィスィズリデュースリスク / バッチュメイスティルビーヘルドアカウンタブル |

---

## ドリル 5: 弱形(the / to / and / of)

**決まり**: [linking-rules.md](linking-rules.md) の 7

推論: 弱形は**速く・短く・弱く**。ここを 1 語ずつはっきり言うと、文全体が遅くなり、内容語が目立たなくなる。`the` は子音の前で **ザ**、母音の前で **ジ**。

### チャンクだけ

| カタカナ | 英語 | 出どころ |
|---|---|---|
| エイムズトゥ | aims to | [overview.md](overview.md) 1 |
| バイユーズィンザクラウド | by using the cloud | [overview.md](overview.md) 1 |
| ジアンサー | the answer（母音の前は ジ） | [overview.md](overview.md) 5 |
| コンペアザ | compare the | [overview.md](overview.md) 5 |
| ザガヴァメンクラウド | The Government Cloud | [overview.md](overview.md) 1 |

### 文を通す

| 日本語 | English | カタカナ |
|---|---|---|
| SaaSが常に正解とは限らない。ライフサイクルコストで比べよう。 | SaaS is not always the answer; compare the lifecycle cost. | サースィズ / ナロールウェイズ / ジアンサー / コンペアザ / ライフサイクルコスト |

---

## ドリル 6: 子音 + 母音(語の切れ目が消える)

**決まり**: [linking-rules.md](linking-rules.md) の 1 と 8

推論: 語の切れ目が消えるので、**知っている語なのに聞き取れない**のがこの形。自分で言えるようになると、聞こえるようになる。

### チャンクだけ

| カタカナ | 英語 | 出どころ |
|---|---|---|
| アンダヴォイド | and avoid | [overview.md](overview.md) 2 |
| アンダッドメトリクスグラジュアリ | and add metrics gradually | [topics/operations-modernization.md](topics/operations-modernization.md) |
| ガヴァナンスユーズィズ | Governance uses | [principles/02-native-use/04-aws/](principles/02-native-use/04-aws/README.md) |
| スィキュリティハバンガードデューティ | Security Hub and GuardDuty | [principles/02-native-use/04-aws/](principles/02-native-use/04-aws/README.md) |
| ジオウンリリミッツオン | The only limits on | [principles/02-native-use/04-aws/](principles/02-native-use/04-aws/README.md) |

### 文を通す

| 日本語 | English | カタカナ |
|---|---|---|
| ガバナンスは、ゲートではなくガードレールで行う。 | Governance uses guardrails, not gates. | ガヴァナンスユーズィズ / ガードレイルズ / ナッゲイツ |
| 小さく始めて、指標を少しずつ増やす。 | Start small and add metrics gradually. | スタートスモール / アンダッドメトリクスグラジュアリ |
| Security HubとGuardDutyが見張って、通知してくれる。 | Security Hub and GuardDuty watch your account and notify you. | スィキュリティハバンガードデューティ / ウォチュアアカウント / アンノウティファイユー |

---

## そろえたこと(2026-10-17)

147 組を並べたら、**同じ決まりなのに書き方が違う**所があった。練習で混ざるので、**アメリカ英語に合わせて 27 か所そろえた**(本人「どっちでもいい」)。

| 何が | 前 | 後 | 数 |
|---|---|---|---|
| 母音の前の t(ラ行) | ナッオールウェイズ / ナットイナフ / ナットオンイーシーツー / ナットアバックアップ / ゲタジーキャス / ソウイティズ / ユージットオンリ / セタマンスリ / ワットイズ / イットインクリースィズ / イットアプライズ / ウィザウトアスーミング / セットアップ | ナロールウェイズ / ナリナフ / ナロンイーシーツー / ナラバックアップ / ゲラジーキャス / ソウイリズ / ユーズィロウンリ / セラマンスリ / ワリズ / イリンクリースィズ / イラプライズ / ウィザウラスーミング / セラップ | 20 |
| `-ing` + 母音(決まり 9) | ユーズィン**グエ**イ… / メイキン**グオ**ンリ / デュアリン**グア**ペレイション | ユーズィン**ゲ**イ… / メイキン**ゴ**ウンリ / デュアリン**ガ**ペレイション | 3 |
| 同じ語で 2 通り | ザガヴァメ**ント**クラウド | ザガヴァメ**ン**クラウド | 4 |

- 決めた理由: アプリで鳴らす声(Kokoro の `am_michael` など)が**アメリカ英語**だから。聞こえる音とカタカナが食い違うと、そこでつまずく。`english-app` の `content/core/linking.json`(`get it` → ゲリッ)とも同じ書き方になった。
- 決まり 10 と、その注意(子音のあとはラ行にしない、`n` + t は消える)は [linking-rules.md](linking-rules.md) に書いた。
- ※未検証: 本人の耳で確かめていない。実際の音を聴いて違ったら直す。

---

[← README に戻る](README.md)
