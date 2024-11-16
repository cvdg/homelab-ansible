
Give `admin_user` access to `docker.socket`

```shell
$ systemctl --user enable podman.socket
$ systemctl --user start podman.socket
$ systemctl --user status podman.socket
...
export DOCKER_HOST=unix:///run/user/$(id -u)/podman/podman.sock
```
