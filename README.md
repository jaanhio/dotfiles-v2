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
stow --target $HOME tmux # tmux refers to the name of directory for storing tmux related config files. 
```

This will setup the following files in the $HOME directory symlinked to the config files in this repo.
```
.tmux.conf -> Documents/repos/dotfiles-v2/tmux/.tmux.conf
.tmux.reset.conf -> Documents/repos/dotfiles-v2/tmux/.tmux.reset.conf
```

## Setting up tmux

Several plugins are used in this setup.

After copying the config files, install the plugins using `prefix + I`.

#### Installing tmux-thumbs

`tmux-thumbs` is a plugin written in Rust. 

There's 2 ways to install it:
- compiling it locally
- downloading binary

For the first option, `rustc` is required. On Mac, this can be installed using `rustup`, which in turn can be installed using `homebrew`. You can follow the guide [here](https://www.petergirnus.com/blog/rust-macos-how-to-install).

```
brew install rustup
```

Install packages.
```
rustup-init
```

After installation, a `.cargo` directory should be found in the `$HOME` directory. Binaries are located in `$HOME/.cargo/bin`. Update `$PATH` to access these binaries.
