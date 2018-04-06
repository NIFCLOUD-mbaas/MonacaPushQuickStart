name: inverse
layout: true
class: center, middle, inverse
---
# <span style="font-size: 30%">【Monaca × ニフクラ mobile backend】</span><br>アプリにプッシュ通知を<br>組み込もう！
富士通クラウドテクノロジーズ株式会社

.right[<img src="document-img/takano.png" alt="takano.png" width="150px">]

.footnote[
20180411 MonacaPushQuickStart
]

---
layout: true
class: center, middle, inverse_sub
---
# はじめに

---
layout: false

.footnote_right[
はじめに
]

## はじめに
### プッシュ通知はなぜアプリに必要なのか？

.center[
<img src="document-img/push_image.png" alt="push_image" width="450px">
]

---
.footnote_right[
はじめに
]

### アプリの存在は忘れてしまうもの…
１人が１ヶ月に１回以上起動するアプリの数は .color_red[__およそ .size_large_20[27個]__]<br>
１人が１ヶ月に10回以上起動するアプリの数 .color_red[__わずか .size_large_20[9個]__]


.center[
<img src="document-img/app_image_01.png" alt="app_image_01" width="400px">
]

と言われています。アクティブに使われるアプリになるのはとても大変です…<br>
そこで、プッシュ通知が活躍してくる訳ですが、その使い方には工夫も必要です。

---
.footnote_right[
はじめに
]

### 1. アプリの変化を伝える役割
アプリのオートアップデートが当たり前になった今、新機能追加やバージョンアップがされても、そのままでは気づく手段がありません。<br>
__新しい機能を紹介やバージョンアップのお知らせ__ を伝えるためにプッシュ通知は有効と言えます。

.center[
<img src="document-img/app_image_02.png" alt="app_image_02" width="600px">
]


---
.footnote_right[
はじめに
]

### 2. リマインダーとしての役割
しつこく送り続けると受信しない設定にされる可能性があるプッシュ通知ですが、ユーザがあえて通知を受けたいと思うアプリがあります。<br>
__メッセージ系アプリ・リマインダー系アプリ__ がその例です。<br>
特定の時間や特定の場所に行ったときなど、ユーザーに応じてプッシュ通知を出し分けています。この通知の仕方であれば __ユーザにストレスを与えることなく__ アプリの存在を思い出してもらうことができます。

.center[
<img src="document-img/app_image_03.png" alt="app_image_03" width="550px">
]

---
.footnote_right[
はじめに
]

### 3. アプリを立ち上げずに内容を把握させる役割
今や当たり前となりましたが、送られて来たメッセージはプッシュ通知としてロック画面にも表示されるようになっています。<br>
アプリを起動せずとも「本文」を読むことができるので、返信をするかどうか、<br>
つまり __アプリを開くかどうかをプッシュ通知の内容で選択ができます__ 。
<br><br><br>

.center[
<img src="document-img/app_image_04.png" alt="app_image_04" width="650px">
]

---
.footnote_right[
はじめに
]

### まとめると…
* 上手にプッシュ通知を活用することでアプリを活性化させることが可能です！

.center[
<img src="document-img/app_image_05.png" alt="app_image_05" width="600px">
]

<br>
それではアプリの活性化に欠かせないプッシュ通知の導入方法について学んでいきましょう！

