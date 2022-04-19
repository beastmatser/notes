# Go

Go's installation process can be a bit tricky, but it's not too bad.

First we'll fetch version 1.18 of Go, of course you can use any version you want.

```sh
wget https://go.dev/dl/go1.18.linux-amd64.tar.gz
```

Then we'll extract it to the current directory.

```sh
tar -zxvf go1.18.linux-amd64.tar.gz
```

Lastly we'll move the binary to the `/usr/local/go` directory, and add it to your path variables. In some case you may need to add `/bin` to the path.

```sh
sudo mv go /usr/local/go
```
