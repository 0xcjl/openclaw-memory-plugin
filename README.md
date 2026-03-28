<!--
  OpenClaw Memory System Plugin
  Default language: English (EN)
  To switch language: add ?lang=zh or ?lang=ja to the URL
  e.g.: github.com/0xcjl/openclaw-memory-plugin/blob/main/README.md?lang=zh
-->

<!--[if IE]><meta http-equiv="refresh" content="0;url=?lang=en"><![endif]-->
<!--[if lt IE 9]><![endif]-->

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>OpenClaw Memory System Plugin</title>
<style>
  :root {
    --bg: #0d1117;
    --text: #c9d1d9;
    --muted: #8b949e;
    --border: #30363d;
    --accent: #58a6ff;
    --tab-bg: #161b22;
    --tab-active: #21262d;
    --code-bg: #161b22;
  }
  @media (prefers-color-scheme: light) {
    :root {
      --bg: #ffffff;
      --text: #24292f;
      --muted: #57606a;
      --border: #d0d7de;
      --accent: #0969da;
      --tab-bg: #f6f8fa;
      --tab-active: #ffffff;
      --code-bg: #f6f8fa;
    }
  }
  * { box-sizing: border-box; }
  body {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif;
    background: var(--bg);
    color: var(--text);
    line-height: 1.6;
    max-width: 900px;
    margin: 0 auto;
    padding: 2rem 1.5rem;
  }
  a { color: var(--accent); text-decoration: none; }
  a:hover { text-decoration: underline; }
  h1, h2, h3 { border-bottom: 1px solid var(--border); padding-bottom: 0.3em; }
  h1 { font-size: 2em; margin-top: 0; }
  h2 { font-size: 1.5em; margin-top: 1.8em; }
  h3 { font-size: 1.2em; }
  code, pre {
    background: var(--code-bg);
    border: 1px solid var(--border);
    border-radius: 6px;
    font-size: 0.9em;
    font-family: "SFMono-Regular", Consolas, "Liberation Mono", Menlo, monospace;
  }
  pre { padding: 1em; overflow-x: auto; }
  :not(pre) > code { padding: 0.2em 0.4em; }
  pre code { border: none; padding: 0; background: none; }
  .lang-tabs {
    display: flex;
    gap: 0;
    margin: 1.5em 0 1em;
    border-bottom: 2px solid var(--border);
    list-style: none;
    padding: 0;
  }
  .lang-tabs li {
    margin: 0;
    padding: 0;
  }
  .lang-tabs button {
    background: var(--tab-bg);
    border: 1px solid var(--border);
    border-bottom: none;
    border-radius: 6px 6px 0 0;
    color: var(--muted);
    cursor: pointer;
    font-size: 0.9em;
    font-weight: 600;
    padding: 0.5em 1.2em;
    margin-right: 2px;
    transition: color 0.15s, background 0.15s;
  }
  .lang-tabs button:hover { color: var(--text); background: var(--tab-active); }
  .lang-tabs button.active {
    background: var(--tab-active);
    color: var(--accent);
    border-bottom: 2px solid var(--tab-active);
    margin-bottom: -2px;
  }
  .lang-section { display: none; }
  .lang-section.active { display: block; }
  .badge-row { display: flex; gap: 0.5em; flex-wrap: wrap; margin: 1em 0; }
  .badge {
    background: var(--tab-active);
    border: 1px solid var(--border);
    border-radius: 2em;
    color: var(--muted);
    font-size: 0.75em;
    font-weight: 600;
    padding: 0.2em 0.8em;
  }
  .install-cmd {
    background: var(--code-bg);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 1em 1.2em;
    font-family: monospace;
    overflow-x: auto;
    margin: 1em 0;
  }
  .feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
    gap: 1em;
    margin: 1em 0;
  }
  .feature-card {
    background: var(--tab-bg);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 1em;
  }
  .feature-card h3 { border: none; margin: 0 0 0.3em; font-size: 1em; }
  .feature-card p { margin: 0; color: var(--muted); font-size: 0.9em; }
  hr { border: none; border-top: 1px solid var(--border); margin: 2em 0; }
  table {
    border-collapse: collapse;
    width: 100%;
    margin: 1em 0;
    font-size: 0.9em;
  }
  th, td {
    border: 1px solid var(--border);
    padding: 0.5em 0.8em;
    text-align: left;
  }
  th { background: var(--tab-bg); }
  tr:nth-child(even) td { background: var(--code-bg); }
