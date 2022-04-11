# Install scripts

- [Install scripts](#install-scripts)
  - [Programming Languages](#programming-languages)
    - [Python](#python)
    - [Javascript](#javascript)
    - [Rust](#rust)
    - [Odin](#odin)
      - [Install Odin](#install-odin)
      - [Install ols](#install-ols)
      - [Ols config](#ols-config)
      - [Setup neoclide with ols](#setup-neoclide-with-ols)
    - [Nim](#nim)
    - [Kotlin](#kotlin)
  - [Zsh](#zsh)
    - [Zsh](#zsh-1)
  - [Neovim](#neovim)
    - [Neovim](#neovim-1)
    - [VimPlug](#vimplug)
    - [Neoclide extensions](#neoclide-extensions)
  - [Vscode](#vscode)
    - [Plugins](#plugins)

## Programming Languages

### Python

```sh
sudo apt install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl \
git
git clone https://github.com/pyenv/pyenv.git ~/.pyenv
pyenv install 3.10.x
pyenv global 3.10.x
```

### Javascript

```sh
curl -sL https://deb.nodesource.com/setup_17.x | sudo -E bash
sudo apt install nodejs -y

# Install yarn
sudo npm install -g pnpm
```

### Rust

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
# Install a complete toolchain
sudo apt-get update
sudo apt install build-essential -y
```

### Odin

#### Install Odin

```sh
git clone https://github.com/odin-lang/Odin
cd Odin
printf "deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial-12 main" |sudo tee /etc/apt/sources.list.d/llvm-toolchain-xenial-12.list
wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key |sudo apt-key add -
sudo apt update
sudo apt install llvm-12
sudo apt install clang
sudo update-alternatives --install \
    /usr/bin/llvm-config       llvm-config      /usr/bin/llvm-config-12  200
make
```

#### Install ols

```sh
git clone https://github.com/DanielGavin/ols
cd ols
source build.sh
```

#### Ols config

```json
{
  "collections": [{ "name": "core", "path": "/home/user/Odin/core" }],
  "thread_pool_count": 4,
  "enable_semantic_tokens": false,
  "enable_document_symbols": true,
  "enable_hover": true,
  "enable_format": true,
  "enable_snippets": true,
  "formatter": {
    "tabs": false,
    "characters": 90
  }
}
```

#### Setup neoclide with ols

```json
{
  "languageserver": {
    "odin": {
      "command": "ols",
      "filetypes": ["odin"],
      "rootPatterns": ["/home/user/ols.json"]
    }
  }
}
```

### Nim

```sh
curl https://nim-lang.org/choosenim/init.sh -sSf | sh
# add 'export PATH=$PATH:$HOME/.nimble/bin' to the .zshrc file
```

### Kotlin

```sh
sudo apt update
sudo apt install default-jdk
sudo apt install zip unzip -y
curl -s https://get.sdkman.io | bash
sdk install kotlin
```

## Zsh

### Zsh

```sh
sudo apt install zsh -y

# set shell to zsh
chsh -s $(which zsh)

```

## Neovim

### Neovim

```sh
curl -LO https://github.com/neovim/neovim/releases/download/nightly/nvim.appimage
chmod u+x nvim.appimage
./nvim.appimage
mkdir -p ~/bin
mv ./nvim.appimage ~/bin/nvim.appimage
```

### VimPlug

```sh
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```

And run `:PlugInstall`

### Neoclide extensions

```
:CocInstall coc-marketplace coc-yaml coc-vimlsp coc-tsserver coc-tslint coc-toml coc-rust-analyzer coc-pyright coc-prettier coc-pairs coc-json
```

## Vscode

### Plugins

```sh
code --install-extension bungcip.better-toml
code --install-extension formulahendry.code-runner
code --install-extension smugller.c-go-syntax-highlighter-pros
code --install-extension leonardssh.vscord
code --install-extension editorconfig.editorconfig
code --install-extension irongeek.vscode-env
code --install-extension dbaeumer.vscode-eslint
code --install-extension file-icons.file-icons
code --install-extension github.copilot
code --install-extension github.vscode-pull-request-github
code --install-extension eamodio.gitlens
code --install-extension davidwang.ini-for-vscode
code --install-extension ritwickdey.liveserver
code --install-extension magicstack.magicpython
code --install-extension yzhang.markdown-all-in-one
code --install-extension davidanson.vscode-markdownlint
code --install-extension mateushenriquenascimentosoares.mit-license-generator
code --install-extension kosz78.nim
code --install-extension danielgavin.ols
code --install-extension esbenp.prettier-vscode
code --install-extension ms-python.vscode-pylance
code --install-extension ms-python.python
code --install-extension ms-vscode-remote.remote-containers
code --install-extension ms-vscode-remote.remote-ssh
code --install-extension ms-vscode-remote.remote-ssh-edit
code --install-extension ms-vscode-remote.remote-wsl
code --install-extension matklad.rust-analyzer
code --install-extension foxundermoon.shell-format
code --install-extension tyriar.sort-lines
code --install-extension alexcvzz.vscode-sqlite
code --install-extension beastmatser.ti-basic-autocomplete
code --install-extension xadillax.viml
code --install-extension redhat.vscode-yaml
```
