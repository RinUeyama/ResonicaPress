## 判定

スキル入手判定を除き，1D20 を用いる．

## クリア条件

想定の可否を問わず，GM がエンディングと規定したタイミングまで進めること．
各レゾニカにおいては，異常を発生させた要因を解決すること．

## ステータス

健康度，HP，MP のみを持つ．

### 健康度

レゾニカ内の住人としての状態を示す．
|名称|効果|
|:--|:--|
|健康|なし|
|軽傷|なし|
|重症|戦闘不可，撃破か中級以上の毒薬によってのみ到達|
|危篤|戦闘・移動不可|

### HP

レゾニカ内のキャラクターは，マモノに対する盾として HP を持つ．
HP が 0 のときマモノに対して無力であり，この状態で攻撃を受けるとロストする．
HP はマモノ以外の攻撃に対しては影響力を持たず，たとえばレゾニカの住人に襲撃された場合，
GM が都度規定する別のリソースが消費されるか，あるいはフィーリングとして伝えられる．

HP は一部のイベントやアイテムと，ルノンによる修復によってのみ回復する．

### MP

レゾニカの事象を捻じ曲げるためのリソースとして MP を持つ．
MP は戦闘開始時に最大 MP 分保持する．
イベント等で最大 MP が失われた場合，現在 MP もそれに伴い減少する．

## 霧の小道

ルノンと出会い，彼から霧系アイテムを購入したり ステータス の修復を依頼することができる．

|   内容   | 費用 | 詳細                                                          |
| :------: | ---: | :------------------------------------------------------------ |
| 霧の欠片 |  500 | 3 つでスキル 1 つをランダムに生成．またはスキルの帰属を上書き |
| 霧の吐息 | 3000 | 射程 0．自身または味方 1 名の HP を最大 HP の 20％分回復      |
|  霧の雫  | 5000 | 射程 0．自身または味方 1 名の最大 MP 欠損を 1 修復            |
| HP 修復  | 1000 | 減少量問わず最大 HP まで修復                                  |
| MP 修復  | 1000 | 減少量問わず MP の最大値を本来の値まで修復                    |

### スキル習得

霧の欠片や不要なスキルを合計 3 つ使用することでスキル 1 つをランダムに獲得する．

獲得判定

- 1D6, 1D100

スキルは霧の欠片を 1 つ使用することで，帰属 PL を変更することができる．

### アビリティ取得

霧の核をアビリティのランク数だけ使用することで取得することができる．
ただし取得したいアビリティのランクより 1 少ないアビリティを最低 3 種取得していなければならない．

アビリティは霧の枯葉を使用することで未収得状態に戻すことができる．その際，取得に使用した霧の核は返還される．

## 戦闘ルール

### 終了条件

以下のいずれかが満たされた時，戦闘は終了する．

- 戦闘参加者の全員が戦闘を放棄する
- 参加陣営のうち，逃走，戦闘不能等によってただ 1 つの陣営のみが残る

### 戦闘ターン

- PL 側のターン行動  
   それぞれが同時行動する．処理順が重要な場合，PL の任意の順序で解決
- エネミー側のターン行動
  それぞれが同時行動する．処理順が重要な場合，GM の任意の順序で解決

#### ターンの流れ

1. 詠唱が完了したスキルを使用
1. 自身の MP を MPreg 分回復
1. 移動，スキル，アイテムからいずれかを選択
1. 自身が受けた DoT を処理
1. 自身が受けた バフ・デバフ・CC を解除し，一時 CC 耐性を獲得

### 戦場(BF)

BF[1, 2, 3, 4]と間合いが分かれており，自陣は 1, 2，敵陣は 3, 4 に登場する．

#### 移動の妨害

- 味方が現在より大きな数字の間合いに移動する際，同じ間合いに敵がいれば妨害されうる．
- 敵が現在より小さな数字の間合いに移動する際，同じ間合いに味方がいれば妨害してもよい．

妨害は宣言すれば自動成功するが，リープには適用されない．

### 移動

### スキル

|  名称  | 効果                                                                                       |
| :----: | :----------------------------------------------------------------------------------------- |
|  通常  | 自身のターン中に合計で 1 度のみ使用可能                                                    |
|  即時  | いついかなるタイミングでも使用可能．たとえば攻撃を宣言された場合，それに割り込んで使用可能 |
|  貫通  | 射程内の各間合いにいる 1 人ずつを対象として取得                                            |
|  AoE   | 射程内の全員に攻撃                                                                         |
| リープ | 間合い内に敵がいても 1 移動                                                                |
|  詠唱  | 使用宣言をした次のターン開始時に発動                                                       |

### バフ・デバフ・CC

|  名称  |  分類  | 効果                                                        |
| :----: | :----: | :---------------------------------------------------------- |
|  強化  |  バフ  | 最終ダメージ+50％                                           |
|  防御  |  バフ  | 最終ダメージ‐50％                                           |
|  弱化  | デバフ | 最終ダメージ-50％                                           |
|  脆弱  | デバフ | 最終ダメージ+50％                                           |
|  発狂  |   CC   | ターン中，MP を使い切り，攻撃可能なら攻撃しなければならない |
| スネア |   CC   | 移動・リープ・回避不可                                      |

一時 CC 耐性：各耐性+12

### 命中判定

- 命中率：20 + 命中補正 - 被攻撃者の回避率

攻撃者の会心が発生した場合，回避と共存する．

| 名称 | 効果              |
| :--: | :---------------- |
| 会心 | 最終ダメージ+50％ |
| 回避 | 最終ダメージ‐50％ |

### 判定の例

強化状態のキャラクター A（会心率 18）が脆弱状態のキャラクター B（回避率 3）を威力 200 のスキルで攻撃し，
判定で 18 を出した．

- 200 x (1 + 50(強化) + 50(脆弱) + 50(会心) - 50(回避)) = 200 x 2 = 400

なお補正値には上下限が存在する．

|  閾  | 効果量             |
| :--: | :----------------- |
| 上限 | 最終ダメージ+100％ |
| 下限 | 最終ダメージ‐50％  |

## 住人との戦闘

マモノだけではなく，住人と戦闘することもある．
この場合のルールはおおむね上記通りだが，命中判定とダメージの扱いが異なる．

### 命中判定

- 命中率：max([武術 - 被攻撃者の近接武術], [剣術等の武術 - 10])　（最低値：クリティカル率）

戦闘スキルではなく技能の 1 種として扱うため，会心率と回避率は考慮せず，クリティカルとファンブルのみ扱う．

|     名称     | 効果                                  |
| :----------: | :------------------------------------ |
| クリティカル | +1 ダメージ                           |
|  ファンブル  | 武術を一時的に 0 として扱う．行動不可 |
