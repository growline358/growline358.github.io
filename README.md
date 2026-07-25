# growline.github.io

Growlineが開発しているアプリの一覧・プライバシーポリシー・利用規約・お問い合わせをまとめる静的サイト。
ビルドツールなし、プレーンなHTML/CSSのみ。GitHub Pages（`main`ブランチのルート）で公開する想定。

## 構成

```
index.html                        トップページ（Appsギャラリー）
apps/<app-slug>/index.html        アプリ紹介ページ
apps/<app-slug>/privacy/index.html  プライバシーポリシー
apps/<app-slug>/terms/index.html    利用規約
contact/index.html                お問い合わせ
assets/css/style.css              共通スタイル
```

## 新しいアプリを追加する手順

1. `apps/<new-app-slug>/` を作り、`index.html` / `privacy/index.html` / `terms/index.html` を追加
   （既存の `apps/daily-plus/` をコピーして書き換えるのが早い）
2. トップページ（`index.html`）のAppsセクションに `.app-card` を1つ追加

## 注意: コンテンツの同期

各アプリのプライバシーポリシー・利用規約の本文は、アプリ側（例: Daily+の場合
`mobile/src/screens/Menu/content/termsContent.ts` / `privacyContent.ts`）が正データ。
このサイトのHTMLは手動でコピーしたものなので、**アプリ側の本文を変更したら、このサイトのHTMLも忘れずに更新する**こと。
