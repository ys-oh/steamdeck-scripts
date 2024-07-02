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
sudo cat << EOF > /etc/containers/registries.conf.d/99-dockerio.conf
[registries.search]
registries = ['docker.io']
EOF
```
