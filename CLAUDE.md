# CLAUDE.md

このファイルは Claude Code がこのリポジトリで作業する際のガイダンスを提供します。

## プロジェクト概要

タスク管理ボードアプリケーション。

## デプロイ先

https://melmoon-lab.github.io/task-board/

`main` ブランチへのプッシュで GitHub Actions が自動ビルド・デプロイを実行する。

## 技術スタック

| 用途 | ライブラリ / ツール |
|------|-------------------|
| UI フレームワーク | React 18 |
| ビルドツール | Vite 5 |
| 言語 | JavaScript (JSX) |
| スタイル | CSS（コンポーネントごとの `.css` ファイル） |
| 状態管理 | React `useState` / `useEffect`（外部ライブラリなし） |
| 永続化 | `localStorage` |
| CI/CD | GitHub Actions |
| ホスティング | GitHub Pages |

## コンポーネント命名規約

- **ファイル名**: PascalCase（例: `App.jsx`, `TaskItem.jsx`）
- **コンポーネント関数名**: PascalCase でファイル名と一致させる
- **CSS ファイル名**: コンポーネント名と同名（例: `App.css`, `TaskItem.css`）
- **CSS クラス名**: kebab-case（例: `.task-item`, `.delete-btn`, `.input-row`）
- **ローカルストレージキー**: `task-board-<用途>` 形式（例: `task-board-tasks`）

## Git 運用ルール

- コードを変更するたびに、必ず GitHub へプッシュすること
- コミットメッセージは変更内容を端的に日本語で記述すること
- `main` ブランチへの直接プッシュは避け、機能単位でブランチを切ること
- プッシュ前には `git status` で変更内容を確認すること
- 力ずくの操作（`git push --force`、`git reset --hard` 等）は事前に確認を求めること

### コミット・プッシュの手順

```bash
git add <変更ファイル>
git commit -m "変更内容の説明"
git push origin <ブランチ名>
```

## 禁止事項

- `rm -rf` コマンドは絶対に実行しない
- `.env` ファイルを読んだり変更したりしない
- `package.json` の依存パッケージを無断で変更しない
- ファイルの削除・上書き前には必ず確認を求めること

## 一般ルール

- 作業完了後は変更をコミット・プッシュしてからタスク完了を報告すること
- ファイル名・フォルダ名の日付は「YYYYMMDD」形式にすること
