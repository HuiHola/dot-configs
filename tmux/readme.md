# ⚡ My Tmux Configuration

A minimal, keyboard-focused **tmux configuration** designed for a fast terminal workflow with **Vim-style navigation, popup terminals, Lazygit, clipboard integration, and a clean interface**.

> Built for developers who prefer working primarily from the terminal.

---

## ✨ Features

* `\` as the tmux prefix
* Popup terminal with `Space`
* Lazygit popup with `g`
* Window selector using `fzf`
* Vim-style pane movement
* Vim-style copy mode
* System clipboard integration with `xclip`
* Mouse support
* Large `50,000` line history
* Automatic window renumbering
* Hidden status bar by default
* Toggle status bar with `b`
* Pane resizing with `Shift + H/J/K/L`
* Tiled layout shortcut
* Quick configuration reload
* Dark Catppuccin-inspired colors

---

## 📦 Requirements

Install the following packages:

### Debian / Ubuntu / Kali Linux

```bash
sudo apt install tmux fzf xclip
```

For Lazygit, install it separately:

```bash
sudo apt install lazygit
```

Check the installations:

```bash
tmux -V
fzf --version
xclip -version
lazygit --version
```

---

## 📁 Installation

Create the tmux configuration directory:

```bash
mkdir -p ~/.config/tmux
```

Create the configuration file:

```bash
nvim ~/.config/tmux/tmux.conf
```

Paste the configuration into the file.

Then start tmux:

```bash
tmux
```

Or reload the configuration from inside tmux:

```text
\ + r
```

You should see:

```text
Reloaded
```

---

# ⌨️ Keybindings

## Prefix

The default tmux prefix `Ctrl+B` has been disabled.

### New Prefix

```text
\
```

Press:

```text
\ + key
```

to execute a tmux command.

For example:

```text
\ + Space
```

opens the popup terminal.

---

## 🪟 Popups

### Popup Terminal

```text
\ + Space
```

Opens an 80% × 80% popup terminal.

```tmux
bind Space display-popup -E -w 80% -h 80%
```

---

### Window Selector

```text
\ + w
```

Opens an `fzf` window selector.

You can search through your tmux windows and select one interactively.

---

### Lazygit

```text
\ + g
```

Opens Lazygit inside an 80% × 80% popup.

```text
\ + g
```

This makes Git operations accessible without leaving tmux.

---

# 🖱️ Mouse

Mouse support is enabled:

```tmux
set -g mouse on
```

You can:

* Select panes
* Resize panes
* Scroll
* Select windows
* Interact with tmux using the mouse

---

# 📜 History

Tmux history is increased to:

```text
50,000 lines
```

```tmux
set -g history-limit 50000
```

Useful when working with:

* Build output
* Logs
* Compilers
* Debugging
* Long-running commands

---

# 🪟 Windows

Windows start at index `1`:

```tmux
set -g base-index 1
```

Panes also start at `1`:

```tmux
setw -g pane-base-index 1
```

Windows are automatically renumbered:

```tmux
set -g renumber-windows on
```

---

# 📐 Splits

## Horizontal Split

```text
\ + v
```

Creates a pane on the right.

```tmux
bind v split-window -h
```

---

## Vertical Split

```text
\ + h
```

Creates a pane below.

```tmux
bind h split-window -v
```

---

# 🧭 Pane Movement

Movement follows Vim's:

```text
h j k l
```

### Move Left

```text
\ + h
```

### Move Down

```text
\ + j
```

### Move Up

```text
\ + k
```

### Move Right

```text
\ + l
```

Configuration:

```tmux
bind h select-pane -L
bind j select-pane -R
bind k select-pane -U
bind l select-pane -D
```

---

# 📏 Pane Resizing

Use:

```text
\ + H
\ + J
\ + K
\ + L
```

### Resize Left

```text
\ + Shift + H
```

### Resize Down

```text
\ + Shift + J
```

### Resize Up

```text
\ + Shift + K
```

### Resize Right

```text
\ + Shift + L
```

Each press moves the pane boundary by `5` cells.

---

# 📋 Clipboard

Tmux uses Vim copy mode:

```tmux
setw -g mode-keys vi
```

Start copy mode:

```text
\ + [
```

Then:

```text
Space
```

starts the selection.

Press:

```text
Enter
```

to copy the selection to the system clipboard.

The configuration uses:

```bash
xclip -selection clipboard
```

So copied text can be pasted into applications outside tmux.

---

# 📊 Status Bar

The status bar is **disabled by default**:

```tmux
set -g status off
```

This keeps the terminal clean and distraction-free.

## Toggle Status Bar

```text
\ + b
```

The status bar can be turned on and off dynamically.

When enabled, it displays the current session and window numbers.

---

# 🎨 Theme

The configuration uses a dark color palette inspired by Catppuccin:

```text
Background : #1e1e2e
Foreground : #cdd6f4
Blue       : #89b4fa
Border     : #45475a
Message BG : #313244
```

Active panes and windows are highlighted using the blue accent.

---

# 🧩 Layouts

## Tiled Layout

```text
\ + t
```

Automatically arranges all panes into a tiled layout.

```tmux
bind t select-layout tiled
```

---

# 🔄 Reload Configuration

After changing `tmux.conf`:

```text
\ + r
```

This reloads:

```text
~/.config/tmux/tmux.conf
```

and displays:

```text
Reloaded
```

You don't need to restart tmux.

---

# 🗺️ Keybinding Cheat Sheet

| Key           | Action               |
| ------------- | -------------------- |
| `\`           | Prefix               |
| `\ + Space`   | Popup terminal       |
| `\ + w`       | fzf window selector  |
| `\ + g`       | Lazygit popup        |
| `\ + b`       | Toggle status bar    |
| `\ + v`       | Horizontal split     |
| `\ + h`       | Vertical split       |
| `\ + h/j/k/l` | Move between panes   |
| `\ + H/J/K/L` | Resize panes         |
| `\ + t`       | Tiled layout         |
| `\ + r`       | Reload configuration |
| `\ + [`       | Enter copy mode      |
| `Space`       | Start selection      |
| `Enter`       | Copy selection       |

---

# 📄 Configuration

The complete configuration is located at:

```text
~/.config/tmux/tmux.conf
```

The configuration is intentionally kept simple and dependency-light.

---

## 🔧 Philosophy

This configuration is built around three ideas:

```text
Keyboard First
      ↓
Minimal Interface
      ↓
Fast Terminal Workflow
```

Instead of relying heavily on menus or mouse interaction, common operations are mapped to short Vim-like keybindings.

---

## 🚀 Workflow

A typical workflow looks like:

```text
                    tmux
                      │
          ┌───────────┼───────────┐
          │           │           │
       Terminal     Editor      Lazygit
          │           │           │
       Commands     Neovim      Git
          │
       Popups
          │
       fzf / tools
```

Everything stays inside one tmux session.

---


**Made for terminal lovers. ⚡**
