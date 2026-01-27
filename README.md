# 珈琲焙煎記録 PWA

スマホで使える焙煎ログ管理アプリです。オフラインでも動作し、データはデバイス内に保存されます。

## 機能

- ✅ 焙煎記録の保存・閲覧
- ✅ タイマー機能（1ハゼ、2ハゼ、終了時間の記録）
- ✅ DTR（Development Time Ratio）自動計算
- ✅ データエクスポート（JSON/CSV）
- ✅ データインポート（JSON）
- ✅ オフライン動作
- ✅ PWAインストール対応（ホーム画面に追加可能）

## インストール方法

### Android（Chrome）

1. Chromeでアプリを開く
2. メニュー（⋮）→「アプリをインストール」をタップ
3. ホーム画面にアイコンが追加されます

### iPhone（Safari）

1. Safariでアプリを開く
2. 共有ボタン（□↑）をタップ
3. 「ホーム画面に追加」をタップ
4. ホーム画面にアイコンが追加されます

## デプロイ方法

### GitHub Pagesを使う場合

1. GitHubリポジトリを作成
2. 以下のファイルをアップロード：
   - `index.html`
   - `manifest.json`
   - `service-worker.js`
   - `icon-192.png`
   - `icon-512.png`
3. Settings → Pages → Source を `main` ブランチに設定
4. 生成されたURLにアクセス

### Netlifyを使う場合

1. [Netlify](https://www.netlify.com/)にアクセス
2. 「New site」→「Deploy manually」を選択
3. プロジェクトフォルダをドラッグ&ドロップ
4. 自動生成されたURLにアクセス

### ローカルでテストする場合

PWAはHTTPSが必要なため、ローカルHTTPサーバーで起動します：

```bash
# Python 3がインストールされている場合
python -m http.server 8000

# Node.jsがインストールされている場合
npx http-server -p 8000
```

その後、`http://localhost:8000`にアクセスしてください。

## データ管理

### エクスポート

- **JSONエクスポート**: データをJSON形式でダウンロード（他のデバイスで復元可能）
- **CSVエクスポート**: データをCSV形式でダウンロード（Excelで開ける）

### インポート

- JSONファイルをインポートすることで、別のデバイスや過去のバックアップからデータを復元できます

## 技術スタック

- HTML5
- JavaScript (Vanilla)
- Tailwind CSS (CDN)
- LocalStorage API
- Service Worker API
- Web App Manifest

## ライセンス

MIT License
