# iOSアプリの構成

## CocoaTouch
iOS アプリは Apple が整備する Cocoa Touch と呼ばれるフレームワーク群を利用して構成されています。Cocoa Touch の主要なフレームワークに Foundation と UIKit があります。
Foundation は文字列やコレクションといったプログラミング言語としての基本的なクラスから、並行処理やネットワーク処理のためのクラスまで、基本的なプログラミングの概念を提供するツールが揃っています。
UIKit はユーザインタフェース機能を提供するフレームワークです。ボタンやラベル、テーブルなどのiOS の GUIでアプリケーションを構成するための重要な機能のほとんどを担っています。

## View
Viewはユーザーに画像やテキストなどを画面の表示を行うコンポーネントで、UIViewとそのサブクラスにあたります。Viewは複数のサブViewを持つことができ、Viewを重なり合わせて一つの画面を作成します。
Viewのオブジェクトには、UIImageView（画像）、UITextView（テキスト）、UILable（ラベル）、UIButton（ボタン）などが提供されています。


## UIViewController
View ControllerはUIViewControllerのサブクラスで、自身が管理する一つのviewを持ちます。View Controllerは管理しているViewの更新と、そのviewで発生したイベントを受け取ってハンドリングを行っています。
アプリの画面は、1つ以上のView Controllerで構成されていて、UIWindowが持つRootViewControllerに、必要に応じて複数のView Controllerが重なり、もしくは遷移してアプリの機能を提供しています。

## まとめ
iOSアプリは原則的に一つのウィンドウ（UIWindow)を持ち、その上に必要なViewを積み重ねていきます。ViewにはViewControllerによって直接管理されるものと、そのsubviewとして表示されるだけのView Controllerとは対応しないViewがあります。

<img src="img.png" >