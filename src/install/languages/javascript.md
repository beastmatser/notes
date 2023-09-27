# Javascript

Using the installation script at [github.com/nodesource/distributions](https://github.com/nodesource/distributions#installation-instructions).

Download and import the Nodesource GPG key.

```sh
sudo apt-get update
sudo apt-get install -y ca-certificates curl gnupg
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://deb.nodesource.com/gpgkey/nodesource-repo.gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/nodesource.gpg
```

Create deb repository

```
set NODE_MAJOR 20
echo "deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_$NODE_MAJOR.x nodistro main" | sudo tee /etc/apt/sources.list.d/nodesource.list
```

Run Update and Install

```
sudo apt-get update
sudo apt-get install nodejs -y
```

Both of these npm replacements are useful for installing packages, install either pnpm or yarn.

```sh
# yarn
sudo npm install -g yarn
# pnpm
sudo npm install -g pnpm
```
