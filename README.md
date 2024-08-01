# dotfiles-v2

This is the updated dotfiles collection that uses [GNU Stow](https://www.gnu.org/software/stow/) to symlink to config files in $HOME.

## Setting up using `stow`

Let's say we want to symlink the tmux related configuration file.

```
├── tmux
│   ├── .tmux.conf
│   └── .tmux.reset.conf

```

Execute:
```
stow --target $HOME tmux 
```

This will setup the following files in the $HOME directory symlinked to the configuration files in this repo.
```
.tmux.conf -> Documents/repos/dotfiles-v2/tmux/.tmux.conf
.tmux.reset.conf -> Documents/repos/dotfiles-v2/tmux/.tmux.reset.conf
```
