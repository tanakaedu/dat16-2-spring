# デジタルアーツ東京　2016年度2年生用リポジトリ

# 12回目(7/15)
## 先週のニュース続報
- 任天堂のWiiUや3DSの個人開発はイマイチでした。

## 夏休みの宿題
- 小作品を１本完成させる
  - ジャンル、使用言語は自由
    - Visual C# / Unity / DirectX / Java / Scratch / [プログラミングの必要なし！簡単にスマホアプリが開発できるツール9選](https://freelance.levtech.jp/guide/detail/38/?utm_content=bufferf4992&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer)
- 夏休み明けに以下をフォルダーにまとめてLANDISKで提出
  - すぐに実行できるデータ一式
  - プログラムや画像、音声など、ビルドに必要なデータ一式
  - WordかPowerPointで作成した作品紹介
    - タイトル
    - 動作環境
    - 開発環境
    - 起動方法
    - 使い方
    - 利用目的
    - ビルド方法
    - 参考にした書籍やWebページがあれば、それらのリスト

## セットアップ作業
- Unityのチェック
  - guestでログイン
  - Unityを起動
  - Unityのバージョンが5.3.4かを確認。違う場合、インストール
  - [Edit]>[Preferences]>[External Tools]を開いて、エディターがMono Developになっていることを確認。違う場合、Monoに変更
- データのコピー
  - [ドキュメント]フォルダーに、[unitydatas]というフォルダーを作成
  - LAN DISKの指定のフォルダーを、上記のフォルダー内にコピー
以上、全てのPCに実施

## 実習
- 各自のPCで、配布資料に従って、作業を進めて、多人数プレイアプリを完成させる
- 上記ができたら、別の資料とデータを使って、秋葉原の多人数プレイを完成させる
- 上記で時間が余ったら、Unityちゃんの移動(とくにジャンプ)の動作改善を試みる


---

# 11回目(7/8)
- https://developer.nintendo.com/
- 体験入学用の資料の修正の仕上げ
  - 秋葉原のネットワークに置いて、通信にマッチメイキングサーバーを利用するように書き換える

# 10回目(7/1)
- 体験入学用の資料の検証
  - ネットワークから「\\LANDISK-A601\disk\2016年\学生用フォルダー\ゲームプログラム２年」フォルダーを開く
  - 「体験入学素材」フォルダーをコピーして、ドキュメントフォルダーなどに貼り付ける
  - 「体験入学素材」フォルダー内の「01Unityゲーム開発_印刷_15夏.pdf」を開いて、指示通り作業
    - 途中で出てくる「指定の場所の指定のファイル」は、上記フォルダー内の「akihabara-dat15sumnet.unitypackage」のこと
  - 上記のPDFが終わったら「03UNet開発_印刷_15夏.pdf」を続けて行う
  - 途中で作業できない部分が出てきたら報告
- 体験講義用のデータの更新
  - 不要なデータや、更新が必要なものに対応する
  - Visual Studio用の設定は不要
- Unity3dのアセットバンドル調査
  - 目的1：別々のプロジェクトで作成されたショットを、ほかのプレイヤーと共有できるか？
  - 目的2：プレイヤーの共有か可能か？
    - プレイヤープレハブはゲームで1つのみなので、これを個別に設定するのは不可
    - 各自が作成したプレイヤーをアセットバンドルで共有して、プレイヤーの子要素として見た目を共有できるか？
    - 挙動はローカルで制御した位置などをデータとして同期するだけなので、現状でも問題はない
  - Unity公式のマニュアル: http://docs.unity3d.com/ja/current/Manual/BuildingAssetBundles.html


