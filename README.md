# Ansible Collection - alxndr42.commons

Basic infrastructure for Debian-based servers.

## basics

Basic system configuration.

Installs a more secure SSH configuration and configures unattended upgrades.
Security updates provided by the distribution will always be installed,
non-security updates can optionally be allowed.

Please see [roles/basics/README.md](roles/basics/README.md) for details.

## certbot

Installs [certbot](https://eff-certbot.readthedocs.io/).

Required variables:

| Variable | Description |
| --- | --- |
| `certbot_email` | Contact email. |

Please see [roles/certbot/README.md](roles/certbot/README.md) for details.

## golang

Installs [Go](https://go.dev/) for system-wide use.

Please see [roles/golang/README.md](roles/golang/README.md) for details.

## nginx

Installs [nginx](https://nginx.org/docs/).

Please see [roles/nginx/README.md](roles/nginx/README.md) for details.

## License

GNU General Public License v3 or later (GPLv3+)
