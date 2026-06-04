# CODECHART for Vercel

CODE CHART の歩み値・板・チャート検証ツールを Vercel 静的ホスティング向けに切り出した版です。

## 動作

- ブラウザ上で CSV / JSON を選択して読み込みます。
- `main_Ticks.json`、`main_Masters.json`、`main_ItaRows.json` の複数ファイル読み込みに対応しています。
- 複数銘柄 JSON 読み込み時は `/` で銘柄検索、`Space` / `Shift + Space` で銘柄移動できます。
- データはブラウザ内で処理します。サーバーへアップロードする処理はありません。

## ローカル確認

```bash
npm run check
python3 -m http.server 8766
```

ブラウザで `http://127.0.0.1:8766/` を開きます。

## Vercel

Vercel 側ではビルドコマンドなし、出力ディレクトリはプロジェクトルートです。

CLI で直接デプロイする場合:

```bash
npx vercel --prod
```
