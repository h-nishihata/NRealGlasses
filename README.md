# NRealGlasses
## 環境
### ハードウェア
- Nreal Light glasses
- Sony Xperia
### ソフトウェア
- Unity 2019.2.13f1
- Android Studio 3.5.2
- Android SDK 9.0 (**デバイスのOSヴァージョンと合わせる．** Android StudioのSDK Managerでインストールされているか確認)
- [nrSDK for Unity](https://developer.nreal.ai/download) 1.2.1 (unity packageとしてプロジェクトファイルにインストール)
   
## ビルド・インストール手順
- Build SettingsでプラットフォームがAndroidになっているか，シーンが正しく選択されているか確認．
- Player Settings > Android settingsを以下のように設定し，ビルドする．  
  
| 項目 | 設定内容 |
| ------------- | ------------- |
| Default Orientation | Portrait |
| Auto Graphics API | false |
| Graphics APIs | OpenGLES3 |
| Company Name | **nreal（←重要．「com.nreal.helloMR」などのようにする．）** |
| Minimum API Level | Android 9.0(Pie) |
| Target API Level | Android 9.0(Pie) |
| Write Permission | External(SDCard) |
| Allow 'unsafe' code | true |
| Quality > V Sync Count | Don't Sync |  
  
- SDK ManagerでAndroid SDK Platform-Toolsをインストールし，[Android Debug Bridge](https://developer.android.com/studio/command-line/adb)(adb)が使える状態にする．
- PCとAndroidデバイスをUSB接続し，以下のコマンドを実行．  
`adb install [ビルドした.apkファイルの絶対パス]`
　　
## アプリ実行
- AndroidデバイスとARグラスをUSB接続する（Nreal Light Controllerが自動的に起動する）．インストールしたアプリを起動．
- 像が正しく表示されないときは，ARグラスの左のツルに付いている，輝度調整の「-」ボタンを長押しする．
