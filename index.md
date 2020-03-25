# Unityのインストール
## どのバージョンをインストールするか？
* 使いたいアセットをリストアップ/事前検証する
* 使いたいアセット、プロジェクトがバージョンに対応しているか
* 使いたいアセット同士でコンフリクトが生じていないか確認
* 特別な理由がないなら、LTS(長期サポート)バージョンを利用する

# Android開発環境の構築
*　省略

# プロジェクトの作成
## Organizationの適切な設定
* 一部の機能がPersonal Versionでは制限される
* Professional Versionでプロジェクトを作成する。背景色が黒いエディター。
![2](https://user-images.githubusercontent.com/20265353/77128588-003e2c00-6a94-11ea-9d5b-eacbf737fa5e.png)

# プロジェクトの共有
## プロジェクトのアップロード
* Collabアイコンからプロジェクトを登録。
4.png
* シーンに適当に変更を加え保存。例：カプセルをシーンに追加して保存
5.png
* 変更内容を記述してアップロード
## 他のアカウントからのプロジェクトの参照
6.png
* 最新の情報に更新する。
* Collaborate対象には太陽のマークが付いている。
* ↓アイコンでフォルダを指定してダウンロード。

# プロジェクトの初期設定 (Oculus Quest)
* [参考URL：フレームシンセンス](https://framesynthesis.jp/tech/unity/oculusquest/)

## Oculus Integrationのインポート

# 1.操作対象を主語<Target>
## ポインターによる入力
  * Oculus Integration - OVR Input Event Systemを利用。
  * UGUIも考慮
## コライダー侵入による入力
  * 手指、道具、飛び道具の侵入
  * ColliderEnter
## 視線による入力
  * ポインターとの同時操作を想定するため、Rayを飛ばす形で実装
  * Raycastを飛ばす側(Player)から受信する
  * UGUIも考慮
## 各入力を処理
* 入力は1か所で、Interfaceを介する
* 必要なInterfaceを実装したTargetPointer**をアタッチ
## 各入力に対するアクション
  * アニメーション

# 2.プレイヤー側オブジェクトを主語<Player>
  * プレイヤーの位置移動...CameraRigの親を動かす
  * プレイヤーの回転...CameraRigの親を動かす
## 拡張例 Actionを伴うもの（武器等）<Player.HandTools>
  * targetに送信
  * ボタンクリックやUI操作を受信
  
# 3.グラフィック関連-<Graphics>
## UI関連
  ### フェードアウト用UI
    * Oculus Integration - OVR Screen fadeを利用
  ### カメラの正面のUI
    * Z 0.5Mあたりに表示
  ### ワールドスペースに表示するUI
    * DoTweenによるアニメーション
    * Animaterによるアニメーション 
## 2DCG
 * SpritesController
## 2D動画
 * MoviesController
 * AVProVideoを使う
## 3DCG＜non-static＞
  * CGControlelr
  * 操作・アニメが介在するものと、固定の背景オブジェクトは別扱いで考える
## 3DCG＜static＞
  ### ファイル連携
  ### ライティング
  ### ベイク
  
  

  







 
----------
 

# 以下、MVCにとらわれずわかりやすいネーミングでサンプル実装。細分化＜単一責任原則＞
# TODO...設計は深入りすると時間無限なので現状のまとめ優先。

# 設計
## UMLクラス図
* https://www.slideshare.net/torisoup/unityzenject
* https://scrapbox.io/pf35301/SOLID%E5%8E%9F%E5%89%87
* http://unity-yuji.xyz/object-oriented-code-design-solid/
* https://qiita.com/Nekomasu/items/fe175fbb2cd4282a0e1c
* https://www.slideshare.net/torisoup/ss-148151761

* Prefab と NameSpaceの対応関係をつくりたい 
* 各NameSpaceの入出力は1か所にしたい

クラス図を基に、各機能の最低限をつくる。
MVCはいったん忘れる。
SOLID､
オープンクローズド原則
依存性逆転の原則

## 設計覚書
* インターフェースは、まず、単一単機能の原則の上になりたつ。インターフェースに複数の機能を望むと話がややこしくなる。












