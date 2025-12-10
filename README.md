# Zenn ブログ

[Zenn](https://zenn.dev/) の記事・本を管理するリポジトリです。

## ディレクトリ構成

```
.
├── articles/    # 記事
└── books/       # 本
```

## セットアップ

```bash
npm install
```

## 記事の作成

Zenn CLI を使用して記事を作成できます。

```bash
npx zenn new:article
```

## textlint

日本語の文章校正に textlint を使用しています。

### チェック実行

```bash
npm run lint
```

### 自動修正

```bash
npm run lint:fix
```

### 適用ルール

- **preset-ja-spacing** - 日本語のスペースルール
- **preset-ja-technical-writing** - 技術文書向けルール（文長制限、句読点の数など）

## CI

GitHub Actions で以下のタイミングで textlint が自動実行されます。

- `master` / `main` ブランチへのプッシュ時
- プルリクエスト作成・更新時
