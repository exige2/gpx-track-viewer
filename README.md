# GPXトラックビューア

GPX・TCX・Garmin FIT（.fit / Garmin Connectのエクスポート.zip）の軌跡を地図上に表示し、アイコンが軌跡をなぞる再生と、距離・時間入りの動画書き出し（MP4 / WebM）ができるWebアプリです。

- ファイルはすべてブラウザ内で処理され、サーバーには送信されません
- PWA対応：スマホのホーム画面やPCにアプリとして追加できます
- ビルド不要の静的ファイルのみ（GitHub Pages / Netlify / Cloudflare Pages にそのまま置けます）

## 構成

| ファイル | 役割 |
| --- | --- |
| `index.html` | アプリ本体（Leaflet・JSZipはcdnjsから読み込み） |
| `manifest.webmanifest` | PWAの設定（名前・アイコン・ファイル関連付け） |
| `sw.js` | オフライン用キャッシュ（地図タイルはキャッシュしない） |
| `icon-*.png` ほか | アイコン |

## 地図

背景地図は地理院タイル、CARTO、OpenStreetMap を切り替えて使います。各提供元の利用規約に従い、出典表示を地図と書き出し動画に入れています。