</style>
</head>
<body>

<ul class="lang-tabs" id="langTabs">
  <li><button class="active" data-lang="en">🇺🇸 English</button></li>
  <li><button data-lang="zh">🇨🇳 中文</button></li>
  <li><button data-lang="ja">🇯🇵 日本語</button></li>
</ul>

<!-- ─── English (default) ─────────────────────────────────────────── -->
<div class="lang-section active" id="sec-en">

# OpenClaw Memory System Plugin

<div class="badge-row">
  <span class="badge">openclaw</span>
  <span class="badge">openclaw-plugin</span>
  <span class="badge">memory</span>
  <span class="badge">ai-agent</span>
  <span class="badge">bm25</span>
  <span class="badge">multi-agent</span>
</div>

Persistent memory system for OpenClaw multi-agent workflows — **zero external dependencies**, pure Python BM25 + keyword indexing, DAG association graph, and session lifecycle hooks.

---

## ✨ Features

<div class="feature-grid">
  <div class="feature-card">
    <h3>🔍 BM25 Recall</h3>
    <p>Pure-Python Okapi BM25 semantic search. No pip packages — stdlib only.</p>
  </div>
  <div class="feature-card">
    <h3>🔑 Keyword Index</h3>
    <p>Fast token-based indexing with shared标记 and agent isolation.</p>
  </div>
  <div class="feature-card">
    <h3>🪝 Lifecycle Hooks</h3>
    <p>before-task recall + after-task save CLI for session memory management.</p>
  </div>
  <div class="feature-card">
    <h3>🔗 DAG Association</h3>
    <p>Typed directed links between memory entries. BFS path finding.</p>
  </div>
  <div class="feature-card">
    <h3>⚡ WAL Snapshot</h3>
    <p>Non-blocking index rebuild after writes. Sub-500ms recall target.</p>
  </div>
  <div class="feature-card">
    <h3>🌐 Multi-Agent</h3>
    <p>Agent-scoped memory isolation with shared cross-agent memories.</p>
  </div>
</div>

---

## 📦 Installation

```bash
# From GitHub (once published to ClawHub/npm)
openclaw plugins install @0xcjl/openclaw-memory-plugin

# From local directory
git clone https://github.com/0xcjl/openclaw-memory-plugin.git
openclaw plugins install ./openclaw-memory-plugin
```

Then restart the gateway:

```bash
openclaw gateway restart
```

---

## 🚀 Quick Start

### CLI Usage

```bash
# Install dependencies (none required — pure Python/stdlib)
# No pip install needed!

# Build indexes
./scripts/memory-hook.sh build

# Recall memories before a task (< 500ms target)
./scripts/memory-hook.sh before-task "optimize Vue rendering performance"

# Save after task completion
./scripts/memory-hook.sh after-task "completed Vue optimization" /tmp/result.md

# Search memories
python3 scripts/bm25_search.py --search "Docker CI/CD pipeline" --top 5 --json

# Build DAG auto-links (shared tags → edges)
python3 scripts/dag-builder.py build

# Find shortest path between memory entries
python3 scripts/dag-builder.py paths abc123 def456
```

### Plugin Tools (via OpenClaw)

Once installed, these tools are automatically registered:

| Tool | Description |
|------|-------------|
| `memory_recall` | Recall top-N memories before a task |
| `memory_save` | Save task output to memory |
| `memory_search` | BM25 full-text search |
| `memory_build` | Rebuild all indexes |
| `memory_dag_link` | Link two memory entries |

Example conversation with the agent:
> "recall memories about Vue performance optimization"
> "save this task: completed the refactor"
> "search memories for Docker deployment issues"

---

