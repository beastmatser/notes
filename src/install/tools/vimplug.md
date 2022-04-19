# Vimplug

Vimplug is a plugin manager for Vim. Installing it is pretty easy.

```sh
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

If you already had an `init.vim` or `.vimrc` file, you will need to run `:PlugInstall` in your Vim instance to install the plugins.

If neoclide is one of your extensions, installing some lsp's might be useful. Using `coc-marketplace` you can view all available extensions, which you can call upon by using `:CocList marketplace`.

```sh
:CocInstall coc-marketplace coc-yaml coc-vimlsp coc-tsserver coc-tslint coc-toml coc-rust-analyzer coc-pyright coc-prettier coc-pairs coc-json
```
