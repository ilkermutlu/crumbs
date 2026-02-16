# crumbs

Dotfiles managed with [chezmoi](https://www.chezmoi.io/).

## What's included

- **Shell** — zsh config (`.zshrc`, `.zshenv`, `.zprofile`)
- **Git** — global gitconfig and ignore patterns (templated for name/email)
- **Neovim** — Lua-based config with Lazy plugin manager (`nvim-ja`)
- **Doom Emacs** — `config.el`, `init.el`, `packages.el`
- **tmux** — `.tmux.conf`
- **Terminal** — Ghostty and Kitty configs
- **SSH** — client config
- **CLI tools** — GitHub CLI, television, git-delta
- **Brewfile** — Homebrew packages and casks for macOS

## Setup

```sh
# Install chezmoi and apply
sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply ilkermutlu/crumbs
```

On first run, chezmoi will prompt for your name and email (used in gitconfig templates). On macOS, it will also run `brew bundle` to install packages from the Brewfile.

## Usage

```sh
# Pull latest changes and apply
chezmoi update

# Edit a managed file
chezmoi edit ~/.zshrc

# See what would change
chezmoi diff

# Apply changes
chezmoi apply
```
