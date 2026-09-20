# vim-X11

`gvim`, the X11 and Wayland GUI of Vim.

This sysext can be installed alongside the `vim` sysext, which provides the
terminal version.

## How to use

A sysext can only provide files under `/usr`, so the global vimrc shipped by
the Fedora package is available under `/usr/etc` and has to be copied to `/etc`
to be picked up:

```
$ sudo cp -a /usr/etc/vimrc /etc/
```

## Compatibility

This sysext should be compatible with all Fedora variants (CoreOS, Atomic
Desktops, etc.) but has only been tested on Atomic Desktops.