---
.footnote_right[
はじめに
]
### Monacaって何？
* __もなか 【[Monaca](https://ja.monaca.io/)】__ HTML5/JavaScript/CSS3でスマホアプリが開発できる開発環境。開発スタイル／コーディング環境は選択可能。

.center[![Monacaとは？](document-img/AboutMonaca.png)]

---
.footnote_right[
はじめに
]
### ニフクラ mobile backend って何？
* __にふくら-もばいる-ばっくえんど 【[ニフクラ mobile backend](http://mb.cloud.nifty.com/about.htm)】__ スマートフォンアプリに必要なバックエンド機能が開発不要で利用できるクラウドサービス。 クラウド上に用意された機能をAPIで呼び出すだけで利用できます。また、APIを簡単に使うためのSDKを用意しています（ iOS / Android / Monaca / Unity ）。mobile Backend as a Service の頭文字を取って、通称 **mBaaS** と呼ばれています。

.center[<img src="document-img/About_mBaaS.png" alt="mBaaSとは？" width="350px">]

---
.footnote_right[
はじめに
]

### Monaca と mBaaS で<br>サーバー連携アプリは簡単に実現可能に
この２つを組み合わせると、高度なアプリも簡単スピーディーに開発できます

.center[![Monaca×mBaaS](document-img/Monaca_mBaaS.png)]

.left-column[
__《アプリ側》Monaca のすごいところ__
.size_small_7[
* 無料で使える！
* iOS / Android 同時に開発可能！
* いつでもどこでも、ブラウザで開発OK！
]
]
.right-column[
__《サーバー側》mBaaS のすごいところ__
.size_small_7[
* 無料で使える！
* **バックエンドの開発・運用は一切不要**！
* **管理画面** からクラウドの状況を確認できる！
]
]

---
.footnote_right[
はじめに
]

## 今回体験する内容

動作確認端末（ iOS / Android ）により内容が異なります

### 講義
#### プッシュ通知の仕組み
* プッシュ通知が配信されて、端末に届くまでの流れを紹介します

### ハンズオン
#### プッシュ通知の導入方法
* 実際に Monaca でアプリを作成し、mBaaS でプッシュ通知を導入する手順を紹介します


---
layout: false

.footnote_right[
.right[
はじめに<br>準備
]
]

## 準備
### 事前準備
#### 共通
下記登録を完了し、アカウントを作成しておいてください

* [Monaca](https://ja.monaca.io/register/start.html) の利用登録（無料）
* [ニフクラ mobile backend](http://mb.cloud.nifty.com/signup.htm) の利用登録（無料）

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]


---
layout: false

.footnote_right[
.right[
はじめに<br>準備
]
]

### 事前準備
#### iOS で動作確認をするの場合
* Mac （OSは最新版推奨）
  * 「キーチェーンアクセス」「Xcode」を利用します
  * Chrome 最新版
* 動作確認用 iPhone または iPad（iOS 9 以降）
* [Apple Developer Program アカウントの取得](https://developer.apple.com/programs/jp/)（__有料：99米ドル/年__）

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
layout: false

.footnote_right[
.right[
はじめに<br>準備
]
]

### 事前準備
#### Android で動作確認をするの場合
* PC
 * Chrome 最新版
* 動作確認用 Android（OS 4以降）
* [Google アカウントの取得](https://accounts.google.com/SignUp)（__無料__）

.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]



---
layout: true
class: center, middle, inverse_sub
---
# 講義

---
layout: false

.footnote_right[
.right[
講義<br>目次
]
]

## 目次

.size_large_13[
1. プッシュ通知配信の仕組み
1. プッシュ通知配信に必要な準備と設定
  * iOS で動作確認をする場合
  * Android で動作確認をする場合
]

---
layout: false

.footnote_right[
.right[
講義<br>1. プッシュ通知配信の仕組み
]
]

## 1. プッシュ通知配信の仕組み

.size_small_9[
* プッシュ通知の配信は必ず APNs / FCM という iOS / Android のプッシュ通知配信サーバーを介して行っています
* アプリの起動時にプッシュ通知受信のための準備として図の ①～③の処理が行われます
  * ① アプリ側から APNs / FCM へプッシュ通知の許可を行うと、② APNs / FCM から デバイストークン / レジスタレーションID という端末とアプリを識別するためのIDが発行されます
  * 取得した デバイストークン / レジスタレーションID はプッシュ通知の配信時に使用する為 ③ アプリ側から mBaaS に保存されます
]

.center[
<img src="document-img/shikumi_01.png" alt="shikumi_01" width="700px">
]

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]
---
.footnote_right[
.right[
講義<br>1. プッシュ通知配信の仕組み
]
]

.size_small_9[
* プッシュ通知配信時には ④～⑥ の処理が行われ、アプリへプッシュ通知が配信されます
   * ④ mBaaS でプッシュ通知の配信登録がされると ⑤ mBaaS から APNs / FCM にプッシュ通知の配信依頼がされます
      * このとき デバイストークン / レジスタレーションID が使われます
   * ⑥ APNs / FCM から順次アプリ側へプッシュ通知が配信されます
]

.center[
<img src="document-img/shikumi_02.png" alt="shikumi_02" width="700px">
]

.size_small_9[
ただし、 APNs / FCM を利用するためには、 証明書 / サーバーキー などを用意し、アプリ側または mBaaS 側に設定する必要があります
]

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
講義<br>2. プッシュ通知配信に必要な準備
]
]

## 2. プッシュ通知配信に必要な準備と設定
### iOS で動作確認をする場合

.center[
<img src="document-img/shikumi_03.png" alt="shikumi_03" width="500px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
講義<br>2. プッシュ通知配信に必要な準備
]
]

.size_small_9[
* iOS の場合は作成に必要なアカウントが有償だったり、作成するファイルに参照関係があるため、参照元から順に作成していく必要があったりと少々面倒です
* また操作を１つでも誤るとプッシュ通知が正しく送られないので注意が必要です
]


.center[
<img src="document-img/shikumi_04.png" alt="shikumi_04" width="500px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
講義<br>2. プッシュ通知配信に必要な準備
]
]

### Android で動作確認をする場合

.size_small_9[
* Android の場合は Google アカウントがあれば特に難しい操作不要で、簡単に準備ができます
]

.center[
<img src="document-img/shikumi_05.png" alt="shikumi_05" width="700px">
]

