トップページURL：
https://humikiri.github.io/

## ブログ記事

Markdown記事を `src/content/blog/` に配置します。記事のスキーマはAstro 7の現行形式に合わせて `src/content.config.ts` で定義しています。

```md
---
title: "記事のタイトル"
pubDate: 2026-10-05
description: "記事の概要（省略可）"
updatedDate: 2026-10-06
tags:
  - 日記
  - 技術
draft: false
---

ここからMarkdown本文を書きます。
```

- `title`: 必須。記事タイトル。
- `pubDate`: 必須。公開日。`YYYY-MM-DD` 形式。
- `description`: 任意。記事の概要。
- `updatedDate`: 任意。更新日。
- `tags`: 任意。文字列の配列（省略時は空配列）。
- `draft`: 任意。下書きかどうか（省略時は `false`）。

開発サーバーは `npm run dev`、本番用ビルドは `npm run build` で実行します。
トップページには新着記事を最大5件表示し、ブログ全記事は `/blog/` で公開日の新しい順に一覧できます。
`main` ブランチへのPushで `.github/workflows/deploy.yml` が実行され、GitHub Pagesへ自動デプロイされます。
既存のガイドライン・レポートと画像は `public/pages/` に置いてあり、従来どおり `/pages/...` のURLで公開されます。
