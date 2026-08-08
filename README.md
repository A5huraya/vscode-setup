# VS Code Setup

A clean, low-distraction VS Code config: Catppuccin Macchiato theme, JetBrains Mono Nerd Font, smooth cursor and scrolling, minimal chrome (no minimap, sidebar moved to the right). Language-agnostic — works for any stack, with optional per-language blocks you can turn on as needed.

## What's in here

| File | Purpose |
|---|---|
| `settings.json` | Editor, workbench, git, and privacy settings |
| `extensions.json` | Recommended extensions (theme + icons) |

## Requirements

- [Catppuccin for VS Code](https://marketplace.visualstudio.com/items?itemName=Catppuccin.catppuccin-vsc) OR [Dark Magic Themes](https://marketplace.visualstudio.com/items?itemName=davidmorais.dark-magic-themes) — color theme
- [Catppuccin Icons for VS Code](https://marketplace.visualstudio.com/items?itemName=Catppuccin.catppuccin-vsc-icons) — icon theme
- [JetBrains Mono Nerd Font](https://www.nerdfonts.com/font/jetbrains-mono) installed on your system

## Install

1. Install the two extensions above (or let `extensions.json` prompt you — see below).
2. Copy the contents of `settings.json` into your user settings file:

   | OS | Path |
   |---|---|
   | macOS | `~/Library/Application Support/Code/User/settings.json` |
   | Linux | `~/.config/Code/User/settings.json` |
   | Windows | `%APPDATA%\Code\User\settings.json` |

   Or open Settings (`Ctrl/Cmd + ,`) → click the `{}` icon top-right to open the JSON view → paste in, merging with anything you want to keep.

3. (Optional, per-project) Drop `extensions.json` into a `.vscode/` folder in any repo. VS Code will prompt collaborators to install the recommended extensions when they open it.

## Notes

- `editor.accessibilitySupport` is set to `"off"` — this removes a small amount of input lag on typing/deleting. Set it back to `"auto"` if you rely on a screen reader.
- The bottom of `settings.json` has commented-out blocks for AI tooling (Claude Code / GitHub Copilot), common per-language formatters (Rust, Python, JS/TS), and ESP-IDF (embedded dev). Uncomment only what applies to you — the file works as-is without any of them.
- `workbench.sideBar.location` is set to `"right"`; flip it back to `"left"` if you'd rather keep the default layout.
