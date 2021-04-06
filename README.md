# Ahauser31's build of dwm - the suckless tiling window manager

The [dwm](https://dwm.suckless.org/) window manager with all the patches applied that make it useful for me.

## Patches and features

- basics (own patch, just some basic settings such as tuning of Makefile, etc)
- center
- coolautostart (good enough autostart method for me)
- decorationhints
- dwmc (extended for my config)
- emoji (own patch to allow colored emoji in dwm)
- fakefullscreen
- focusmaster
- focusonclick
- nokeyboardmousebar (own patch, strips out all support for keybindings and mousebindings apart from click focus and removes the in-built bar)
- pertag
- scratchpads (tuned to my liking)
- shiftview
- sizehints
- sticky (tuned, added issticky rule)
- swallow
- vanitygaps (tuned to my liking)
- xresources (load colors from xresources)
- xsessions (own patch to have an entry for dwm in the login manager)

## Installation

```
git clone https://github.com/ahauser31/dwm-ahauser31
cd dwm-ahauser31
git checkout merged_again
sudo make install
```

## Please install `libxft-bgra`!

This build of dwm does not block color emoji in the status/info bar, so you must install [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/) from the AUR, which fixes a libxft color emoji rendering problem, otherwise dwm will crash upon trying to render one. Hopefully this fix will be in all libxft soon enough.


## Please edit sudoers file!

The sudoers file has to be edited in include keeping the HOME environment variable in order for the installation of the sxhkdrc file to succeed

```
sudo visudo
Defaults env_keep += "HOME"
```


