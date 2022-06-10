# apt-key-migrate

## Service for converting /etc/apt/trusted.gpg into individual keyrings in /usr/share/keyrings

### This is a fork of [mschmitt/apt-key-migrate](https://github.com/mschmitt/apt-key-migrate)

- Changed to use apt lists as recommended by debian [UseThirdParty](https://wiki.debian.org/DebianRepository/UseThirdParty)

- apt-key is deprecated and not supported at all in Ubuntu 22.04.

This script will convert the contents of /etc/apt/trusted.gpg to individual keys 
in /usr/share/keyrings.

A systemd unit that converts on bootup is included, but does not neccessarily 
have to be used.

### Download
```shell
git clone https://github.com/tmiland/apt-key-migrate.git
```
```shell
cd apt-key-migrate
```

### Usage

```shell
chmod +x apt-key-migrate
```
```shell
./apt-key-migrate
```

### Alternatively

```shell
sudo make install
```
```shell
sudo systemctl start apt-key-migrate.service
```

### TODO

- Add option to use Deb822 file format