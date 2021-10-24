# Installing on Debian
This will work on any distro based on Debian.

## Quick Install
You can download a bash script [here](https://github.com/Octonet45/quick-yggdrasil) and run it to install!

## Manual Install
This is how to install Yggdrasil manualy.

Step 1: Installing Packages

```
sudo apt-get install dirmngr
```

```
gpg --fetch-keys https://neilalexander.s3.dualstack.eu-west-2.amazonaws.com/deb/key.txt
gpg --export 569130E8CA20FBC4CB3FDE555898470A764B32C9 | sudo apt-key add -```
```
```
echo 'deb http://neilalexander.s3.dualstack.eu-west-2.amazonaws.com/deb/ debian yggdrasil' | sudo tee /etc/apt/sources.list.d/yggdrasil.list
sudo apt update
sudo apt install Yggdrasil
```

Step 2: Configuration and Installing\

The configuration file will be made into `/etc/yggdrasil.conf/`.

To start Yggdrasil you will need to run `sudo systemctl enable yggdrasil` and `sudo systemctl start yggdrasil`.\
If you want to reload the configuration file run `sudo systemctl reload yggdrasil` or `sudo systemctl restart yggdrasil`.