## 🗂️ Project Structure

```
openclaw-memory-plugin/
├── openclaw.plugin.json   # Plugin manifest
├── index.ts               # TypeScript entry (registers tools)
├── package.json           # npm package
├── scripts/
│   ├── memory-indexer.py  # Keyword index builder + search
│   ├── bm25_search.py     # Pure-Python BM25 implementation
│   ├── memory-hook.sh     # Session lifecycle CLI
│   ├── dag-builder.py     # Memory DAG builder + path queries
│   └── wal-snapshot.sh    # WAL snapshot / background rebuild
├── skills/
│   └── memory-recall/
│       └── SKILL.md       # Skill interface documentation
└── docs/
    └── ARCHITECTURE.md    # System architecture details
```

---

## ⚙️ Configuration

In `~/.openclaw/config.yaml`:

```yaml
plugins:
  entries:
    openclaw-memory-system:
      enabled: true
      config:
        agentId: dev          # default agent ID
        workspaceRoot: ~/.openclaw/workspace-dev
        topN: 3               # memories per recall
```

---

## 📊 Scoring Formula

```
combined_score = bm25_norm × 0.6 + weight × 0.2 + keyword_overlap × 0.2
```

| Component | Range | Weight |
|-----------|-------|--------|
| `bm25_norm` | 0–1 | 60% |
| `weight` | 0–1 | 20% |
| `keyword_overlap` | 0–1 | 20% |

---

## 🌳 Memory TTL Classes

| Class | Meaning | Auto-expiry |
|-------|---------|-------------|
| P0 | Core identity, key configs | Never |
| P1 | Project decisions, progress | ~90 days |
| P2 | Debug, temporary | ~30 days |

---

## 🐳 Requirements

- Python 3 (standard library only — **no pip packages**)
- Bash
- OpenClaw gateway

---

## 📄 License

MIT

---

## 🔗 Related

