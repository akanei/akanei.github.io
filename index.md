# Unityのインストール
## どのバージョンをインストールするか？
* 使いたいアセット、プロジェクトがバージョンに対応しているか
* 使いたいアセットをリストアップ
* 使いたいアセット同士でコンフリクトが生じていないか確認
*　特別な理由がないなら、LTS(長期サポート)バージョンを利用する

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

# Oculus Integrationのインポート

# 以下、MVCにとらわれずわかりやすいネーミングでサンプル実装。細分化＜単一責任原則＞

# ユーザー操作受付

# CG操作

# UI操作

# アニメーション操作

# TODO...設計は深入りすると時間無限なので現状のまとめ優先。

# 設計
* https://www.slideshare.net/torisoup/unityzenject
* https://scrapbox.io/pf35301/SOLID%E5%8E%9F%E5%89%87
* http://unity-yuji.xyz/object-oriented-code-design-solid/
* https://qiita.com/Nekomasu/items/fe175fbb2cd4282a0e1c
* https://www.slideshare.net/torisoup/ss-148151761
クラス図を基に、各機能の最低限をつくる。
MVCはいったん忘れる。
SOLID､
オープンクローズド原則
依存性逆転の原則

## 設計覚書
* インターフェースは、まず、単一単機能の原則の上になりたつ。インターフェースに複数の機能を望むと話がややこしくなる。












