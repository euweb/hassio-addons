# Home Assistant Add-on: VPNC Client

## About

This add-on provides a vpn connection to a network using [vpnc](https://man.archlinux.org/man/vpnc.8.en)


[![Open this add-on in your Home Assistant instance.][addon-badge]][addon]
## Configuration

```yaml
options:
  debug: 0
  vpn-server:
    gateway:
    ID:
    secret:
    username:
    password:
  ping:
    server:
    wait: 60 
```

### debug

Debug level (0,1,2,99) of the vpn connection.

### vpn-server

Connection configuration to the VPN server

### ping

Host to ping inside the VPN after the connection was established. Option _wait_ defines how many seconds to wait between pings. If ping fails reconnection is initiated. This is nessesary if after couple of hours the connection is dropped by VPN server.

**Note**: _Remember to restart the add-on when the configuration is changed._

[addon-badge]: https://my.home-assistant.io/badges/supervisor_addon.svg
[addon]: https://my.home-assistant.io/redirect/supervisor_addon/?repository_url=https%3A%2F%2Fgithub.com%2Feuweb%2Fhassio-addons&addon=47267a49_vpnc_client