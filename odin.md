# Setting up Odin and ols

## Install Odin

```sh
git clone https://github.com/odin-lang/Odin
cd Odin
printf "deb http://apt.llvm.org/xenial/ llvm-toolchain-xenial-12 main" |sudo tee /etc/apt/sources.list.d/llvm-toolchain-xenial-12.list
wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key |sudo apt-key add -
sudo apt update
sudo apt install llvm-12
sudo apt install clang
make
```

## Install ols

```sh
git clone https://github.com/DanielGavin/ols
cd ols
source build.sh
```

### Ols config

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

### Setup neoclide with ols

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
