# ワールドウェザー

React製の天気予報アプリケーションです。都市名を入力すると、リアルタイムの天気情報を取得して表示します。

## 機能

- 世界中の都市の現在の天気情報を取得
- 気温（摂氏）の表示
- 天気の状態（晴れ、曇り、雨など）の表示
- 天気アイコンの表示
- 国名と都市名の表示

## 使用技術

- **React** - UIライブラリ
- **Axios** - HTTP通信
- **WeatherAPI.com** - 天気情報API

## プロジェクト構成

```
react-weather-app/
├── App.js                  # メインアプリケーションコンポーネント
├── App.css                 # アプリケーションスタイル
├── index.js                # エントリーポイント
├── background-image.jpg    # 背景画像
└── components/
    ├── Title.js           # タイトルコンポーネント
    ├── Form.js            # 都市入力フォームコンポーネント
    └── Results.js         # 天気情報表示コンポーネント
```

## セットアップ

### 必要要件

- Node.js (v12以上推奨)
- npm または yarn

### インストール

1. リポジトリをクローン

```bash
git clone https://github.com/taiyo8911/react-weather-app.git
cd react-weather-app
```

2. 依存パッケージをインストール

```bash
npm install
```

必要なパッケージ:
- react
- react-dom
- axios

### API キーの設定

このアプリケーションは[WeatherAPI.com](https://www.weatherapi.com/)を使用しています。

1. [WeatherAPI.com](https://www.weatherapi.com/)で無料のAPIキーを取得
2. `App.js`の19行目にあるAPIキーを自分のキーに置き換えてください

```javascript
axios.get(`https://api.weatherapi.com/v1/current.json?key=YOUR_API_KEY&q=${city}&aqi=no`)
```

## 実行方法

開発サーバーを起動:

```bash
npm start
```

ブラウザで [http://localhost:3000](http://localhost:3000) を開いてアプリケーションを確認できます。

## 使い方

1. 入力フォームに都市名を入力（日本語または英語）
   - 例: Tokyo, London, New York, 東京
2. 「Get Weather」ボタンをクリック
3. 現在の天気情報が表示されます

## コンポーネント詳細

### App.js
- メインコンポーネント
- 状態管理（都市名、天気情報）
- WeatherAPI.comからのデータ取得

### components/Title.js
- アプリケーションタイトル「ワールドウェザー」を表示

### components/Form.js
- 都市名入力フォーム
- ユーザー入力を受け取り、親コンポーネントに渡す

### components/Results.js
- 取得した天気情報を表示
- 都市名、国名、気温、天気状態、アイコンを表示

## ライセンス

このプロジェクトはオープンソースです。

## 作成者

taiyo8911

---

**Note**: 本番環境で使用する場合は、APIキーを環境変数として管理することを推奨します。
