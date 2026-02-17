# Ghostty Configuration

## Shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl+Cmd+T` | Toggle quick terminal (works globally from any app) |
| `Cmd+Up` | Jump to previous shell prompt |
| `Cmd+Down` | Jump to next shell prompt |
| `Cmd+Shift+P` | Open command palette |
| `Cmd+C` | Copy selection (passes through to shell if nothing selected) |
| `Alt+Click` | Move cursor to click position at shell prompt |

## Features

### Quick Terminal
A drop-down terminal summoned from any app with `Ctrl+Cmd+T`. Slides in from the top of the screen at 80% width, auto-hides when focus moves away.

### Auto Light/Dark Theme
Uses Catppuccin Latte (light) and Catppuccin Mocha (dark), switching automatically with macOS appearance.

### Transparency + Blur
Semi-transparent background (92% opacity) with a blur effect behind the window.

### Font Rendering
Font thickening enabled for crisper text on Retina/HiDPI displays. Minimum contrast ratio enforced at 1.1 to prevent unreadable color combinations.

### Shell Integration
- Cursor shape changes at the prompt
- Sudo credential caching
- Terminal title set to current command/directory
- `TERM=xterm-256color` auto-set over SSH
- Ghostty terminfo auto-copied to remote hosts over SSH

### Clipboard & Security
- Paste protection warns before pasting potentially dangerous content (e.g. commands with newlines)
- Trailing spaces trimmed on copy
- Text auto-copied to clipboard on selection

### Window
- Hidden titlebar for a clean look
- 10px padding with extended edge colors
- Display P3 color space for wider gamut on Apple displays
- Window state and font size preserved across restarts
- Resize overlay shows dimensions after first resize

### Safety
- Confirmation prompt before closing a terminal with a running process
- 10-second undo window for accidentally closed tabs
