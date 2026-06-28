# eshine-landing

ESHINE の Landing Page および Privacy Policy を GitHub Pages で公開するための静的サイトです。

## 概要

- **目的**: App Store 審査に必要な Support URL / Privacy Policy URL の公開
- **構成**: 静的 HTML（外部フレームワーク不使用）
- **ホスティング**: GitHub Pages（main ブランチ・root）

## 公開 URL

| ページ | URL |
|---|---|
| Landing Page (LP) | https://joh-shimo-jp.github.io/eshine-landing/ |
| Privacy Policy | https://joh-shimo-jp.github.io/eshine-landing/privacy-policy/ |

## ファイル構成

```
eshine-landing/
├── index.html              # LP 本体
├── privacy-policy/
│   └── index.html          # Privacy Policy ページ
└── README.md               # このファイル
```

## GitHub Pages 有効化手順

1. GitHub リポジトリ（`joh-shimo-jp/eshine-landing`）を開く
2. **Settings** タブをクリック
3. 左サイドバーの **Pages** をクリック
4. **Source** セクションで以下を設定:
   - Branch: `main`
   - Folder: `/ (root)`
5. **Save** をクリック
6. 数分後、`https://joh-shimo-jp.github.io/eshine-landing/` でアクセス可能になる

## ブランチ運用

| ブランチ | 用途 |
|---|---|
| `main` | GitHub Pages のデプロイ対象。直接作業しない |
| `develop` | 開発の基準ブランチ |
| `feature/*` | 機能追加・修正用。develop から派生させる |

### デプロイフロー

```
feature/* → develop → main（GitHub Pages が自動デプロイ）
```

main ブランチへのマージ後、GitHub Pages が自動的にサイトを更新します（通常 1〜2 分）。
