# inwx\_update\_dyndns

A python script which checks at regular intervals if your IPs (IPv4 and IPv6) have changed. If changes are
detected, an HTTP POST request is sent to inwx.com in order to update the A and AAAA record.
To use this script, you need to have created at least one DynDNS account on [inwx.com](https://www.inwx.com).


# Configuration

The script expects a TOML file `/etc/inwx_update_dyndns.toml` where your credentials are set. Have a look at the
[example file](example_config.toml), which should be self-explanatory. At the very least, you need to
update the username and password for the `[[account]]`. If you don't have an IPv6, `ipv6_enabled` should be set to `false`.


# Requirements

* [requests](https://pypi.python.org/pypi/requests)
* [toml](https://pypi.python.org/pypi/toml)


# Installation

For ArchLinux, a package is available on [AUR](https://aur.archlinux.org/packages/inwx_update_dyndns-git).
