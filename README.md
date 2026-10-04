# ⚡ dot-configs

My personal Linux configuration files for a fast, keyboard-driven development environment.

Built around **Neovim + tmux + terminal tools**, with a focus on simplicity, productivity, and a clean developer workflow.

---

## 📁 Configurations

| Configuration        | Description                                                                                    |
| -------------------- | ---------------------------------------------------------------------------------------------- |
| 📝 [Neovim](./nvim/) | Neovim configuration, plugins, LSP, Git, Telescope, terminal and development tools             |
| 🖥️ [tmux](./tmux/)  | Keyboard-focused tmux configuration with popups, Lazygit, Vim navigation and clipboard support |

---

## 📝 Neovim

My Neovim setup is designed as a complete development environment.

### Includes

* 🌳 NvimTree file explorer
* 🔎 Telescope file and text search
* 🔀 Git & Gitsigns
* 🐙 Lazygit integration
* 🧠 LSP support
* ✨ Autocompletion with nvim-cmp
* 📦 LuaSnip
* 🌲 Treesitter
* 💻 Floating terminal
* 📝 Markdown rendering
* 🎨 TokyoNight theme
* 🔌 Arduino development support

👉 **[View Neovim Configuration →](./nvim/readme.md)**

---

## 🖥️ tmux

My tmux configuration is focused on keeping the terminal clean and minimizing unnecessary mouse usage.

### Includes

* `\` as the tmux prefix
* ⚡ Popup terminal
* 🔎 `fzf` window selector
* 🐙 Lazygit popup
* 🧭 Vim-style pane navigation
* 📐 Vim-style pane resizing
* 📋 System clipboard integration
* 🖱️ Mouse support
* 📜 50,000 line history
* 🎨 Dark theme
* 📊 Hidden status bar
* 🔄 Quick configuration reload

👉 **[View tmux Configuration →](./tmux/readme.md)**

---

## 🗂️ Repository Structure

```text
dot-configs/
│
├── README.md
│
├── nvim/
│   ├── init.lua
│   └── README.md
│
└── tmux/
    ├── tmux.conf
    └── README.md
```

Each configuration has its own README containing its **installation instructions and shortcut reference**.

---

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/HuiHola/dot-configs.git
```

Enter the repository:

```bash
cd dot-configs
```

Then choose the configuration you want:

```bash
cd nvim
```

or:

```bash
cd tmux
```

Follow the README inside each directory for installation instructions.

---

## 🛠️ Philosophy

These configurations are built around:

```text
        ┌─────────────────────┐
        │    Keyboard First   │
        └──────────┬──────────┘
                   │
                   ▼
        ┌─────────────────────┐
        │   Minimal & Fast    │
        └──────────┬──────────┘
                   │
                   ▼
        ┌─────────────────────┐
        │ Terminal Workflow   │
        └──────────┬──────────┘
                   │
                   ▼
        ┌─────────────────────┐
        │   Developer Setup   │
        └─────────────────────┘
```

The goal is not to have the most complicated configuration, but to have tools that are **fast, familiar, and useful every day**.

---

## 🔧 Tools

```text
Neovim
tmux
Git
Lazygit
fzf
LSP
Treesitter
```

---

## 📌 Status

This repository is actively evolving as I improve my Linux and development workflow.

New configurations and improvements may be added over time.

---

## 👤 Author

**Dhruv Namdev**

GitHub: **[HuiHola](https://github.com/HuiHola)**

---

⭐ If you find any configuration useful, feel free to fork it and customize it for your own workflow.
