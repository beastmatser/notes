# Python

First install all tools necessary to build Python.

```sh
sudo apt install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl \
git
```

The install pyenv and clone in it into any folder you like, here it will clone into a directory called `~/.pyenv`.

```sh
git clone https://github.com/pyenv/pyenv.git ~/.pyenv
```

Lastly, install any version of Python you want to use, here I'm using Python 3.10.x.

```sh
pyenv install 3.10.x
```

And also don't forget to set a global python version.

```sh
pyenv global 3.10.x
```
