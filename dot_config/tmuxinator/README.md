# Tmuxinator Configuration

Project layouts for [tmuxinator](https://github.com/tmuxinator/tmuxinator), managed as an oh-my-zsh plugin.

## Usage

```sh
# Start a project
txs <project>

# List available projects
txl

# Edit a project layout
txo <project>

# Create a new project
txn <project>
```

These aliases are provided by the `tmuxinator` oh-my-zsh plugin. The full `tmuxinator` command also works.

## Layouts

### `example.yml`

A starter template with three windows:

| Window | Purpose |
|---|---|
| `editor` | Vertical split with nvim |
| `terminal` | General-purpose shell |
| `server` | Runs `npm run dev` |

### Adding your own

Create project-specific layouts that shouldn't be shared by adding them to `.gitignore` in the chezmoi source directory:

```
dot_config/tmuxinator/my-project.yml
```

## How it's wired up

- **Brewfile** installs `tmuxinator` via Homebrew
- **`.zshrc`** loads the `tmuxinator` oh-my-zsh plugin (provides the `mux` alias and completions)
- **`.tmux.conf`** provides the underlying tmux configuration (vi mode, mouse support, `Ctrl+Space` prefix)
