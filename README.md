# Ahauser31's build of dwm - the suckless tiling window manager

The [dwm](https://dwm.suckless.org/) window manager with all the patches applied that make it useful for me.

## Patches and features

- tbd

## Installation

```
git clone https://github.com/ahauser31/dwm-ahauser31
cd dwm-ahauser31
git checkout merged
sudo make install
```

## Please install `libxft-bgra`!

This build of dwm does not block color emoji in the status/info bar, so you must install [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/) from the AUR, which fixes a libxft color emoji rendering problem, otherwise dwm will crash upon trying to render one. Hopefully this fix will be in all libxft soon enough.


## Please edit sudoers file!

The sudoers file has to be edited in include keeping the HOME environment variable

```
sudo visudo
Defaults env_keep += "HOME"
```


