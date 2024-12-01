# Arch Darwin Plymouth Theme Default and Coloured

## Installation


Copy the  theme to /usr/share/plymouth/themes:

```shell
sudo cp -r <folder-name>/usr/share/plymouth/themes
```
## Installation Examples

### Ubuntu/Linux Mint/Tuxedo OS
```shell
sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/logo-mac-style/logo-mac-style.plymouth 110
```
# Select the Theme

```shell
sudo update-alternatives --config default.plymouth
```
# Rebuild the initial Ramdisk:
```shell
sudo update-initramfs -u -k all
```
### Debian/Arch Linux

# Please look, if the theme is recognized
```shell
sudo plymouth-set-default-theme -l
```
# Apply the theme
```shell
sudo plymouth-set-default-theme -R <theme-name>
```
### Fedora

# Please look, if the theme  is recognized
```shell
sudo plymouth-set-default-theme -R <theme-name>
```    
# Rebuild the initrd
```shell
sudo dracut --regenerate-all -f
```
### Directory Structure

```
logo-mac-style/
├── images/
│   └── header-image.png
└── samples/
    └── [sample images]
```

Inspired from: https://www.pling.com/p/2112595 and https://github.com/ArmoredVortex/plymouth-theme-arch-darwin

