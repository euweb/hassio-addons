# Home Assistant Add-on: VPNC Client

## Build and local run

```sh
docker run \
  --rm \
  -it \
  --name builder \
  --privileged \
  -v <PATH to the Addon>:/data \
  -v /var/run/docker.sock:/var/run/docker.sock:ro \
  homeassistant/amd64-builder \
  -t /data \
  --all \
  --test \
  -i vpnc-client-addon-amd64 \
  -d local
```

```sh
docker run -d --cap-add=NET_ADMIN --device /dev/net/tun -it -v <Path to plugin soure directory>:/data local/vpnc-client-addon-amd64:latest
```
