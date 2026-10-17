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

つまずきやすい順に 1 → 5。1 日 1 つでよい。

---

## ドリル 1: 消える t(not / don't / cut / just)

**決まり**: [linking-rules.md](linking-rules.md) の 3(語末の t / d は弱く、小さい `ッ`)

推論: 日本語は t をはっきり出す。「ノット」と言うと、そこで息が切れて、**後ろの語が聞き取れなくなる**。t は止めるだけにして、息を切らずに次の語へ渡す。このリポジトリで一番よく出る形。

### チャンクだけ

| カタカナ | 英語 | 出どころ |
|---|---|---|
| カッコスツ | cut costs | [overview.md](overview.md) 1 |
| ドウンッジャスト | Don't just | [overview.md](overview.md) 3 |
| ナッオールウェイズ | not always | [overview.md](overview.md) 5 |
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

## ドリル 2: `-ing` + 母音(g が次へ渡る)

**決まり**: [linking-rules.md](linking-rules.md) の 9

推論: `-ing` のあとに母音が来ると、g が次の語の頭に移る。日本語の「ビルディング」「ユージング」で止めると、ここが切れる。**グ を次の語にくっつける**と直る。

### チャンクだけ

| カタカナ | 英語 | 出どころ |
|---|---|---|
| ビルディンガワオウン | building our own | [overview.md](overview.md) 2 |
| ビルディンガンオペレイティング | Building and operating | [principles/02-native-use/02-original/](principles/02-native-use/02-original/README.md) |
| ユーズィンゲイダブリューエス | using AWS | [principles/02-native-use/04-aws/](principles/02-native-use/04-aws/README.md)（※） |
| メイキンゴウンリ | making only | [principles/07-data-portability/02-original/](principles/07-data-portability/02-original/README.md)（※） |
| デュアリンガペレイション | during operation | [principles/07-data-portability/02-original/](principles/07-data-portability/02-original/README.md)（※） |

※ 出どころの文では、まだつながっていない書き方（ユーズィン**グエ**イ…）になっている。下の「気づいたこと」を見る。

### 文を通す

| 日本語 | English | カタカナ |
|---|---|---|
| 独自の共通機能は作らず、クラウドサービスをそのまま(ネイティブに)使う。 | We use cloud services natively and avoid building our own shared features. | ウィユーズ / クラウドサーヴィスィズ / ネイティヴリ / アンダヴォイド / ビルディンガワオウン / シェアドフィーチャーズ |
| システムの構築と運用は、利用システムの責任。 | Building and operating the system is your responsibility. | ビルディンガンオペレイティング / ザシステムイズヨアリスポンスィビリティ |
| アプリだけを可搬にしても、意味がない。 | Making only the application portable is meaningless. | メイキンゴウンリジアプリケイションポータブル / イズミーニングレス |
| 運用中も、データを持ち運べる状態を保つ。 | Keep your data portable during operation, too. | キープヨアデイタポータブル / デュアリンガペレイション / トゥー |

---

## ドリル 3: t / d + you(チュ・ジョ)

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

## ドリル 4: 弱形(the / to / and / of)

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
| SaaSが常に正解とは限らない。ライフサイクルコストで比べよう。 | SaaS is not always the answer; compare the lifecycle cost. | サースィズ / ナッオールウェイズ / ジアンサー / コンペアザ / ライフサイクルコスト |

---

## ドリル 5: 子音 + 母音(語の切れ目が消える)

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

## 気づいたこと(カタカナの書き方が 2 通りある所)

147 組を並べると、**同じ決まりなのに書き方が違う**所が見つかった。練習の前に、どちらで覚えるかを決めたい。

| 何が | 片方 | もう片方 | 推論 |
|---|---|---|---|
| `-ing` + 母音 | `building our own` → ビルディン**ガ**ワオウン(つながる) | `using AWS` → ユーズィン**グエ**イダブリューエス、`making only` → メイキン**グオ**ンリ、`during operation` → デュアリン**グア**ペレイション(つながっていない) | 決まり 9 を当てるなら、**ユーズィンゲイ…／メイキンゴウンリ／デュアリンガペレイション**。ドリル 2 はこの形で練習する |
| `not` の t | `not always` → **ナッ**オールウェイズ | `not on EC2` → **ナット**オンイーシーツー | どちらも母音の前。書き方をそろえたい |
| `the Government` | ザガヴァメ**ン**クラウド | ザガヴァメ**ント**クラウド | 同じ語で 2 通り |

### 決めたいこと: 母音の前の t をどうするか

- このリポジトリは、t を**止める**書き方(ナッオールウェイズ)。[linking-rules.md](linking-rules.md) の 3 もそれ。
- 推論: アメリカ英語では、母音にはさまれた t は**ラ行に近い音**(フラップ)になりやすい。`not always` は「ナラ(ー)ルウェイズ」、`not enough` は「ナリナフ」に近い。
- 別の教材(`english-app` の `content/core/linking.json`)は、フラップで書いている(`get it` → ゲリッ、`a lot of` → アララ)。**同じ人が 2 つの書き方で練習すると混ざる**ので、どちらかにそろえたい。
- ※未検証: 本人がどちらの音で聞き取りたいか(アメリカ英語に寄せるか、止める書き方のままか)はまだ決めていない。

---

[← README に戻る](README.md)