# 9回目(6/24)
- Unity5.3.4でUnity公式のマッチメイキングサービスについて調査する
  - 利用の条件(費用、接続制限)
    - https://unity3d.com/jp/services/multiplayer
    - 開発中は、20CCU(同時に20名まで接続)までの制限で無料で利用可能
    - 公開する場合はProfessionalライセンスが必要で、さらにアクセス量に応じた費用が発生
    - 参考URL : [FreelyApps UnityMultiplayerの料金について](http://freelyapps.blog.jp/archives/1054487065.html)
  - 使い方は[こちら](https://github.com/tanakaedu/dat162-haru/wiki/9%E5%9B%9E%E7%9B%AEUnet%E3%83%9E%E3%83%83%E3%83%81%E3%83%A1%E3%82%A4%E3%82%AD%E3%83%B3%E3%82%B0%E3%82%B5%E3%83%BC%E3%83%93%E3%82%B9)
- Unity5.3でのシーン切り替え
  - Application.LoadLevel()→SceneManager.LoadScene()
  - シーン間の変数の保持を行う方法(ハイスコアをゲーム内で常に保持しておくなどに利用)
    - SceneManagerにそのための機能はないので、今まで通りパラメータを持ち越すためのクラスを作成してstaticプロパティで対応
- 体験入学用の資料の検証
  - ネットワークから「\\LANDISK-A601\disk\2016年\学生用フォルダー\ゲームプログラム２年」フォルダーを開く
  - 「体験入学素材」フォルダーをコピーして、ドキュメントフォルダーなどに貼り付ける
  - 「体験入学素材」フォルダー内の「01Unityゲーム開発_印刷_15夏.pdf」を開いて、指示通り作業
    - 途中で出てくる「指定の場所の指定のファイル」は、上記フォルダー内の「akihabara-dat15sumnet.unitypackage」のこと
  - 上記のPDFが終わったら「03UNet開発_印刷_15夏.pdf」を続けて行う
  - 途中で作業できない部分が出てきたら報告


# 8回目(6/17)
- Unity5.3.4でマルチプレイヤーを動かす方法をまとめる
  - [Unity公式ドキュメント LocalDiscoveryで、LAN内のほかのPCに接続する](http://docs.unity3d.com/ja/current/Manual/UNetDiscovery.html)
  - [Unity公式ドキュメント 0からマルチプレイヤープロジェクトをセットアップする](http://docs.unity3d.com/ja/current/Manual/UNetSetup.html)
  - [Unity公式ドキュメント](http://docs.unity3d.com/ja/current/Manual/UNetOverview.html)
  - http://forum.unity3d.com/threads/feedback-needed-new-doc-for-getting-started-with-unity-multiplayer.368900/


# 7回目(6/10)
- Androidの操作をUnityで確認
- Android向けビルドを試す
- 以前作成した光らせるデモなどを、Android向けにビルドして動きを確認する
- シナリオエンジン [ジョーカースクリプト](http://jokerscript.jp/) をAndroidでビルド


# 6回目(6/3)
- Androidの接続

## Unity Remote4のapkファイルを入手するには・・・
- 該当アプリがインストール済みのAndroid端末で、ESエクスプローラーを起動
- アプリボタンを押す
- apkを取り出したいアプリを長押して、ダウンロードを選択
- USBでPCと接続して、Backups>appsフォルダー内から取り出す


# 5回目(5/27)
- [日本科学未来館 企画展「GAME ON」特別イベント「ゲームってなんでプログラミング？」](http://www.miraikan.jst.go.jp/event/1604141719829.html)
- Unityでのテスト
  - http://qiita.com/RyotaMurohoshi/items/9ef76d76de691a98975a
  - MonoDevelopではエラーがでる可能性がある
    - Unityの[Window]>[Editor Tests Runner]でテストウィンドウを開いてテストする
    - UnityTestToolsアセットはインポートしなくても単体テストが可能
- NUnitの利用
  - https://github.com/nunit/nunit-csharp-samples
- AndroidのUnityからの書き出し

## Androidのテストとビルド
- Unity5.3.4を起動
- 新しいプロジ作成。AndroidTestなどの名前にする
- Cubeを作成
- Scaleを、x=10、y=1、z=10ぐらいにして、画面下の方に配置
- Sphereを作成
- [Add Component]>[Physics]>[Rigidbody]を追加
- 以上で、いったん動かして、ボールが落下するのを確認

### おまけ
- Materialを作って、ボールに色をつける
- PhysicMaterialを作って、ボールが跳ね返るようにしてみる
  - Bounceness を0.8などにして、弾性を上げる
  - Bounce Combine をMaximum

### 床の設定
- Cubuに、[Add Component]>[Physic]>[Rigidbody]
- RigidbodyのUse Gravityをはずす
- Is Kinematicにチェック(物理挙動を無視して動かすので)
- [Add Component]>[New Script]で、Sumahoという名前のC#スクリプトを作成
- [Update]関数を以下のように編集
```
	void Update () {
		Vector3 ac = Input.acceleration;
		Debug.Log (ac);
	}
```
- 上書き保存して、Unityに戻る

### スマートフォンにUnityPlayerをインストール
- Playストアを起動
- Unity Remote4を検索してインストール

### テスト
- Unityの[Edit]>[Project Settings]>[Editor]メニューを選択
- [Device]欄を、[Any Android Device]に変更
- Unity Remoteを起動してから、PCに接続して、Unityを実行

### 接続できないとき
- AndroidのUnity Remoteを閉じ、Unityを閉じ、USBケーブルをはずす
- USBケーブルで、PCとAndroidを接続
- USBデバッグモードになっていることを確認
- AndroidでUnity Remoteを起動
- PCで、Unityを起動
- UnityでPlay

以上で動いた。


# 4回目
- インストール作業
  - [インストール手順2016](http://am1tanaka.hatenablog.com/entry/2016/04/05/230542)
    - GitHub Desktop
    - Atom
    - Firefox
    - Android SDK


# 3回目
## 情報
- [5/24 自作キャラのゲーム作成を無料体験【Unity/iClone/Maya】](https://kenjin.unity3d.jp/events/show/365)
- [Unity 5.4 パブリックベータ版](http://blogs.unity3d.com/jp/2016/03/15/enhanced-visuals-better-performance-and-more-the-unity-5-4-public-beta-is-ready/)
- [Unityのイベント関数の実行順](http://docs.unity3d.com/ja/current/Manual/ExecutionOrder.html)
- [Unity 軽量なビルドサイズでWebGL用に出力する](https://medium.com/@verochan/how-to-export-your-unity-3d-project-to-webgl-and-keep-a-reasonable-build-size-8f6a719e7c18#.9en0lp9nz)
- [日本科学未来館 GAME ON](http://www.fujitv.co.jp/events/gameon/)

## 今日のテーマ
- スマホ対応 or ユニットテスト

# 今年度の方針
- 簡単な解説をしたあとは、資料をもとに各自作業を進める
- 各回、学習内容は本リポジトリで分かるようにするので、欠席した時は各自でフォローすること
- 学習成果は常に各自のGitHubに反映させて、毎週、何をしたかが講師に分かるようにする

## テーマ
以下のようなことを扱う予定。各自、自分のGitHubに、学習の成果が出るように工夫すること。
- Unity:表現力の向上
  - [テラシュールブログ Unity 5 で画面を綺麗にするライティングに挑戦してみるメモ](http://tsubakit1.hateblo.jp/entry/2015/03/10/030139)
  - [テラシュールブログ Unity 5 で「光モノ系」を表現するあれこれ](http://tsubakit1.hateblo.jp/entry/2015/06/24/055130)
- Unity:スマートフォン用作品の開発
- Unity:マルチプレイヤー
- Unity:ユニットテスト/統合テスト
- Unity サーティフィケーションプログラム:認定デベロッパーについて調査
- TensorFlow:チュートリアルでAIを学ぶ
- サーバー:Heroku + Pythonなど

# 参考URL
## 就職関連
- [paiza ITエンジニア・プログラマを目指す就活で押さえるべきポイント](http://paiza.jp/advice/student_advice)
- [paiza新卒](http://paiza.jp/student)
- [Actcat 採用情報](http://www.actcat.co.jp/jobs)

## ゲーム開発コミュニティ
- [Pico Pico Cafe](http://www.picopicocafe.com/)
- 東京インディーズ
  - [HP](http://www.tokyoindies.com/)
  - [Facebook](https://www.facebook.com/events/264884527192215/)
  - [デジゲー博2016](http://digigame-expo.org/)
- [Unity県人会議イベント一覧](https://kenjin.unity3d.jp/events)

## Unity関連
- [Unity5.4β版](http://blogs.unity3d.com/jp/2016/03/15/enhanced-visuals-better-performance-and-more-the-unity-5-4-public-beta-is-ready/)

## AI関連
- [Google TensorFlow](http://tensorflow.org/)
  - Googleがオープンソースで公開した機械学習システム
  - データの流れを表す図(Data Flow Graph)を使って、計算方法を組み立てられる
  - ある入力を、データフローグラフに従って評価
  - 評価した結果が目的の値(小さい値とか、大きい値とか)になるように、計算式内のパラメータを調整する
  - 上記を繰り返すことで、入力に対して、良さそうな結果を出力する
  - 機械学習の例
    - [TensorFlow公式 初心者のためのMNISTの学習](http://tensorflow.org/tutorials/mnist/beginners/index.md)
    - [t-hiroyoshi Caffeで手書き数字(MNIST)の認識学習をする](http://qiita.com/t-hiroyoshi/items/2bf473fd06c352d97579)
- [ITmedia Microsoft ProjectAIX](http://www.itmedia.co.jp/news/articles/1603/15/news082.html)
  - マインクラフトを採用する人工知能訓練プロジェクト
  - 2016年夏にオープンソースで公開予定
  

