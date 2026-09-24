# ivpn

IVPN daemon from IVPN's official repositories.

## How to use

```bash
sudo systemd-tmpfiles --create
sudo systemctl start ivpn-service
sudo ivpn login
sudo ivpn connect -f
```

## Compatibility

This sysext is compatible with all Fedora variants (CoreOS, Atomic Desktops, etc.).
