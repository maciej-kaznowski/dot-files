# dot-files

## Summary

Configured in this repo are various dot files for my personal machine:
- [Kitty](https://github.com/kovidgoyal/kitty) as the terminal
- [Sway](https://github.com/swaywm/sway) as the compositor
- [Waybar](https://github.com/Alexays/Waybar) as the system bar
- [Swaylock-effects](https://github.com/mortie/swaylock-effects) as the lockscreen
- [Wofi](https://hg.sr.ht/~scoopta/wofi) as the application launcher
- [zsh](https://www.zsh.org/) and [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh) as the shell


## Previews
![Desktop](docs/readme_desktop.png?raw=true "Desktop")
![Wofi](docs/readme_wofi.png?raw=true "Wofi")
![Windows](docs/readme_windows.png?raw=true "Windows")

## Using this repo

### Pulling locally

```bash
git clone --separate-git-dir=$HOME/.myconf /path/to/repo $HOME/myconf-tmp
cp ~/myconf-tmp/.gitmodules ~  # If you use Git submodules
rm -r ~/myconf-tmp/
alias config='/usr/bin/git --git-dir=$HOME/.myconf/ --work-tree=$HOME'
```

### Creating a non-intrusive dot-files repo

Inspired by [StreakyCobra](https://news.ycombinator.com/item?id=11070797#11071754):

1. `git init --bare $HOME/.myconf`
2. `alias config='/usr/bin/git --git-dir=$HOME/.myconf/ --work-tree=$HOME'`
3. `config config status.showUntrackedFiles no`
4. `config add .vimrc`
5. `config commit -m "Add vim config"`
6. `config push`
