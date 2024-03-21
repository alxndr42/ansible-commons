# pyenv

Installs [pyenv][].

Copies the [ensure-python](files/ensure-python) script to `/usr/local/bin`.

[pyenv]: https://github.com/pyenv/pyenv

## Variables

| Variable | Description |
| --- | --- |
| `pyenv_packages` | Required system packages for pyenv. |
| `pyenv_users` | List of usernames to install pyenv for. |
| `pyenv_users_create` | Whether to create missing users. |
| `pyenv_version` | Version of pyenv to check out. |

Please see [defaults/main.yml](defaults/main.yml) for default values.
