# Rust - Docker mod for code-server

This mod adds rustup to code-server, to be installed/updated during container start.

In openssh-server docker arguments, set an environment variable `DOCKER_MODS=linuxserver/mods:openssh-server-rsync`

If adding multiple mods, enter them in an array separated by `|`, such as `DOCKER_MODS=linuxserver/mods:code-server-rust|linuxserver/mods:code-server-mod2`

## Tips and tricks

* To decrease startup times when multiple mods are used, we have consolidated `apt-get update` down to one file. As seen in the [nodejs mod](https://github.com/linuxserver/docker-mods/tree/code-server-nodejs/root/etc/cont-init.d)
* Some images has helpers built in, these images are currently:
    * [Openvscode-server](https://github.com/linuxserver/docker-openvscode-server/pull/10/files)
    * [Code-server](https://github.com/linuxserver/docker-code-server/pull/95)