.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]

---
layout: true
class: center, middle, inverse_sub
---
# ハンズオン


---
layout: false

.footnote_right[
.right[
ハンズオン<br>作業手順
]
]

## 作業手順

.size_small_9[
1. プッシュ通知受信に必要な準備
  * iOSで動作確認する場合
  * Androidで動作確認する場合
1. mBaaSの準備
  * アプリ新規作成
  * プッシュ通知設定
1. Monacaの準備
  * プロジェクト新規作成
  * プッシュ通知プラグインの有効化
  * 実装と mBaaS APIキーの設定
     * Androidで動作確認する場合のみ
1. ビルド
  * iOSで動作確認する場合
  * Androidで動作確認する場合
1. 動作確認と実装コード解説
  * iOSで動作確認する場合
  * Androidで動作確認する場合
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

## 1. プッシュ通知受信に必要な準備
### iOSで動作確認する場合
次の 1.～8. の手順で必要なファイルを作っていきます

.left-column[
.size_small_9[
1. __CSRファイル__ の作成 .size_small_5[.color_red[※初回のみ]]
1. __開発用証明書.cer__ の作成 .size_small_5[.color_red[※初回のみ]]
1. __開発用証明書秘密鍵.p12__ の作成
1. __App ID__ の作成（Bundle ID）
1. __端末登録__ .size_small_5[.color_red[※初回のみ]]
1. __プロビジョニングプロファイル__ の作成
1. __プッシュ通知用証明書.cer__ の作成
1. __プッシュ通知用証明書.p12__ の作成
]
]

.right-column[
<img src="document-img/APNs_00.PNG" alt="APNs_00" width="350px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

#### 1. CSRファイル の作成 .size_small_7[.color_red[※初回のみ]]

.size_small_9[
* キーチェーンアクセスを開きます
* 「キーチェーンアクセス」＞「証明書アシスタント」＞「認証局に証明書を要求」をクリックします
* 「ユーザーのメールアドレス」を入力します<br>（「通称」はそのまま、「CAのメールアドレス」は空欄でOK）
* 「要求の処理」は「ディスクに保存」を選択し「鍵ペア情報を設定」にチェックを入れます
* 「続ける」をクリックします
]

.center[
<img src="document-img/APNs_02.PNG" alt="APNs_02" width="650px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

#### 1. CSRファイル の作成 .size_small_7[.color_red[※初回のみ]]

.size_small_9[
* 保存先の選択が出るので任意の場所を選択し「保存」をクリックします
* 「鍵ペア情報」画面を確認して「続ける」をクリックします
* 「設定結果」画面が出るので「完了」をクリックします
]

.center[
<img src="document-img/APNs_03.PNG" alt="APNs_03" width="650px">
]

.size_small_9[
* CSRファイルの作成は完了です
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

#### 2. 開発用証明書.cer の作成 .size_small_7[.color_red[※初回のみ]]
.size_small_9[
* [Apple Developer Program](https://developer.apple.com/account/) にログインします https://developer.apple.com/account/
* 「Certificates, Identifiers & Profiles」をクリックします
]

.center[
<img src="document-img/APNs_04.PNG" alt="APNs_04" width="450px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* 「Certificates」＞「All」をクリックし、右上の「 + 」をクリックします
* 「Add iOS Certificate」画面が表示されるので設定していきます
* 「iOS App Development」にチェックをいれ、下の方の「Continue」をクリックします
* 次の画面も「Continue」をクリックして進みます
]

.center[
<img src="document-img/APNs_05.PNG" alt="APNs_05" width="650px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* 1. で作成した「CSRファイルの作成」を選択し、「Continue」をクリックします
]

.center[
<img src="document-img/APNs_06.PNG" alt="APNs_06" width="325px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* 開発者用証明書.cer が作成されるので、「Download」をクリックして任意の場所に書き出します
* ダウンロードが終わったら「Done」をクリックします
]

.center[
<img src="document-img/APNs_07.PNG" alt="APNs_07" width="325px">
]

.size_small_9[
* 開発用証明書.cer の作成は完了です
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]


---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

#### 3. 開発用証明書秘密鍵.p12 の作成
.size_small_9[
* Monacaでアプリをビルドする際は開発用証明書の秘密鍵が必要です
* 2.で作成した開発用証明書.cer をダブルクリックしてキーチェーンアクセスを開きます
]

.center[
<img src="document-img/APNs_23.PNG" alt="APNs_23" width="700px">
]

.size_small_9[
* 証明書左側に三角マークがあり、クリックすると中に秘密鍵が確認できます
* 確認したら閉じて図のようにしておきましょう
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* 閉じた状態で右クリックして「"iPhone Developer: ～"を書き出す…」をクリックします
]

.center[
<img src="document-img/APNs_24.PNG" alt="APNs_24" width="700px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* ファイル名「名前」と保存先「場所」を指定して「保存」をクリックします
* パスワードを求められますが、 __何も入力しない__ で「OK」をクリックします
]

.center[
<img src="document-img/APNs_25.PNG" alt="APNs_25" width="700px">
]

.size_small_7[
※この後、システム側にパスワードを求められる場合があります。対応してください。
]

.size_small_9[
* 開発用証明書秘密鍵.p12 が書き出されます
* 開発用証明書秘密鍵.p12 作成は完了です
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

#### 4. App ID の作成（Bundle ID）
.size_small_7[
※ 2. をスキップした方は、[Apple Developer Program](https://developer.apple.com/account/) を開き、「Certificates, Identifiers & Profiles」をクリックします
]

.size_small_9[
* 「Identifiers」の「AppIDs」をクリックして、右上の「＋」をクリックします
* 上から順に設定していきます
* まず「App ID Description」の「Name」にアプリの概要を記入します
* 次に「App ID Suffix」では「Explicit App ID」を選択し、「Bundle ID」を入力します
  * 「Wildcard App ID」ではプッシュ通知が利用できないので注意！
  * 「Bundle ID」はアプリ側で同じものを設定しますので必ず控えておきましょう
]
  .center[
  <img src="document-img/APNs_08.PNG" alt="APNs_08" width="700px">
  ]


.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* 最後に「App Services」では「Push Notifications」にチェックを入れます
  * これを忘れるとプッシュ通知が利用できないので注意！
* 「Continue」をクリックします
]

.center[
<img src="document-img/APNs_09.PNG" alt="APNs_09" width="400px">
]


.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* 「Push Notifications」が__Configurable__になっていることを確認しましょう
* 「Register」をクリックし次の画面で「Done」をクリックします
]

.center[
<img src="document-img/APNs_10.PNG" alt="APNs_10" width="700px">
]

.size_small_9[
* これで App ID 作成は完了です
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

#### 5. 端末登録 .size_small_7[.color_red[※初回のみ]]
.size_small_9[
* 「Devices」＞「All」をクリックして、右上の「＋」をクリックします
* 「Register Device」を選択し、端末の「Name」と「UUID」を入力します
]

.center[
<img src="document-img/APNs_11.PNG" alt="APNs_11" width="400px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* 端末のUUIDはXcodeを使うと確認し易いです
  * Mac に端末を接続し、Xcodeを起動します
  * 「Window」＞「Devices and Simulators」をクリックします
  * 「identifier」としてUUIDが確認できます
]

.center[
<img src="document-img/APNs_12.PNG" alt="APNs_12" width="600px">
]

.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* 記入できたら「Continue」をクリックします
* 次の画面で端末情報を確認して「Register」をクリックします
* 更に次の画面で「Done」をクリックすると端末登録は完了です
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

#### 6. プロビジョニングプロファイル の作成

.size_small_9[
* 「Provisioning Profiles」＞「All」をクリックして、右上の「＋」をクリックします
* 利用する App ID、開発用証明書、端末をそれぞれ紐付けていきます
* 「Development」の「iOS App Development」を選択し「Continue」をクリックします
]

.center[
<img src="document-img/APNs_13.PNG" alt="APNs_13" width="350px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* 4.で作成した App ID を選択し、「Continue」をクリックします
* 2.で作成した（あるいは既存の） 開発用証明書 を選択し「Continue」をクリックします
]

.center[
<img src="document-img/APNs_14.PNG" alt="APNs_14" width="700px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* 5.で登録した（あるいは既存の）端末を選択し、「Continue」をクリックします
* 最後に「Profile Name」にファイル名入力します
* 紐付けを確認し「Continue」をクリックします
]

.center[
<img src="document-img/APNs_15.PNG" alt="APNs_15" width="700px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* プロビショニングプロファイルがが作成されるので、「Download」をクリックして書き出します
* ダウンロードが終わったら「Done」をクリックします
]

.center[
<img src="document-img/APNs_16.PNG" alt="APNs_16" width="350px">
]

.size_small_9[
* プロビショニングプロファイルの作成は完了です
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

#### 7. プッシュ通知用証明書.cer の作成
.size_small_9[
* 「Certificates」＞「All」をクリックして、右上の「＋」をクリックします
* 2.で開発用証明書を作成したときとは異なり、「Development」の「Apple Push Notification service SSL (Sandbox)」を選択し、 「Continue」をクリックします
]

.center[
<img src="document-img/APNs_17.PNG" alt="APNs_17" width="350px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* 4.で作成した App ID を選択し、「Continue」をクリックします
* 次の画面は「Continue」をクリックして進みます
]

.center[
<img src="document-img/APNs_18.PNG" alt="APNs_18" width="700px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* 1.で作成した（あるいは既存の）CSRファイルを選択し「Continue」をクリックします
* プッシュ通知用証明書.cer が作成されるので「Download」をクリックして書き出します
* ダウンロードが終わったら「Done」をクリックします
]

.center[
<img src="document-img/APNs_19.PNG" alt="APNs_19" width="700px">
]

.size_small_9[
* プッシュ通知用証明書.cer の作成は完了です
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

#### 8. プッシュ通知用証明書.p12 の作成

.size_small_9[
* 7.で作成した プッシュ通知用証明書.cer をダブルクリックしてキーチェーンアクセスを開きます
* プッシュ通知用証明書.cer の左にある三角マークをクリックして開きます
  * プッシュ通知用証明書.cer ファイルには鍵がセットされています
]

.center[
<img src="document-img/APNs_20.PNG" alt="APNs_20" width="700px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* プッシュ通知用証明書.p12 を書き出すには、開いた状態で __鍵ではなく証明書の上で右クリック__ をして「～を書き出す…」をクリックします
]

.center[
<img src="document-img/APNs_21.PNG" alt="APNs_21" width="700px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

.size_small_9[
* ファイル名「名前」と保存先「場所」を指定して「保存」をクリックします
* パスワードを求められますが、 __何も入力しない__ で「OK」をクリックします
]

.center[
<img src="document-img/APNs_22.PNG" alt="APNs_22" width="700px">
]

.size_small_9[
※この後、システム側にパスワードを求められる場合があります。対応してください。

* プッシュ通知用証明書.p12 が書き出されます
* プッシュ通知用証明書.p12 作成は完了です
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

#### 確認

.size_small_9[
* 下記のファイルが作成されていればOKです
* て１つのフォルダに保存しておきましょう
  * App ID はテキストに控えておきましょう
]

.center[
<img src="document-img/APNs_00.PNG" alt="APNs_00" width="600px">
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

### Androidで動作確認する場合

* [Firebase Console](https://console.firebase.google.com/)にアクセスします https://console.firebase.google.com/
  * プッシュ通知の配信に必要な __サーバーキー__、 __送信者ID__ を取得します
* プロジェクトを新規作成します
  * 「プロジェクトの追加」をクリックします

.center[
<img src="document-img/FCM_01.png" alt="FCM_01" width="600px">
]

.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

* プロジェクトの追加画面が開くので、プロジェクト名と国/地域を入力し、「プロジェクトを作成」をクリックします

.center[
<img src="document-img/FCM_02.png" alt="FCM_02" width="400px">
]


.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

* しばらく待つと以下の画面が表示されるので「次へ」をクリックします

.center[
<img src="document-img/FCM_03.png" alt="FCM_03" width="350px">
]

.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

* コンソール画面が表示されるので、左上の設定（歯車マーク）をクリックし、「プロジェクトの設定」をクリックします

.center[
<img src="document-img/FCM_04.png" alt="FCM_04" width="700px">
]

.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>1. プッシュ通知受信に必要な準備
]
]

* 設定画面が開かれます
* 上部タブの「クラウドメッセージング」をクリックします
* プロジェクト認証情報として「サーバーキー」と「送信者ID」を確認できます

.center[
<img src="document-img/FCM_05.png" alt="FCM_05" width="700px">
]

* これらのコードは後ほど使います（このまま開いておいてください）

.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]


---
.footnote_right[
.right[
ハンズオン<br>2. mBaaSの準備
]
]

## 2. mBaaSの準備
* mBaaS にログインします http://mb.cloud.nifty.com/

.center[<img src="document-img/mBaaS_1.png" alt="mBaaSの準備1" width="600px">]


.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>2. mBaaSの準備
]
]

### アプリ新規作成

* 新しいアプリを作成します
* アプリ名を入力し、「新規作成」をクリックします 例）.color_blue[__PushDemo__]

.center[![mBaaSの準備2-1](document-img/mBaaS_2-1.png)]

* mBaaSを既に使用したことがある場合は、画面上方のメニューバーにある「+新しいアプリ」をクリックすると同じ画面が表示されます

.center[![mBaaSの準備2-2](document-img/mBaaS_2-2.png)]

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>2. mBaaSの準備
]
]

* アプリが作成されるとAPIキー（２種類）が発行されます
 * APIキーは後で使用します
* ここでは使用しないので、「OK」で閉じます

.center[![mBaaSの準備3](document-img/mBaaS_3.png)]

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>2. mBaaSの準備
]
]

* 管理画面が表示されます

.center[<img src="document-img/mBaaS_4.png" alt="mBaaSの準備4" width="600px">]

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>2. mBaaSの準備
]
]

### プッシュ通知設定

* プッシュ通知の設定をします
* 右上の「アプリ設定」をクリックして、「プッシュ通知」をクリックします

.center[<img src="document-img/mBaaS_5.png" alt="mBaaS_5" width="600px">]

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>2. mBaaSの準備
]
]

