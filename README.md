# dotfiles

## Setup

```sh
git clone <repo> ~/dev/dotfiles
brew install stow
stow -d ~/dev/dotfiles -t ~ home
```

Stow creates symlinks in `~` pointing into this repo. Edit files here; changes propagate everywhere.

## What's managed

| File in "home" dir          | Target                        |
| --------------------------- | ----------------------------- |
| `.zshrc`                    | `~/.zshrc`                    |
| `.oh-my-posh.toml`          | `~/.oh-my-posh.toml`          |
| `.config/zed/settings.json` | `~/.config/zed/settings.json` |
| `.claude/CLAUDE.md`         | `~/.claude/CLAUDE.md`         |
| `.claude/settings.json`     | `~/.claude/settings.json`     |
| `.claude/skills/`           | `~/.claude/skills/`           |

Not managed by stow (reference only): `betterfox/`, `ghostly/`, `vscode/`, `zsh/`

## Adding a new machine

Remove any conflicting files first, then run the stow command above. Stow will refuse to overwrite existing regular files.

## Never commit

`~/.claude/settings.json` is safe (no secrets). Never commit: `history.jsonl`, `sessions/`, `cache/`, `backups/`, `projects/`.
