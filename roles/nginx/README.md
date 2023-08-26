# nginx

Installs [nginx](https://nginx.org/docs/).

The script [`nginx-site`](files/nginx-site) creates, enables and disables sites
using the included [template](files/nginx/sites-available/template).

## Variables

| Variable | Description |
| --- | --- |
| `nginx_access_log` | `access_log` value for *nginx.conf*. |
| `nginx_bad_user_agents` | List of `User-Agent` [map patterns][] to block. |
| `nginx_ciphers` | `ssl_ciphers` value for *nginx.conf*. |
| `nginx_curves` | `ssl_ecdh_curve` value for *nginx.conf*. |
| `nginx_default_site` | Configure/remove the `default` site (with ACME webroot). |
| `nginx_error_log` | `error_log` value for *nginx.conf*. |
| `nginx_packages` | Packages to install. |
| `nginx_worker_connections` | `worker_connections` value for *nginx.conf*. |
| `nginx_worker_processes` | `worker_processes` value for *nginx.conf*. |
| `acme_webroot` | Path of the `webroot` directory. |
| `openssl_ciphersuites` | `Ciphersuites` value for *openssl.cnf*. |

Please see [defaults/main.yml](defaults/main.yml) for default values.

[map patterns]: https://nginx.org/en/docs/http/ngx_http_map_module.html#map
