# 開発フロー

← [README に戻る](../README.md#-開発フロー)

```mermaid
flowchart TB
    subgraph 1. 要件定義
        A1[/project:requirements] --> A2[ヒアリング] --> A3[docs/PRD.md 作成]
    end
    
    subgraph 2. 設計
        B1[/project:design] --> B2[PRD.md 確認] --> B3[docs/DESIGN.md 作成]
        B2 --> B4[docs/SCREEN.md 作成]
    end
    
    subgraph 3. API設計
        C1[/project:api] --> C2[DESIGN.md 確認] --> C3[docs/openapi.yaml 作成]
    end
    
    subgraph 4. 実装
        D1[/project:implement] --> D2{src/ 存在?}
        D2 -->|No| D3[環境構築] --> D4[GitHub Issue 取得]
        D2 -->|Yes| D4
        D4 --> D5[コード実装] --> D6[Issue 更新・クローズ]
    end
    
    subgraph 5. 繰り返し
        E1[/project:continue] --> E2[Open Issue 確認] --> E3[次のタスク実装]
    end
    
    A3 --> B1
    B3 --> C1
    B4 --> C1
    C3 --> D1
    D6 --> E1
    E3 --> D5
```

## フェーズ詳細

### 1. 要件定義
- **コマンド**: `/project:requirements`
- **処理内容**: ヒアリング → 要件整理
- **成果物**: docs/PRD.md

### 2. 設計
- **コマンド**: `/project:design`
- **処理内容**: PRD.md 確認 → 全体設計・画面設計
- **成果物**: docs/DESIGN.md, docs/SCREEN.md

### 3. API設計
- **コマンド**: `/project:api`
- **処理内容**: DESIGN.md 確認 → API定義
- **成果物**: docs/openapi.yaml

### 4. 実装
- **コマンド**: `/project:implement`
- **処理内容**: 
  - src/ 無ければ環境構築（create-next-app）
  - GitHub Issue からタスク取得
  - コード実装
  - Storybook 追加（UIの場合）
  - テスト作成
  - Issue 更新・クローズ
- **成果物**: src/, Issue更新

### 5. 繰り返し
- **コマンド**: `/project:continue`
- **処理内容**: Open な Issue 確認 → 次のタスク実装

## その他のコマンド

| コマンド | 説明 |
|----------|------|
| `/project:status` | 進捗状況を確認 |
| `/project:task` | 新しいタスクを作成 |

---

← [README に戻る](../README.md#-開発フロー)