#### iOSで動作確認する場合

* 「プッシュ通知の許可」設定・保存と「証明書（p12）」として先ほど作成した「プッシュ通知用証明書.p12」を選択しアップロードします


.center[<img src="document-img/mBaaS_6.png" alt="mBaaS_6" width="600px">]


.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>2. mBaaSの準備
]
]

#### Androidで動作確認する場合

* 「プッシュ通知の許可」設定と「APIキー」として先ほど取得した「サーバーキー」を貼り付け、それぞれ保存します

.center[<img src="document-img/mBaaS_7.png" alt="mBaaS_7" width="600px">]


.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

## 3. Monacaの準備

* Monacaにログインをします

.center[<img src="document-img/Monaca_01.png" alt="Monaca_01" width="700px">]

https://ja.monaca.io/

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

### プロジェクト新規作成

* 新規でプロジェクトを作ります
* 「新規プロジェクトの作成」をクリックします
* テンプレート選択画面で「No Framework」をクリックすると「最小限のテンプレート」が表示されますので、「作成」をクリックします

.center[<img src="document-img/Monaca_02.png" alt="Monaca_02" width="650px">]

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

* 「プロジェクト名」を入力し、「プロジェクトを作成する」をクリックします

.center[<img src="document-img/Monaca_03.png" alt="Monaca_03" width="350px">]

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

