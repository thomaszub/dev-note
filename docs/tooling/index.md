# Tooling

This note is about useful tooling.

## dotfiles

Add to `.zshrc` the alias

```sh
alias dotcfg="git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME"
```

Then execute the following commands:

```sh
git init --bare $HOME/.dotfiles
dotcfg config --local status.showUntrackedFiles no
```

Setting the upstream, adding files, etc. work as usual except the command `dotcfg` is used.