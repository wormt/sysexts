# qemu

`qemu-kvm` and the QEMU system emulation modules, to run virtual machines with
KVM.

## How to use

A sysext can only provide files under `/usr`, so the configuration shipped by
the Fedora package is available under `/usr/etc` and has to be copied to `/etc`
to be picked up:

```
$ sudo cp -a /usr/etc/qemu /etc/
```

The `qemu` user and `kvm` group are created at boot by `systemd-sysusers` from
`/usr/lib/sysusers.d/qemu.conf`.

For a complete virtualization stack, install the `libvirtd` or
`libvirtd-desktop` sysext alongside this one.

## Compatibility

This sysext should be compatible with all Fedora variants (CoreOS, Atomic
Desktops, etc.) but has only been tested on Atomic Desktops.
