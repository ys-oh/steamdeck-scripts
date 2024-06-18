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

```
sudo pacman -S openssh vi
```
