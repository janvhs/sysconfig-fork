# systemd-resolved DNS integration

Currently not handled by the existing DNS resolvers.

## Full Tunneling

Set VPN connections with

## Split Tunneling


## Debugging

resolvectl --cache=no query -4 "${DOMAIN}"
resolvectl --cache=no query -6 "${DOMAIN}"

or combine

ping -4 "${DOMAIN}"
ping -6 "${DOMAIN}"
with
tcpdump -ni any port 53
or less verbose
tcpdump -n -i any -Q out 'port 53 and not host 127.0.0.53'
