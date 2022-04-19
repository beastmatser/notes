# Javascript

Installing javascript is surprisingly easy.

First fetch a nodejs version, in this case we're using version 17.x.

```sh
curl -sL https://deb.nodesource.com/setup_17.x | sudo -E bash
```

Then you can install nodejs using the following command:

```sh
sudo apt install nodejs -y
```

Both of these npm replacements are useful for installing packages, install either pnpm or yarn.

```sh
# yarn
sudo npm install -g yarn
# pnpm
sudo npm install -g pnpm
```
