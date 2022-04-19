# Odin

Installing [Odin](https://odin-lang.org/) requires some more steps.

First we'll start by cloning the repository and directly move into this newly created directory.

```sh
git clone https://github.com/odin-lang/Odin && cd Odin
```

Then we need to install some dependencies to build Odin. The last command will set the default llvm version to version 12.

```sh
sudo apt update
sudo apt install llvm-12
sudo apt install clang
sudo update-alternatives --install \
    /usr/bin/llvm-config       llvm-config      /usr/bin/llvm-config-12  200
```

Once that's done we can build Odin and don't forget to add the Odin folder to your path.

```sh
make
```

To get a better experience with Odin we will install the [Odin Language Server](https://github.com/DanielGavin/ols), or more commonly knows as ols.

```sh
git clone https://github.com/DanielGavin/ols && cd ols
```

Then build it.

```sh
./build.sh
```

Next replace the default ols.json file with a more configured version, something like this (replace `path` with the path to your Odin folder):

```json
{
  "collections": [
    {
      "name": "core",
      "path": "/home/user/Odin/core"
    }
  ],
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

Using neoclide we can add odin to the languageservers. (Launch the `coc-settings.json` file by using the following command in neovim: `:CocConfig`)

```json
{
  "languageserver": {
    "odin": {
      "command": "ols",
      "filetypes": ["odin"],
      "rootPatterns": ["/home/user/ols/ols.json"]
    }
  }
}
```
