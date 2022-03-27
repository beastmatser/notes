# Install scripts

- [Programming languages](#programming-languages)
- [Zsh](#zsh)
- [Neovim](#neovim)
- [Vscode](#vscode)

## Programming Languages

### Python

```sh
sudo apt update
sudo apt upgrade -y
sudo apt install software-properties-common -y
sudo add-apt-repository ppa:deadsnakes/ppa -y
sudo apt update
sudo apt install python3.10 -y
sudo apt install python3.9 -y
sudo apt install python3.8 -y
sudo apt install python3.7 -y
sudo apt install python3.6 -y

# Install venv for python3.10
sudo apt install python3.10-venv -y
mkdir ~/.venv
```

### Javascript

```sh
curl -sL https://deb.nodesource.com/setup_17.x | sudo -E bash
sudo apt install nodejs -y

# Install yarn
sudo npm install -g yarn
```

### Rust

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
# Install a complete toolchain
sudo apt-get update
sudo apt install build-essential -y
```

### Odin

Odin has some more tools to configure, click [here](odin.md) for a more precise guide.

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

### Zsh and oh-my-zsh

```sh
sudo apt install zsh -y

# set shell to zsh
chsh -s $(which zsh)

# Install oh-my-zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

```

### Plugins

```sh
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```

## Neovim

### Neovim

1. Go to [releases](http://github.com/neovim/neovim/releases) on the neovim repository
2. Download `nvim.appimage`
3. Run to fully install neovim:

```sh
chmod u+x nvim.appimage && ./nvim.appimage
# export PATH="$PATH:$HOME/bin" must be added in the .zshrc file
mkdir -p ~/bin
mv nvim.appimage ~/bin/nvim
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

