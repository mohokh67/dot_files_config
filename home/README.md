# home/

This directory is the GNU Stow package. Everything inside mirrors the structure of `~` and gets symlinked there when you run:

```sh
stow -d ~/dev/dotfiles -t ~ home
```

Only files intended to live in `~` belong here.
