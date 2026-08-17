# K-POS

Cloudflare Workers + D1で動作するPOSシステムです。

## 主な機能

- レジ・会計管理
- 商品マスタ管理
- スタッフ・権限管理
- 在庫管理
- 低在庫Webhook通知
- ガチャ商品管理
- 会計履歴
- ロール別表示設定
- ダークモード

## 動作環境

- Cloudflare Workers
- Cloudflare D1
- Cloudflare R2（画像を使用する場合）
- Node.js / Bun

## セットアップ

1. リポジトリをForkまたはClone
2. Cloudflare D1を作成
3. `wrangler.jsonc` にD1を設定
4. 必要に応じてR2を設定
5. Cloudflare Workersへデプロイ
6. SUPER_ADMINで初回ログイン

## D1設定

`wrangler.jsonc` のD1設定を使用するD1に変更します。

```json
"d1_databases": [
  {
    "binding": "DB",
    "database_name": "k-pos-db",
    "database_id": "YOUR_DATABASE_ID"
  }
]
