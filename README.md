# Using this repo

## Pulling locally

```bash
git clone --separate-git-dir=$HOME/.myconf /path/to/repo $HOME/myconf-tmp
cp ~/myconf-tmp/.gitmodules ~  # If you use Git submodules
rm -r ~/myconf-tmp/
alias config='/usr/bin/git --git-dir=$HOME/.myconf/ --work-tree=$HOME'
```

## Creating a non-intrusive dot-files repo

Inspired by [StreakyCobra](https://news.ycombinator.com/item?id=11070797#11071754):

1. `git init --bare $HOME/.myconf`
2. `alias config='/usr/bin/git --git-dir=$HOME/.myconf/ --work-tree=$HOME'`
3. `config config status.showUntrackedFiles no`
4. `config add .vimrc`
5. `config commit -m "Add vim config"`
6. `config push`
