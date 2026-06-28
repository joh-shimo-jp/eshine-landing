# eshine-landing

ESHINE の公開サイト（GitHub Pages）。

| ページ | ファイル | URL |
|---|---|---|
| LP | `index.html` | https://joh-shimo-jp.github.io/eshine-landing/ |
| Privacy Policy | `privacy-policy/index.html` | https://joh-shimo-jp.github.io/eshine-landing/privacy-policy/ |

## GitHub Pages

- ブランチ: `main`
- 公開元: リポジトリルート

## ブランチ運用

| ブランチ | 用途 |
|---|---|
| `main` | GitHub Pages のデプロイ対象。直接作業しない |
| `develop` | 開発の基準ブランチ |
| `feature/*` | 機能追加・修正用。develop から派生 |

### デプロイフロー

```
feature/* → develop → main（GitHub Pages が自動デプロイ）
```

main ブランチへのマージ後、GitHub Pages が自動的にサイトを更新します（通常 1〜2 分）。

## GitHub Pages 有効化（初回のみ）

1. [eshine-landing Settings → Pages](https://github.com/joh-shimo-jp/eshine-landing/settings/pages)
2. Source: Branch `main` / Folder `/ (root)` → Save