* プロジェクトが開かれます

.center[<img src="document-img/Monaca_04.png" alt="Monaca_04" width="700px">]


.size_small_7[
* 今回はプレビュー画面は使用しないので、「プレビュー」タブをクリックして閉じておきましょう
]

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]


---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

### プッシュ通知プラグインの有効化

* ｍBaaS のプッシュ通知を利用するためのプラグインを導入します
* 「設定」タブをクリックして、「Cordovaプラグインの管理...」をクリックします

.center[<img src="document-img/Monaca_05.png" alt="Monaca_05" width="350px">]

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

* 検索窓に `ncmb` と入力して、Enterボタンを押します

.center[<img src="document-img/Monaca_06.png" alt="Monaca_06" width="650px">]

* すると「NifCloudMB」というプラグインが表示されます

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

* プラグインにカーソルを合わせると吹き出しが表示されます
* 吹き出し内の「有効」をクリックします

.center[<img src="document-img/Monaca_07.png" alt="Monaca_07" width="650px">]

* 有効なプラグインとして表示されればOKです

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

### 実装と mBaaS APIキーの設定

* 引き続きmBaaSとの連携のための設定を行います
* 既に開いている `index.html` タブをクリックして表示します
* `<script></script>`タグ内にコードを書いていきます

.center[<img src="document-img/Monaca_08.png" alt="Monaca_08" width="650px">]


