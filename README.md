# steamdeck-scripts

## desktop mode first step!

**set user password**
```
passwd $USER
```

**enable steamos filesystem**
```bash
sudo steamos-readonly enable
```

**initiailize package manager**
```bash
sudo pacman-key --init
sudo pacman-key --populate archlinux
sudo pacman-key --populate holo
```

## Install Recommanded Packages

- openssh
- text editor (vi)

```bash
sudo pacman -S openssh vi
```

## add docker registry in Podman
Under `/etc/containers/` there is a file called `registries.conf`. It is complemented by `man 5 containers-registries.conf`.

```bash
# vi /etc/containers/registries.conf
...
[registries.search]
registries = ['docker.io']
...
```

## Setup Python Environment

install pip
```bash
sudo pacman -S python-pip
```

then, if error message ('externally-managed-environment') is occured,

```bash
# remove file
sudo rm /usr/lib/python3.11/EXTERNALLY-MANAGED
```


## Setup Gstreamer Enviroments

```
sudo pacman -S \
  gstreamer \
  gst-libav ffmpeg \
  gst-plugins-bad gst-plugins-good gst-plugins-bad
```
