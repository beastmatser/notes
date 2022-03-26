# Install scripts

- [Programming languages](#programming-languages)
- [Zsh](#zsh)
- [Neovim](#neovim)

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

```sh
git clone https://github.com/odin-lang/Odin
cd Odin
printf "deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial-12 main" |sudo tee /etc/apt/sources.list.d/llvm-toolchain-xenial-12.list
wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key |sudo apt-key add -
sudo apt update
sudo apt install llvm-11
sudo apt install clang
make
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

1. Go to [releases](http://github.com/neovim/neovim/releases]) on the neovim repository
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
