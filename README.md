# homelab-ansible

Configure my homelab with `ansible`.

## dns01.griend.dev

```shell
$ raspinfo | head
System Information
------------------

Raspberry Pi 3 Model B Rev 1.2
PRETTY_NAME="Debian GNU/Linux 12 (bookworm)"
NAME="Debian GNU/Linux"
VERSION_ID="12"
VERSION="12 (bookworm)"

Raspberry Pi reference 2024-10-22
```

This is an old [Raspberry Pi 3b](https://www.raspberrypi.com/products/raspberry-pi-3-model-b/), its
age must be close to 10 years old.

With `nmtui` it is configured with a fixed IP address:

| Key             |  Value                    |
| :-------------- | :------------------------ |
| address:        | 192.168.2.128/24          |
| gateway:        | 192.168.2.254             |
| dns servers:    | 127.0.0.1
|                 | 192.168.2.17 (pihole on TrueNas) |
|                 | 192.168.2.254 (dns from router) |
| search domains: | griend.dev                |
