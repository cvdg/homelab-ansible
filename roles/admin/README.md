# Setup traefik

## Setup `admin_user`

Give `admin_user` access to `docker.socket`

```shell
$ systemctl --user enable podman.socket
$ systemctl --user start podman.socket
$ systemctl --user status podman.socket
...
export DOCKER_HOST=unix:///run/user/$(id -u)/podman/podman.sock
```


## Store CloudFlare secret

```shell
$ printf **************************************** | podman secret create cf_dns_api_token -
cca470e31b5334e1898f79c21
$ podman secret ls
ID                         NAME              DRIVER      CREATED        UPDATED
cca470e31b5334e1898f79c21  cf_dns_api_token  file        7 seconds ago  7 seconds ago
```
