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