.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

### 実装と mBaaS APIキーの設定

* 次のコードを全てコピーして `<script></script>`タグ内に貼り付けてください


.size_large_13[

```js
document.addEventListener("deviceready", function(){
    // デバイストークンを取得してinstallationに登録する
    window.NCMB.monaca.setDeviceToken(
        "YOUR_NCMB_APPLICATION_KEY",
        "YOUR_NCMB_CLIENT_KEY",
        "YOUR_FCM_SENDER_ID"
    );
},false);
```
]

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

* こんな感じになればOKです

.center[<img src="document-img/Monaca_09.png" alt="Monaca_09" width="650px">]

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

* 次は赤枠内を設定してきます

.center[<img src="document-img/Monaca_10.png" alt="Monaca_10" width="650px">]

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

* 上２つに mBaaS でアプリ新規作成時に発行された APIキー（アプリケーションキーとクライアントキー）を設定します

.center[<img src="document-img/code_api.png" alt="code_api" width="400px">]

* APIキーはmBaaSの管理画面「アプリ設定」＞「基本」で確認できます
* アプリケーションキーとクライアントキーをコピーして、それぞれ`YOUR_NCMB_APPLICATIONKEY`と`YOUR_NCMB_CLIENTKEY`に貼り付けます
* このとき、ダブルクォーテーション「`"`」は消さないように注意しましょう

.center[<img src="document-img/confirm_apikey.png" alt="SDK初期化2" width="600px">]


.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

* こんな感じになればOKです

.center[<img src="document-img/code_api_2.png" alt="code_api_2" width="700px">]

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

#### Androidで動作確認する場合のみ

* ３つ目も設定します

.center[<img src="document-img/code_api_3.png" alt="code_api_3" width="400px">]

* Firebase console で確認した「送信者ID」を貼り付けます
* こんな感じになればOKです

.center[<img src="document-img/code_api_4.png" alt="code_api_4" width="700px">]

.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>3. Monacaの準備
]
]

### .color_blue[作業が完了したら保存を忘れずに！]
* メニューバーの「保存」をクリックします
 * Windowsの場合は、「Ctrl + S」でも保存できます
 * Macの場合は、「Command + S」でも保存できます

