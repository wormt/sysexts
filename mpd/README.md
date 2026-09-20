# mpd

## How to use

The configuration shipped by Fedora package is available under `/usr/etc` must be copied to `etc`:

```bash
sudo cp -a /usr/etc/mpd.conf /etc/
```

The `mpd` user, its runtime directory and its state directory also have to be
created:

```bash
sudo systemd-sysusers
sudo systemd-tmpfiles --create
sudo mkdir -p /var/lib/mpd/music /var/lib/mpd/playlists
sudo chown -R mpd:mpd /var/lib/mpd
sudo systemctl enable --now mpd
```

## Compatibility

This sysext is compatible with all Fedora variants (CoreOS, Atomic Desktops, etc.).
