# Logo Mac Style Plymouth Theme

Note: The Default Style is Arch Linux Styled "Only" Follow Instructions if you want custom image else just install

## Logo Customization

1) Please open the image "header-image.png" in your image editor (Gimp eg.)
2) Add your Logo to the project. Place your logo inside the black box (you may need to resize it).

The optional dimensions are:
square:           130px x 130px
rectangular:      244px x 130px

The sample images from the "samples"-folder can be used for comparison.
Everything below the black box should remain free. This space is used as a gap to the progress bar.
The black box (guide lines) can still remain in the picture as such.
The background of the Plymouth theme is black, so these "guide lines" are not visible.
But you can remove them if you wish. It's up to you to decide how you want it.

3) Save/Export the image as png with the file name "header-image.png"
4) Move your edited header-image.png file into the "images"-folder

## Installation

5) If we assume that the unzipped theme folder is located in your download directory:

Copy the finished theme to /usr/share/plymouth/themes:

cd ~/Downloads
sudo cp -r logo-mac-style /usr/share/plymouth/themes

## Installation Examples

### Ubuntu/Linux Mint/Tuxedo OS

sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/logo-mac-style/logo-mac-style.plymouth 110

# Select the Theme
sudo update-alternatives --config default.plymouth

# Rebuild the initial Ramdisk:
sudo update-initramfs -u -k all

### Debian/Arch Linux

# Please look, if the theme "logo-mac-style" is recognized
sudo plymouth-set-default-theme -l

# Apply the theme
sudo plymouth-set-default-theme -R logo-mac-style

### Fedora

# Please look, if the theme "logo-mac-style" is recognized
sudo plymouth-set-default-theme -R logo-mac-style

# Rebuild the initrd
sudo dracut --regenerate-all -f

### Directory Structure

```
logo-mac-style/
├── images/
│   └── header-image.png
└── samples/
    └── [sample images]
```

Credits: https://www.pling.com/p/2112595

