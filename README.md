# todo_app
## 機能
- ユーザー認証（ログイン/ログアウト）
- タスクの作成、表示、削除
- タスクの優先度と期限の管理
- タグによるタスク分類

## 環境
### フロントエンド
| 言語・フレームワーク  | バージョン | 備考 |
| --------------------- | ---------- | --------------- |
| Vue.js 3              |            | Composition API |
| Vuetify 3             |            |                 |
| TypeScript            |            |                 |
| Pinia                 |            | 状態管理         |

### バックエンド
| 言語・フレームワーク  | バージョン | 備考 |
| --------------------- | ---------- | --------------- |
| Django 4              |            |                 |
| Django REST Framework |            |                 |
| SQLite3               |            |                 |

### 起動手順

1. リポジトリのクローン

2. .env.exampleファイルを複製して名前を変更
<code>frontend/src/.env.example</code>→<code>.env</code>

3. Docker Desktop のインストール

https://www.docker.com/ja-jp/products/docker-desktop/

4. Docker Desktopを起動

5. コンテナの構築（ビルド）と起動

   ```bash
   docker compose up -d --build
   ```

6. データベースのマイグレーション

   ```bash
   docker compose exec backend python manage.py migrate
   ```

7. アプリケーションへのアクセス

- フロントエンド: http://localhost:5173
- バックエンド: http://localhost:8000


## ログインユーザー情報
データベースのマイグレーション実行時に作成
- Username: testuser
- Password: testpass123
