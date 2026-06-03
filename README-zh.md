# ATFEditor

> **写 Markdown 不用再开浏览器。开文件不用再找 IDE。**
>
> 原生 macOS 纯文本与 Markdown 编辑器——编辑在左、预览在右，一个窗口搞定。

![ATFEditor 截图](https://via.placeholder.com/800x500?text=ATFEditor+Screenshot)

---

## 你不是这样写 Markdown 的吗？

开 VS Code 写内容 → 开浏览器看渲染 → 切回来继续写。**两个窗口来回切，一天几十次。**

或者拿到一个 `.md` 文件，终端 `cat` 看了三分钟 raw markup，才发现只是要看结果。

**ATFEditor 把这些都省了。**

一个窗口、不分心——左侧编辑器写 Markdown / 代码，右侧 Sidecar 即时显示渲染结果。从 Open File 到看到预览，两秒钟。

---

## 你用 ATFEditor 来做什么

### 写 Markdown，所见即所得

左写右看，不用离开编辑器就知道标题层级对不对、表格有没有歪、code block 有没有漏反引号。

### 快速开档，秒速预览

Markdown、代码、JSON、HTML——拖进去或选开启，自动选对预览模式。不用管文件类型，只管打开。

### 顺便看 Git diff

编辑的同时看一眼这个文件改了什么。行号旁边直接标颜色：黄＝修改、绿＝新增、红＝删除。不用切到终端下 `git diff`。

### 不怕别人改同一份文件

其他程序修改了文件？ATFEditor 会检测到并问你要不要重新载入。不会默默覆盖你的编辑。

---

## 适用情境

| 你是在做这个的人吗？ | ATFEditor 可以帮你 |
|----------------------|--------------------|
| 写技术文档、博客、README | Markdown 即时预览，不用开浏览器 |
| 写 Swift / Python / JS / Go 等代码 | 40+ 种语言语法高亮，简洁编辑环境 |
| 需要快速翻看各种文件 | 开档自动判断类型，Markdown → JSON → HTML 都行 |
| 用 Git 管理项目 | 内置 diff 检视，行级增删改一目了然 |

---

## 它跟其他编辑器有什么不同？

| | ATFEditor | VS Code / Cursor | Typora | Bear |
|---|-----------|------------------|--------|------|
| **架构** | SwiftUI + AppKit 原生 | Electron | Electron | 原生 |
| **重量** | ~15 MB，开机瞬开 | 200-500 MB | ~150 MB | ~50 MB |
| **专注范围** | 纯文本 + Markdown | 全端 IDE | 纯 Markdown | 笔记 |
| **预览模式** | Markdown + HTML + JSON + diff | 靠 extensions | Markdown 为主 | 纯文本 |
| **Git diff** | 内置，行级标记 | 内置 | 无 | 无 |
| **售价** | $7.99（买断） | 免费 | 付费授权 | 订阅制 |

**ATFEditor 不是 IDE。** 它不做编译、不跑测试、不连 terminal。它只做一件事：**让你快速打开、编辑、预览文件**——而且做得超级原生、超级快。

---

## 预览模式一览

| 类别 | 支持格式 |
|------|---------|
| **代码** | Swift, Python, JS, TS, Go, Rust, C/C++, Java, Ruby, Shell, YAML, JSON, HTML, CSS, SQL 等 40+ 语言 |
| **Markdown** | `.md` 完整渲染（标题、表格、code block、图片） |
| **纯文本** | `.txt`, `.log` |
| **网页** | 本地 `.html` 内嵌预览 |
| **结构化数据** | JSON, XML, CSV, PLIST 格式化显示 |
| **Git Diff** | 彩色 unified diff + 行号色块 |

---

## 下载

从 [Releases](https://github.com/arikechen/ATFEditor/releases) 下载最新的 `.dmg`。

---

## 系统需求

- macOS 14.0 (Sonoma) 或更新
- Apple Silicon / Intel

---

## 快速构建

```sh
xcodegen generate
xcodebuild -project ATFEditor.xcodeproj -scheme ATFEditor build
open ATFEditor.xcodeproj
```

> `project.yml` 是唯一的 Xcode 配置来源，**不要**手动编辑 `.xcodeproj`。

### 依赖套件

| 套件 | 用途 |
|------|------|
| [CodeEditSourceEditor](https://github.com/CodeEditApp/CodeEditSourceEditor) | 代码编辑器核心 |
| [CodeEditLanguages](https://github.com/CodeEditApp/CodeEditLanguages) | Tree-sitter 语法检测 |
| [swift-markdown-ui](https://github.com/gonzalezreal/swift-markdown-ui) | Markdown 渲染引擎 |

---

## 开发蓝图

- [x] Markdown 即时预览
- [x] 代码语法高亮与编辑
- [x] 多格式文件预览（Markdown、HTML、JSON）
- [x] Git diff 与状态
- [x] 外部文件变更检测
- [x] 弹出窗口
- [ ] Markdown 格式化工具栏
- [ ] 编辑区 / 预览区同步滚动
- [ ] Mermaid 图表
- [ ] LaTeX 数学公式
- [ ] Frontmatter 支持
- [ ] 主题市集

---

## 许可协议

详见 [LICENSE.txt](LICENSE.txt)。
