# ATFEditor

> **Markdown を書くのに、もうブラウザを開く必要はありません。**
> **ファイルを開くのに、もう IDE を探す必要はありません。**
>
> ネイティブ macOS プレーンテキスト & Markdown エディター——左に編集、右にプレビュー、1つのウィンドウで完結。

![ATFEditor スクリーンショット](https://via.placeholder.com/800x500?text=ATFEditor+Screenshot)

---

## あなたもこうやって Markdown を書いていませんか？

VS Code で書いて → ブラウザでレンダリングを確認して → 戻って書き続ける。**2つのウィンドウを行ったり来たり、1日に何十回も。**

あるいは `.md` ファイルを受け取って、ターミナルで `cat` しながら raw markup を3分も眺めて、やっと結果を確認する。

**ATFEditor はそんな無駄を全部省きます。**

1つのウィンドウ、集中力はそのまま——左側のエディターで Markdown / コードを書き、右側の Sidecar にレンダリング結果が即座に表示されます。ファイルを開いてからプレビュー表示まで、わずか2秒。

---

## ATFEditor でできること

### Markdown を書いて、そのまま確認（WYSIWYG）

左で書いて右で確認。エディターを離れずに見出しのレベル、テーブルの崩れ、コードブロックのバッククォート漏れが一目でわかります。

### ファイルを高速オープン、一瞬でプレビュー

Markdown、コード、JSON、HTML——ドラッグ＆ドロップまたは開くを選択するだけで、自動的に適切なプレビューモードを選択。ファイルの種類を気にする必要はありません。

### Git diff も一緒に確認

編集中にそのファイルの変更差分を確認できます。行番号横に色で表示：黄＝変更、緑＝追加、赤＝削除。ターミナルで `git diff` する必要はありません。

### 他の人が同じファイルを編集しても大丈夫

他のプログラムがファイルを変更したら ATFEditor が検出し、再読み込みするかどうかを確認します。あなたの編集が勝手に上書きされることはありません。

---

## こんなシーンに最適

| あなたはこんな人ですか？ | ATFEditor が助けます |
|--------------------------|---------------------|
| 技術文書、ブログ、README を書く人 | Markdown 即時プレビュー、ブラウザ不要 |
| Swift / Python / JS / Go などでコードを書く人 | 40+言語のシンタックスハイライト、ミニマルな編集環境 |
| 様々なファイルを素早く閲覧したい人 | ファイルを開くだけで自動判別、Markdown → JSON → HTML 全部OK |
| Git でプロジェクト管理している人 | 内蔵 diff ビューア、行単位の追加・削除・変更が一目瞭然 |

---

## 他のエディターとの違いは？

| | ATFEditor | VS Code / Cursor | Typora | Bear |
|---|-----------|------------------|--------|------|
| **アーキテクチャ** | SwiftUI + AppKit ネイティブ | Electron | Electron | ネイティブ |
| **サイズ** | ~15 MB、瞬時起動 | 200-500 MB | ~150 MB | ~50 MB |
| **フォーカス範囲** | プレーンテキスト + Markdown | フルスタック IDE | Markdown 特化 | ノート |
| **プレビューモード** | Markdown + HTML + JSON + diff | 拡張機能依存 | Markdown 中心 | プレーンテキスト |
| **Git diff** | 内蔵、行レベル表示 | 内蔵 | なし | なし |
| **価格** | $7.99（買い切り） | 無料 | 有料ライセンス | サブスクリプション |

**ATFEditor は IDE ではありません。** コンパイル、テスト実行、ターミナル接続はしません。ただ1つのことだけをやります：**ファイルを素早く開いて、編集して、プレビューする**——そしてそれを超ネイティブ、超高速で実現します。

---

## プレビューモード一覧

| カテゴリ | 対応フォーマット |
|----------|----------------|
| **コード** | Swift, Python, JS, TS, Go, Rust, C/C++, Java, Ruby, Shell, YAML, JSON, HTML, CSS, SQL など40+言語 |
| **Markdown** | `.md` 完全レンダリング（見出し、テーブル、コードブロック、画像） |
| **プレーンテキスト** | `.txt`, `.log` |
| **Webページ** | ローカル `.html` 埋め込みプレビュー |
| **構造化データ** | JSON, XML, CSV, PLIST フォーマット表示 |
| **Git Diff** | カラー unified diff + 行番号カラーブロック |

---

## ダウンロード

最新の `.dmg` は [Releases](https://github.com/arikechen/ATFEditor/releases) からダウンロードできます。

---

## システム要件

- macOS 14.0 (Sonoma) 以降
- Apple Silicon / Intel

---

## ビルド手順

```sh
xcodegen generate
xcodebuild -project ATFEditor.xcodeproj -scheme ATFEditor build
open ATFEditor.xcodeproj
```

> `project.yml` が唯一の Xcode 設定ソースです。`.xcodeproj` は**手動で編集しないでください**。

### 依存パッケージ

| パッケージ | 用途 |
|-----------|------|
| [CodeEditSourceEditor](https://github.com/CodeEditApp/CodeEditSourceEditor) | コードエディター核心 |
| [CodeEditLanguages](https://github.com/CodeEditApp/CodeEditLanguages) | Tree-sitter シンタックス検出 |
| [swift-markdown-ui](https://github.com/gonzalezreal/swift-markdown-ui) | Markdown レンダリングエンジン |

---

## 開発ロードマップ

- [x] Markdown 即時プレビュー
- [x] コードシンタックスハイライトと編集
- [x] マルチフォーマットプレビュー（Markdown、HTML、JSON）
- [x] Git diff とステータス表示
- [x] 外部ファイル変更検出
- [x] ポップオーバーウィンドウ
- [ ] Markdown フォーマットツールバー
- [ ] エディター / プレビュー 同期スクロール
- [ ] Mermaid 図表
- [ ] LaTeX 数式
- [ ] Frontmatter 対応
- [ ] テーママーケットプレイス

---

## ライセンス

詳細は [LICENSE.txt](LICENSE.txt) をご覧ください。
