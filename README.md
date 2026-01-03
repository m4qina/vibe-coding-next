# Next.js バイブコーディング テンプレート

## 🎯 これは何？

Claude Code でバイブコーディングするためのプロジェクトテンプレートです。

AIに指示を出すだけで、要件定義から実装まで一貫したフォーマットで開発を進められます。

## 🛠 技術スタック

| カテゴリ | 技術 |
|----------|------|
| フレームワーク | Next.js (App Router) |
| 言語 | TypeScript |
| スタイリング | Tailwind CSS |
| Linter / Formatter | ESLint / Prettier |
| パッケージ管理 | npm |
| ホスティング | Vercel |
| CI/CD | GitHub Actions |

## 📦 テンプレートに含まれるもの

```
├── docs/           # ドキュメントテンプレート
├── .github/        # CI/CD 設定
├── .claude/        # Claude Code カスタムコマンド
├── CLAUDE.md       # AI向け指示書
└── README.md       # このファイル
```

※ `src/` はAIが初回実装時に自動生成します

## 🚀 はじめかた

1. このテンプレートから新規リポジトリを作成
2. clone して Claude Code で開く
3. `/project:requirements` で要件定義
4. `/project:design` で設計
5. `/project:api` でAPI設計（必要に応じて）
6. `/project:implement` で実装スタート

## 🔄 開発フロー

👉 [開発フロー図](./docs/DEVELOPMENT_FLOW.md)

| # | フェーズ | コマンド | 成果物 |
|---|----------|----------|--------|
| 1 | 要件定義 | `/project:requirements` | docs/PRD.md |
| 2 | 設計 | `/project:design` | docs/DESIGN.md, SCREEN.md |
| 3 | API設計 | `/project:api` | docs/openapi.yaml |
| 4 | 実装 | `/project:implement` | src/, Issue更新 |
| 5 | 繰り返し | `/project:continue` | - |

## 💬 コマンド一覧

Claude Code で以下のスラッシュコマンドが使用可能です：

| コマンド | 説明 | 成果物 |
|----------|------|--------|
| `/project:requirements` | 要件定義を行う | docs/PRD.md |
| `/project:design` | 設計を行う | docs/DESIGN.md, SCREEN.md |
| `/project:api` | API設計を行う | docs/openapi.yaml |
| `/project:implement` | 実装を行う | src/, Issue更新 |
| `/project:continue` | 前回の続きから再開 | - |
| `/project:status` | 進捗状況を確認 | - |
| `/project:task` | 新しいタスクを作成 | GitHub Issue |

## 📄 ドキュメント構成

| ファイル | 内容 | 作成タイミング |
|----------|------|---------------|
| docs/PRD.md | 要件定義書 | `/project:requirements` |
| docs/DESIGN.md | 設計書 | `/project:design` |
| docs/SCREEN.md | 画面設計 | `/project:design` |
| docs/openapi.yaml | API設計（OpenAPI 3.0） | `/project:api` |
| GitHub Issues | タスク・進捗管理 | 随時更新 |

### docs/PRD.md（要件定義書）
- プロジェクト概要・背景
- ターゲットユーザー
- 機能一覧（MVP / 将来）
- 非機能要件

### docs/DESIGN.md（設計書）
- 技術スタック
- ディレクトリ構成
- 状態管理方針
- 主要コンポーネント設計

### docs/SCREEN.md（画面設計）
- 画面一覧
- 画面遷移図
- 各画面のワイヤーフレーム・要素

### docs/openapi.yaml（API設計）
- OpenAPI 3.0 形式
- エンドポイント定義
- リクエスト / レスポンススキーマ
- Swagger UI で確認可能

### GitHub Issues（タスク・進捗管理）
- タスクの作成・管理
- 進捗の記録
- ラベルで分類（feature / bug / docs など）

## ⚙️ 事前準備

このテンプレートは GitHub MCP を使ってタスク・進捗管理を行います。

👉 [GitHub MCP 設定ガイド](./docs/SETUP_GITHUB_MCP.md)

## 📝 ライセンス

MIT
