# mpd

The Music Player Daemon.

## How to use

A sysext can only provide files under `/usr`, so the configuration shipped by
the Fedora package is available under `/usr/etc` and has to be copied to `/etc`
to be picked up:

```
$ sudo cp -a /usr/etc/mpd.conf /etc/
```

The `mpd` user and its state directory also have to be created:

```
$ sudo systemd-sysusers
$ sudo mkdir -p /var/lib/mpd/music /var/lib/mpd/playlists
$ sudo chown -R mpd:mpd /var/lib/mpd
```

Then enable and start the service:

```
$ sudo systemctl enable --now mpd
```

## Compatibility

This sysext should be compatible with all Fedora variants (CoreOS, Atomic
Desktops, etc.) but has only been tested on Atomic Desktops.
