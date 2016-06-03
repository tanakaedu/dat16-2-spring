# デジタルアーツ東京　2016年度2年生用リポジトリ

# 学校のAndroidのドライバーインストール
- コンピューター>ネットワーク>LANDISK-A601>disk>2016年>学生用フォルダー>ゲームプログラム２年>AndroidUSB を開く
- 手順.txtを開いて、HTC用のアプリであるKiesSetupと、TabletSの設定を行う



# Unity Remote4のapkファイルを入手するには・・・
- 該当アプリがインストール済みのAndroid端末で、ESエクスプローラーを起動
- アプリボタンを押す
- apkを取り出したいアプリを長押して、ダウンロードを選択
- USBでPCと接続して、Backups>appsフォルダー内から取り出す

# 6回目()
- Unity マルチプレイヤーのドキュメント  http://forum.unity3d.com/threads/feedback-needed-new-doc-for-getting-started-with-unity-multiplayer.368900/

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
  

