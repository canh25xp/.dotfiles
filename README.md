# OpenWRT dotfiles

## Setup

```sh
git init --bare $HOME/.dotfiles
alias chezmoi='git --git-dir=$HOME/.my-dotfiles/ --work-tree=$HOME'
chezmoi remote add origin https://github.com/canh25xp/.dotfiles
chezmoi config status.showUntrackedFiles no
```

> [!NOTE]
> The reason I chosen `chezmoi` as an alias is because I'm still using [chezmoi](https://github.com/twpayne/chezmoi) as my daily dotfile manager.

## Restore

```sh
git clone --bare https://github.com/canh25xp/.dotfiles
chezmoi config status.showUntrackedFiles no
```

## Usage

```sh
chezmoi status
chezmoi add .gitconfig
chezmoi commit -m 'Add gitconfig'
chezmoi push
```

## References

- [Store dotfiles in a bare git repository](https://www.atlassian.com/git/tutorials/dotfiles)