- [OpenClaw Docs](https://docs.openclaw.ai)
- [ClawhHub](https://clawhub.ai)
- [OpenClaw Memory System Architecture](./docs/ARCHITECTURE.md)

</div>

<!-- ─── 中文 ──────────────────────────────────────────────────────── -->
<div class="lang-section" id="sec-zh">

# OpenClaw 记忆系统插件

<div class="badge-row">
  <span class="badge">openclaw</span>
  <span class="badge">openclaw-plugin</span>
  <span class="badge">memory</span>
  <span class="badge">ai-agent</span>
  <span class="badge">bm25</span>
  <span class="badge">multi-agent</span>
</div>

OpenClaw 多智能体工作流的持久化记忆系统 — **零外部依赖**，纯 Python BM25 + 关键词索引，DAG 关联图谱，以及会话生命周期钩子。

---

## ✨ 功能特性

<div class="feature-grid">
  <div class="feature-card">
    <h3>🔍 BM25 语义搜索</h3>
    <p>纯 Python Okapi BM25 算法实现，无需任何 pip 包。</p>
  </div>
  <div class="feature-card">
    <h3>🔑 关键词索引</h3>
    <p>快速基于词的索引，支持 shared 标记和 Agent 隔离。</p>
  </div>
  <div class="feature-card">
    <h3>🪝 生命周期钩子</h3>
    <p>before-task 召回 + after-task 保存 CLI，管理会话记忆。</p>
  </div>
  <div class="feature-card">
    <h3>🔗 DAG 关联图谱</h3>
    <p>记忆节点间带类型的双向链接，支持 BFS 路径查找。</p>
  </div>
  <div class="feature-card">
    <h3>⚡ WAL 快照</h3>
    <p>写入后非阻塞索引重建，召回延迟目标 &lt; 500ms。</p>
  </div>
  <div class="feature-card">
    <h3>🌐 多 Agent 支持</h3>
    <p>Agent 作用域隔离记忆 + 跨 Agent 共享记忆。</p>
  </div>
</div>

---

## 📦 安装

```bash
# 从 ClawHub / npm 安装（发布后）
openclaw plugins install @0xcjl/openclaw-memory-plugin

# 从本地目录安装
git clone https://github.com/0xcjl/openclaw-memory-plugin.git
openclaw plugins install ./openclaw-memory-plugin
```

然后重启 Gateway：

```bash
openclaw gateway restart
```

---

## 🚀 快速上手

### CLI 使用

```bash
# 构建索引
./scripts/memory-hook.sh build

# 任务前召回（目标 < 500ms）
./scripts/memory-hook.sh before-task "优化 Vue 渲染性能"

# 任务后保存
./scripts/memory-hook.sh after-task "完成 Vue 优化" /tmp/result.md

# 记忆搜索
python3 scripts/bm25_search.py --search "Docker CI/CD" --top 5 --json

# 构建 DAG 自动链接（共享标签 → 边）
python3 scripts/dag-builder.py build

# 查找两条记忆间的最短路径
python3 scripts/dag-builder.py paths abc123 def456
```

### 插件工具（通过 OpenClaw）

安装后自动注册以下工具：

| 工具 | 说明 |
|------|------|
| `memory_recall` | 任务前召回 Top-N 记忆 |
| `memory_save` | 将任务输出保存到记忆 |
| `memory_search` | BM25 全文搜索 |
| `memory_build` | 重建所有索引 |
| `memory_dag_link` | 链接两条记忆 |

### Agent 对话示例

> "召回关于 Vue 性能优化的记忆"
> "保存这个任务：完成了重构"
> "搜索 Docker 部署相关的记忆"

---

## 🗂️ 项目结构

```
openclaw-memory-plugin/
├── openclaw.plugin.json   # 插件清单
├── index.ts               # TypeScript 入口（注册工具）
├── package.json           # npm 包配置
├── scripts/
│   ├── memory-indexer.py  # 关键词索引构建 + 搜索
│   ├── bm25_search.py     # 纯 Python BM25 实现
│   ├── memory-hook.sh     # 会话生命周期 CLI
│   ├── dag-builder.py     # 记忆 DAG 构建 + 路径查询
│   └── wal-snapshot.sh    # WAL 快照 / 后台重建
├── skills/
│   └── memory-recall/
│       └── SKILL.md       # 技能接口文档
└── docs/
    └── ARCHITECTURE.md    # 系统架构说明
```

---

## ⚙️ 配置

在 `~/.openclaw/config.yaml` 中：

```yaml
plugins:
  entries:
    openclaw-memory-system:
      enabled: true
      config:
        agentId: dev          # 默认 Agent ID
        workspaceRoot: ~/.openclaw/workspace-dev
        topN: 3               # 每次召回的记忆数量
```

---

## 📊 评分公式

```
combined_score = bm25_norm × 0.6 + weight × 0.2 + keyword_overlap × 0.2
```

| 组成部分 | 范围 | 权重 |
|---------|------|------|
| `bm25_norm` | 0–1 | 60% |
| `weight` | 0–1 | 20% |
| `keyword_overlap` | 0–1 | 20% |

---

## 🌳 记忆 TTL 分类

| 类别 | 含义 | 自动过期 |
|------|------|---------|
| P0 | 核心身份、关键配置 | 永不 |
| P1 | 项目决策、进展 | 约 90 天 |
| P2 | 调试、临时 | 约 30 天 |

---

## 🐳 环境要求

- Python 3（标准库 — **无需任何 pip 包**）
- Bash
- OpenClaw Gateway

---

## 📄 许可证

MIT

---

## 🔗 相关链接

- [OpenClaw 文档](https://docs.openclaw.ai)
- [ClawhHub](https://clawhub.ai)
- [系统架构详解](./docs/ARCHITECTURE.md)

</div>

<!-- ─── 日本語 ────────────────────────────────────────────────────── -->
<div class="lang-section" id="sec-ja">

# OpenClaw メモリシステムプラグイン

<div class="badge-row">
  <span class="badge">openclaw</span>
  <span class="badge">openclaw-plugin</span>
  <span class="badge">memory</span>
  <span class="badge">ai-agent</span>
  <span class="badge">bm25</span>
  <span class="badge">multi-agent</span>
</div>

OpenClaw マルチエージェントワークフロー向け永続メモリシステム — **外部依存ゼロ**、ピュアPython BM25 + キーワードインデックス、DAG連想グラフ、セッションライフサイクルフック。

---

## ✨ 機能

<div class="feature-grid">
  <div class="feature-card">
    <h3>🔍 BM25 リ:call</h3>
    <p>ピュアPython Okapi BM25実装。pipパッケージ不要。</p>
  </div>
  <div class="feature-card">
    <h3>🔑 キーワードインデックス</h3>
    <p>sharedフラグとエージェント分離に対応する高速トークンインデックス。</p>
  </div>
  <div class="feature-card">
    <h3>🪝 ライフサイクルフック</h3>
    <p>before-task recall + after-task save CLI。</p>
  </div>
  <div class="feature-card">
    <h3>🔗 DAG連想グラフ</h3>
    <p>メモリエントリ間の型付き有向リンク。BFS経路検索。</p>
  </div>
  <div class="feature-card">
    <h3>⚡ WALスナップショット</h3>
    <p>書き込み後のノンブロッキングインデックス再構築。</p>
  </div>
  <div class="feature-card">
    <h3>🌐 マルチエージェント</h3>
    <p>エージェントスコープのメモリ分離と共有クロスエージェントメモリ。</p>
  </div>
</div>

---

## 📦 インストール

```bash
# ClawHub / npm から（公開後）
openclaw plugins install @0xcjl/openclaw-memory-plugin

# ローカルディレクトリから
git clone https://github.com/0xcjl/openclaw-memory-plugin.git
openclaw plugins install ./openclaw-memory-plugin
```

Gatewayを再起動：

```bash
openclaw gateway restart
```

---

## 🚀 クイックスタート

```bash
# インデックスのビルド
./scripts/memory-hook.sh build

# タスク前のrecall（目標 < 500ms）
./scripts/memory-hook.sh before-task "Vueパフォーマンス最適化"

# タスク後の保存
./scripts/memory-hook.sh after-task "Vue最適化完了" /tmp/result.md

# メモリ検索
python3 scripts/bm25_search.py --search "Docker CI/CD" --top 5 --json

# DAG自動リンクビルド
python3 scripts/dag-builder.py build
```

---

## ⚙️ 設定

`~/.openclaw/config.yaml`:

```yaml
plugins:
  entries:
    openclaw-memory-system:
      enabled: true
      config:
        agentId: dev
        workspaceRoot: ~/.openclaw/workspace-dev
        topN: 3
```

---

## 🐳 必要環境

- Python 3（標準ライブラリのみ — pipパッケージ不要）
- Bash
- OpenClaw Gateway

---

## 📄 ライセンス

MIT

</div>

<script>
// ── Language switcher ────────────────────────────────────────────────────────
(function () {
  var LANG = localStorage.getItem('readme-lang') || 'en';
  var tabs = document.getElementById('langTabs');
  var sections = document.querySelectorAll('.lang-section');

  function activate(lang) {
    localStorage.setItem('readme-lang', lang);
    sections.forEach(function (s) {
      s.classList.toggle('active', s.id === 'sec-' + lang);
    });
    tabs.querySelectorAll('button').forEach(function (b) {
      b.classList.toggle('active', b.dataset.lang === lang);
    });
  }

  // Check URL param first
  var params = new URLSearchParams(window.location.search);
  if (params.has('lang')) {
    var urlLang = params.get('lang');
    if (['en', 'zh', 'ja'].indexOf(urlLang) !== -1) {
      LANG = urlLang;
      activate(LANG);
      // Remove lang param from URL without reload
      params.delete('lang');
      var newUrl = window.location.pathname + (params.toString() ? '?' + params : '');
      history.replaceState(null, '', newUrl);
    }
  } else {
    activate(LANG);
  }

  tabs.addEventListener('click', function (e) {
    var btn = e.target.closest('button');
    if (btn) activate(btn.dataset.lang);
  });
})();
</script>

</body>
</html>
