# ⚡ Neovim Modern Dev Setup (LSP + Autocomplete + Git + UI)

A powerful, clean, and modern Neovim setup for Linux users with full support for:

-  LSPs: Python, JavaScript, TypeScript, Node.js, HTML, CSS, JSON, YAML, Bash, Lua
-  Autocompletion with `nvim-cmp` + Snippets via `LuaSnip`
-  Fuzzy finding with `Telescope`
-  Syntax highlighting with `Treesitter`
-  File tree explorer with `nvim-tree`
-  Git integration using `lazygit`, `gitsigns`, and `fugitive`
-  Beautiful theme: Tokyonight
-  MarkDown file view
---

## 📦 Features

| Feature | Plugin |
|--------|--------|
| LSP | `nvim-lspconfig`, `pyright`, `tsserver`, etc. |
| Autocomplete | `nvim-cmp`, `cmp-nvim-lsp`, `LuaSnip` |
| Git Integration | `lazygit.nvim`, `gitsigns.nvim`, `vim-fugitive` |
| File Explorer | `nvim-tree.lua` |
| Fuzzy Finder | `telescope.nvim` |
| Status Line | `lualine.nvim` |
| Theme | `tokyonight.nvim` |

---

## Quick Start

### 1. Clone the repo (or just download the script)

```bash
npm install -g \
  pyright \
  typescript \
  typescript-language-server \
  vscode-langservers-extracted \
  yaml-language-server \
  bash-language-server

pip install --user pylint
sudo apt install ripgrep
sudo apt install lazygit
```
### 2. Open nvim and run
```bash
:PlugInstall
```



# ⚡ Neovim Shortcut Keys

A quick reference for the custom keybindings in this Neovim configuration.

---

## 🎯 Leader Key

This configuration uses Neovim's default **Leader key**:

```text
\
```

So:

```text
<leader>ff
```

means:

```text
\ + f + f
```

---

## 🌳 File Explorer

| Shortcut   | Action          |
| ---------- | --------------- |
| `Ctrl + N` | Toggle NvimTree |

---

## 🔎 Telescope

| Shortcut    | Action                  |
| ----------- | ----------------------- |
| `\ + f + f` | Find files              |
| `\ + f + g` | Live grep / search text |

---

## 🔀 Git

| Shortcut    | Action          |
| ----------- | --------------- |
| `\ + g + s` | Open Git status |
| `\ + l + g` | Open Lazygit    |

---

## 🧠 LSP

| Shortcut    | Action                     |
| ----------- | -------------------------- |
| `g d`       | Go to definition           |
| `K`         | Show documentation / hover |
| `\ + r + n` | Rename symbol              |
| `\ + f`     | Format current file        |

---

## 💻 Floating Terminal

| Shortcut    | Action                             |
| ----------- | ---------------------------------- |
| `\ + t + t` | Toggle floating terminal           |
| `\ + t + t` | Toggle terminal from terminal mode |

The floating terminal opens at approximately:

```text
90% width
85% height
```

---

## ✍️ Completion

When completion suggestions are available:

| Key     | Action                      |
| ------- | --------------------------- |
| `Enter` | Confirm selected completion |

Completion sources include:

* LSP
* Current buffer
* File paths

---

## 📝 Markdown

Markdown files automatically enable:

```text
Render Markdown
```

This provides rendered Markdown inside Neovim.

---

## 🧩 Supported LSPs

This configuration includes LSP support for:

```text
Python       → pyright
JavaScript   → tsserver
HTML         → html
CSS          → cssls
JSON         → jsonls
YAML         → yamlls
Bash         → bashls
Lua          → lua_ls
C/C++        → clangd
Arduino      → clangd
```

---

# 📋 Quick Cheat Sheet

```text
┌──────────────────────────────────────────┐
│           NEOVIM SHORTCUTS               │
├──────────────────────────────────────────┤
│ Ctrl + N       File Explorer             │
│                                          │
│ \ ff           Find Files                │
│ \ fg           Live Grep                 │
│                                          │
│ \ gs           Git Status                │
│ \ lg           Lazygit                   │
│                                          │
│ gd             Go to Definition          │
│ K              Hover Documentation       │
│ \ rn           Rename Symbol             │
│ \ f            Format File               │
│                                          │
│ \ tt           Floating Terminal         │
│                                          │
│ Enter          Confirm Completion        │
└──────────────────────────────────────────┘
```

---

## 🔌 Main Plugins

```text
NvimTree        → File Explorer
Telescope       → File/Text Search
Fugitive        → Git
Gitsigns        → Git Changes
Lazygit         → Git UI
LSPConfig       → Language Server
nvim-cmp        → Completion
LuaSnip         → Snippets
Treesitter      → Syntax Highlighting
Floaterm        → Floating Terminal
Render-Markdown → Markdown Rendering
TokyoNight      → Theme
Arduino-Nvim    → Arduino Development
```

> **Note:** `<leader>` is currently `\` only if you have configured `mapleader` elsewhere. The configuration you posted does **not** explicitly set `vim.g.mapleader`, so Neovim's default leader is actually `\`.