正しく保存されていないとビルドに成功してもプッシュ通知が届きません！<br>
忘れずに実施してください。

.footnote[
<img src="document-img/both_icon.png" alt="both_icon" width="100px">
]

---
.footnote_right[
.right[
ハンズオン<br>4. ビルド
]
]

## 4. ビルド
### iOS で動作確認する場合

.size_small_9[
* Monaca で「設定」＞「iOSアプリ設定...」を開きます
* アプリケーション名を変更します（任意）
* App ID を変更します
  * 準備の 4.で App ID 作成時に設定した「 Bundle ID 」に書き換えます
]

.center[<img src="document-img/build_iOS_01.png" alt="build_iOS_01" width="650px">]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>4. ビルド
]
]

.size_small_9[
* 次にで「設定」＞「iOSビルド設定...」を開きます
* 「秘密鍵と証明書のインポート」の「インポート」をクリックします
]

.center[<img src="document-img/build_iOS_02.png" alt="build_iOS_02" width="700px">]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>4. ビルド
]
]

.size_small_9[
* 準備の 3.で作成した 開発用証明書秘密鍵.p12 を設定します
* 「参照する」をクリックしてファイルを選択し、「インポート」をクリックします
  * 「キーのパスワード」は設定していないので空欄でOKです
]

.center[<img src="document-img/build_iOS_03.png" alt="build_iOS_03" width="500px">]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>4. ビルド
]
]

.size_small_9[
* 「Monacaに登録された証明書」を確認すると「証明書」欄に 開発用証明書 が登録されたことが確認できます
* 確認したら、次に「プロファイルのアップロード」をクリックします
]

.center[<img src="document-img/build_iOS_04.png" alt="build_iOS_04" width="700px">]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>4. ビルド
]
]

.size_small_9[
* 準備の 6.で作成した プロビジョニングプロファイルを選択し設定します
* 設定できると「プロファイル」欄に プロビジョニングプロファイルが登録されたことを確認できます
]

.center[<img src="document-img/build_iOS_05.png" alt="build_iOS_05" width="700px">]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>4. ビルド
]
]

.size_small_9[
* 最後に「ビルド」＞「iOSアプリのビルド」を開きます
* 「デバッグ向けビルド」の「デバッグビルド」が選択されていることを確認して、「ビルドを開始する」をクリックします
]

.center[<img src="document-img/build_iOS_06.png" alt="build_iOS_06" width="700px">]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>4. ビルド
]
]

.size_small_9[
* ブラウザの別のタブが開き、ビルドが開始されます
* 少し待つとビルドが完了します
]

.center[<img src="document-img/build_iOS_07.png" alt="build_iOS_07" width="650px">]

.size_small_9[
* QRコードから端末にアプリをダウンロードしましょう
]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>4. ビルド
]
]

### Android で動作確認する場合

.size_small_9[
* 「ビルド」＞「iOSアプリのビルド」を開きます
* 「デバッグ向けビルド」の「デバッグビルド」が選択されていることを確認して、「ビルドを開始する」をクリックします
]

.center[<img src="document-img/build_Android_01.png" alt="build_Android_01" width="700px">]


.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>4. ビルド
]
]

.size_small_9[
* ブラウザの別のタブが開き、ビルドが開始されます
* 少し待つとビルドが完了します
]

.center[<img src="document-img/build_Android_02.png" alt="build_Android_02" width="700px">]

.size_small_9[
* QRコードから端末にアプリをダウンロードしましょう
]

.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>5. 動作確認と実装コード解説
]
]

## 5. 動作確認と実装コード解説
### iOS で動作確認する場合

.left-column[
.size_small_9[
* インストールしたアプリを起動します
* プッシュ通知の許可を求めるアラートが出たら、必ず許可してください
* 端末側で起動したアプリは一度閉じておきます
]
]

.right-column[.center[<img src="document-img/push_iOS_01.png" alt="push_iOS_01" width="230px">]]



.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>5. 動作確認と実装コード解説
]
]

.size_small_9[
* 起動時「デバイストークン」が取得され、端末情報が mBaaS に保存されます
* mBaaS の管理画面から「データストア」＞「installation」クラスを開いて確認します
]

.center[<img src="document-img/push_iOS_02.png" alt="push_iOS_02" width="700px">]

.size_small_9[
* 端末情報を確認できます
  * deviceToken
  * deviceType
  * timeZone など
]

.center[<img src="document-img/push_iOS_03.png" alt="push_iOS_03" width="700px">]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>5. 動作確認と実装コード解説
]
]

.size_small_9[
* プッシュ通知を送ってみましょう
* 「プッシュ通知」＞「＋新しいプッシュ通知」をクリックします
]

.center[<img src="document-img/push_iOS_04.png" alt="push_iOS_04" width="600px">]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>5. 動作確認と実装コード解説
]
]

