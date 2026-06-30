# LP ワークフロー用キャプチャ素材

社長差し替え用。**ファイル名を変えずに上書き**すれば LP に反映されます（`index.html` 参照パス固定）。

## 推奨仕様（共通）

| 項目 | 推奨 |
|------|------|
| 形式 | PNG（透過不要） |
| 縦横比 | **9:19.5 前後**（iPhone 実機キャプチャ）または **9:16** |
| 幅 | **1170px 以上**（Retina 2x 想定） |
| 内容 | ステータスバー込みで OK。個人情報・API キーはマスク |

---

## 必須 5 枚（ワークフロー）

| # | 保存先 | ステップ | 撮る画面 | 備考 |
|---|--------|----------|----------|------|
| 1 | `01-image-gen.png` | **画像生成**（ESHINE 外） | 画像生成ツールの結果画面 | 例: ChatGPT / Gemini / Midjourney / 手描きスキャンなど。**元画像がどこから来たか**が伝わる 1 枚 |
| 2 | `02-eshine-load.png` | **ESHINE 読み込み** | `load_screen` — 画像選択・インポート直後 | ①の画像を読み込んだ状態が望ましい |
| 3 | `03-eshine-structure.png` | **構造化** | `parts_edit_screen` — パーツ切出・BBox 編集中 | ユーザーが構造化していることが分かる画面 |
| 4 | `04-eshine-export.png` | **.esvg 生成** | `convert_screen` — 変換完了 or プレビュー | `.esvg` 出力前後どちらでも可。ウォーターマーク除去トグル等が見えると親切 |
| 5 | `05-ai-import.png` | **AI 読み込み**（ESHINE 外） | AI / 制作側で `.esvg` を開く・読み込む画面 | **推奨サンプル**: 同梱の `LP_sample.esvg`（ウサギ 3 パーツ）を Cursor / NINJINE 等で読み込んだ瞬間をキャプチャ。**ファイル名・パーツ ID（rabbit / ear / hachimaki）・プレビュー**のいずれかが写っていると「構造化データの再利用」が伝わる |

### ステップ 5 — NINJINE 共有 FAB

| ファイル | 役割 |
|----------|------|
| `LP_sample_before.svg` | Before — ESHINE 出力 |
| `ninjine-share-fab.svg` | After — NINJINE 共有 FAB（**ファビコン同一** · LP 用コピー） |

NINJINE 正本: `ninjine/assets/eshine/icon/ninjine-app-icon-preview.svg`（`project_share_fab` = ファビコン流用 · DS-2026-06 確定）  
※ TOP Shell には FAB なし。Feed の `SeedFAB`（タネを書く）とは別物。

---

## 任意 1 枚（チケット説明）

| 保存先 | 用途 |
|--------|------|
| `../screenshots/ticket-store.png` | チケットストア（IAP）— 「Tickets」セクション用。審査用 1290×2796 でも LP 表示は CSS で縮小 |

---

## 撮影の流れ（おすすめ）

同じ題材（例: NINJINE スプラッシュ 1 本）で **①→②→③→④** を通し撮影すると LP のストーリーが一貫します。

```
[外部] 画像生成
    ↓ 同じ画像を
[ESHINE] 読み込み → 構造化 → .esvg 生成
    ↓ 出力ファイルを
[外部] AI / NINJINE 等で読み込み・制作
```

---

## 差し替え後

```bash
cd company/dev/apps/eshine-landing
open index.html   # ローカル確認
git add assets/workflow/
git commit -m "E-LP-02: update workflow screenshots"
```

`main` マージ後に GitHub Pages で公開確認（AC-5）。
