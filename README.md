# ATFEditor

> **寫 Markdown 不用再開瀏覽器。開檔案不用再找 IDE。**
>
> 原生 macOS 純文字與 Markdown 編輯器——編輯在左、預覽在右，一個視窗搞定。

![ATFEditor 截圖](https://via.placeholder.com/800x500?text=ATFEditor+Screenshot)

---

## 你不是這樣寫 Markdown 的嗎？

開 VS Code 寫內容 → 開瀏覽器看渲染 → 切回來繼續寫。**兩個視窗來回切，一天幾十次。**

或者拿到一個 `.md` 檔案，終端 `cat` 看了三分鐘 raw markup，才發現只是要看結果。

**ATFEditor 把這些都省了。**

一個視窗、不分心——左側編輯器寫 Markdown / 程式碼，右側 Sidecar 即時顯示渲染結果。從 Open File 到看到預覽，兩秒鐘。

---

## 你拿 ATFEditor 來做什麼

### 寫 Markdown，所見即所得

左寫右看，不用離開編輯器就知道標題層級對不對、表格有沒有歪、code block 有沒有漏反引號。

### 快速開檔，秒速預覽

Markdown、程式碼、JSON、HTML——拖進去或選開啟，自動選對的預覽模式。不用管檔案類型，只管打開。

### 順便看 Git diff

編輯的同時看一眼這支檔案改了什麼。行號旁邊直接標顏色：黃＝修改、綠＝新增、紅＝刪除。不用切到終端下 `git diff`。

### 不怕別人改同一份檔案

其他程式修改了檔案？ATFEditor 會偵測到並問你要不要重新載入。不會默默覆蓋你的編輯。

---

## 適用情境

| 你是在做這個的人嗎？ | ATFEditor 可以幫你 |
|----------------------|--------------------|
| 寫技術文件、部落格、README | Markdown 即時預覽，不用開瀏覽器 |
| 寫 Swift / Python / JS / Go 等程式碼 | 40+ 種語言語法高亮，簡潔編輯環境 |
| 需要快速翻看各種檔案 | 開檔自動判斷類型，Markdown → JSON → HTML 都行 |
| 用 Git 管理專案 | 內建 diff 檢視，行級增刪改一目瞭然 |

---

## 它跟其他編輯器有什麼不同？

| | ATFEditor | VS Code / Cursor | Typora | Bear |
|---|-----------|------------------|--------|------|
| **架構** | SwiftUI + AppKit 原生 | Electron | Electron | 原生 |
| **重量** | ~15 MB，開機瞬開 | 200-500 MB | ~150 MB | ~50 MB |
| **專注範圍** | 純文字 + Markdown | 全端 IDE | 純 Markdown | 筆記 |
| **預覽模式** | Markdown + HTML + JSON + diff | 靠 extensions | Markdown 為主 | 純文字 |
| **售價** | $7.99（買斷） | 免費 | 付費授權 | 訂閱制 |

**ATFEditor 不是 IDE。** 它不做編譯、不跑測試、不連 terminal。它只做一件事：**讓你快速開啟、編輯、預覽檔案**——而且做得超級原生、超級快。

---

## 預覽模式一覽

| 類別 | 支援格式 |
|------|---------|
| **程式碼** | Swift, Python, JS, TS, Go, Rust, C/C++, Java, Ruby, Shell, YAML, JSON, HTML, CSS, SQL 等 40+ 語言 |
| **Markdown** | `.md` 完整渲染（標題、表格、code block、圖片） |
| **純文字** | `.txt`, `.log` |
| **網頁** | 本機 `.html` 內嵌預覽 |
| **結構化資料** | JSON, XML, CSV, PLIST 格式化顯示 |
| **Git Diff** | 彩色 unified diff + 行號色塊 |

---

## 下載

從 [Releases](https://github.com/arikechen/ATFEditor/releases) 下載最新的 `.dmg`。

---

## 系統需求

- macOS 14.0 (Sonoma) 或更新
- Apple Silicon / Intel

---

## 快速建置

```sh
xcodegen generate
xcodebuild -project ATFEditor.xcodeproj -scheme ATFEditor build
open ATFEditor.xcodeproj
```

> `project.yml` 是唯一的 Xcode 組態來源，**不要**手動編輯 `.xcodeproj`。

### 依賴套件

| 套件 | 用途 |
|------|------|
| [CodeEditSourceEditor](https://github.com/CodeEditApp/CodeEditSourceEditor) | 程式碼編輯器核心 |
| [CodeEditLanguages](https://github.com/CodeEditApp/CodeEditLanguages) | Tree-sitter 語法偵測 |
| [swift-markdown-ui](https://github.com/gonzalezreal/swift-markdown-ui) | Markdown 渲染引擎 |

---

## 開發藍圖

- [x] Markdown 即時預覽
- [x] 程式碼語法高亮與編輯
- [x] 多格式檔案預覽（Markdown、HTML、JSON）
- [x] Git diff 與狀態
- [x] 外部檔案變更偵測
- [x] 彈出視窗
- [ ] Markdown 格式化工具列
- [ ] 編輯區 / 預覽區同步滾動
- [ ] Mermaid 圖表
- [ ] LaTeX 數學公式
- [ ] Frontmatter 支援
- [ ] 主題市集

---

## License

See [LICENSE.txt](LICENSE.txt) for details.
