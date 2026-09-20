# qemu-user-static

Static QEMU user mode emulators and their `binfmt_misc` registration files, to
transparently run binaries built for another architecture.

## How to use

The `systemd-binfmt` service reads `/usr/lib/binfmt.d` at every boot, so the
registrations provided by this sysext are applied on the next boot. To apply
them without rebooting:

```
$ sudo systemctl restart systemd-binfmt.service
```

## Compatibility

This sysext should be compatible with all Fedora variants (CoreOS, Atomic
Desktops, etc.) but has only been tested on Atomic Desktops.
