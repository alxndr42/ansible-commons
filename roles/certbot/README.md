# certbot

Installs [certbot](https://eff-certbot.readthedocs.io/).

## Variables

Required variables:

| Variable | Description |
| --- | --- |
| `certbot_email` | Contact email. |

Optional variables:

| Variable | Description |
| --- | --- |
| `certbot_domains` | Domains to register certificates for. Items can be strings or lists of strings. |
| `certbot_packages` | Packages to install. |
| `certbot_rsa_key_size` | Number of RSA key bits. |
| `acme_webroot` | Path of the `webroot` directory. |

Please see [defaults/main.yml](defaults/main.yml) for default values.
