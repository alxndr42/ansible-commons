# Ansible Collection - alxndr42.commons

Common Ansible roles for Debian-based servers.

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

## nginx

Installs [nginx](https://nginx.org/docs/).

Please see [roles/nginx/README.md](roles/nginx/README.md) for details.

## nodejs

Installs [NodeJS](https://nodejs.org/).

Required variables:

| Variable | Description |
| --- | --- |
| `nodejs_version` | NodeJS [repository](https://github.com/nodesource/distributions#manual-installation) version. |

Please see [roles/nodejs/README.md](roles/nodejs/README.md) for details.

## php

Installs [PHP](https://www.php.net/) with FPM.

Required variables:

| Variable | Description |
| --- | --- |
| `php_version` | PHP package version. |

Please see [roles/php/README.md](roles/php/README.md) for details.

## License

GNU General Public License v3 or later (GPLv3+)
