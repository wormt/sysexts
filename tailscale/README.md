# tailscale

`tailscaled` and the `tailscale` client.

## How to use

A sysext can only provide files under `/usr` and can not enable services, so
`tailscaled` has to be enabled manually:

```
$ sudo systemctl enable --now tailscaled
```

Then connect the node to your tailnet:

```
$ sudo tailscale up
```

## Compatibility

This sysext should be compatible with all Fedora variants (CoreOS, Atomic
Desktops, etc.) but has only been tested on Atomic Desktops.
