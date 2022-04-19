# Neovim

Installing neovim should be pretty easy.

First get the latest appimage:

```sh
curl -LO https://github.com/neovim/neovim/releases/download/nightly/nvim.appimage
```

Then chmod it to be executable:

```sh
chmod u+x nvim.appimage
```

If you run `./nvim.appimage` a new neovim instance will be started.

Then you can move it to somewhere in your $PATH. To keep our home directory clean, we'll move it to `~/bin`. Make sure `~/bin` is in your $PATH.

```sh
mkdir -p ~/bin
mv ./nvim.appimage ~/bin/nvim
```
