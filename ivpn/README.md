# ivpn

IVPN daemon from IVPN's official repositories.

The service, the CLI and the systemd unit all come from the sysext, so it has
to be installed and enabled before anything below works.

## How to use

Install and enable it, for example with `sysexts-manager`:

```bash
sudo sysexts-manager add ivpn https://github.com/wormt/sysexts/releases/download
sudo sysexts-manager update
sudo sysexts-manager enable ivpn
sudo sysexts-manager refresh
```

Then create the directories the daemon wants start the service:

```bash
sudo systemd-tmpfiles --create
sudo systemctl start ivpn-service
sudo ivpn login
sudo ivpn connect -f
```

## Compatibility

This sysext is compatible with all Fedora variants (CoreOS, Atomic Desktops, etc.).