.size_small_9[
* プッシュ通知のフォームが開かれます
* 「メッセージ」の入力、「iOS端末に配信する」へのチェックを入れます
* 「1端末に向けて送信されます」と表記されれば準備OKです
* 「プッシュ通知を作成する」をクリックしてプッシュ通知を配信します
]

.center[<img src="document-img/push_iOS_05.png" alt="push_iOS_05" width="700px">]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>5. 動作確認と実装コード解説
]
]

.size_small_9[
* 少し待つと端末側にプッシュ通知が届きます
* mBaaS 側で配信まで以下のようにステータスが変化します
]

.center[<img src="document-img/push_iOS_06.png" alt="push_iOS_06" width="700px">]

.footnote[
<img src="document-img/iOS_icon.png" alt="iOS_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>5. 動作確認と実装コード解説
]
]

### Android で動作確認する場合

.left-column[
.size_small_9[
* インストールしたアプリを起動します
* 端末側で起動したアプリは一度閉じておきます
]
]

.right-column[.center[<img src="document-img/push_Android_01.png" alt="push_Android_01" width="230px">]]

.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>5. 動作確認と実装コード解説
]
]

.size_small_9[
* 起動時「レジスタレーションID」が取得され、端末情報が mBaaS に保存されます
* mBaaS の管理画面から「データストア」＞「installation」クラスを開いて確認します
]

.center[<img src="document-img/push_Android_02.png" alt="push_Android_02" width="700px">]

.size_small_9[
* 端末情報を確認できます
  * deviceToken
  * deviceType
  * timeZone など
]

.center[<img src="document-img/push_Android_03.png" alt="push_Android_03" width="700px">]

.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>5. 動作確認と実装コード解説
]
]

.size_small_9[
* プッシュ通知を送ってみましょう
* 「プッシュ通知」＞「＋新しいプッシュ通知」をクリックします
]

.center[<img src="document-img/push_iOS_04.png" alt="push_iOS_04" width="600px">]

.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>5. 動作確認と実装コード解説
]
]

.size_small_9[
* プッシュ通知のフォームが開かれます
* 「メッセージ」の入力、「Android端末に配信する」へのチェックを入れます
* 「1端末に向けて送信されます」と表記されれば準備OKです
* 「プッシュ通知を作成する」をクリックしてプッシュ通知を配信します
]

.center[<img src="document-img/push_Android_04.png" alt="push_Android_04" width="700px">]

.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]

---
.footnote_right[
.right[
ハンズオン<br>5. 動作確認と実装コード解説
]
]

.size_small_9[
* 少し待つと端末側にプッシュ通知が届きます
* mBaaS 側で配信まで以下のようにステータスが変化します
]

.center[<img src="document-img/push_Android_05.png" alt="push_Android_05" width="680px">]

.footnote[
<img src="document-img/Android_icon.png" alt="Android_icon" width="50px">
]

---
## まとめ
### __プッシュ通知を体験しました！__

* プッシュ通知の仕組みを学びました
   * アプリ起動時の処理
   * プッシュ通知配信時の処理
* プッシュ通知の実装方法を学びました
   * プッシュ通知に必要な準備
      * iOSの場合は準備が少し面倒…
   * Monaca で mBaaS の実装は非常に簡単！！
      * プラグインの導入
      * 数行のコード

---
layout: true
class: center, middle, inverse_sub
---
# おわりに

---
layout: false

## おわりに
いかがでしたでしょうか？こんなに使いやすくて便利な mBaaS をもっと活用してみたい方へ、mBaaS の各機能をすぐに試すことができるサンプルアプリを多数ご用意しています。Monaca にサンプルプロジェクトをインポートして、簡単な操作をするだけですぐにお試しいただけます！ぜひご活用ください。

.size_large_11[
* [mobile backend を体験しよう！](https://github.com/NIFCloud-mbaas/monaca_data_registration)
 * 使用機能 / データストア
* [アプリにログイン機能をつけよう！](https://github.com/NIFCloud-mbaas/monaca_login_template)
 * 使用機能 / 会員管理
* [地図アプリを作ろう！](https://github.com/NIFCloud-mbaas/MonacaMapApp)
 * 使用機能 / データストア,位置情報検索
* [and more...](http://mb.cloud.nifty.com/doc/current/tutorial/tutorial_monaca.html)
]

---
## 本日の資料配布について
.size_small_9[
アンケートをご回答いただいた方に資料URLをお送りします。ご協力をお願いします。
]

### 配布予定資料「アプリにプッシュ通知を組み込もう！」
.size_small_9[
ニフクラ mobile backend を使うことで、<br>**既存Monacaアプリにも簡単にプッシュ通知機能を導入可能** です！
]

.center[<img src="document-img/push_image.png" alt="push_image" width="300px">]

---
layout: true
class: center, middle, inverse_sub
---
.center[
## ご清聴ありがとうございました！
]
