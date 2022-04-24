# Dotfiles

You can find my dotfiles at [beastmatser/dotfiles](https://github.com/beastmatser/dotfiles). You can install them by running:

```sh
git clone http://github.com/beastmatser/dotfiles ~/dotfiles && cd ~/dotfiles

# .gitignore does not work with stow, so we'll symlink it manually
ln -s ~/dotfiles/git/.gitignore ~/.gitignore
```

My dotfiles are managed by [stow](https://www.gnu.org/software/stow/). First, you need to install stow:

```sh
sudo apt install stow
```

Then you can stow any directory you want e.g.:

```sh
stow fish
stow nvim

# You can also stow all of the dotfiles
stow */
```
