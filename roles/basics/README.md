# basics

Basic system configuration.

Installs a more secure SSH configuration and configures unattended upgrades.
Security updates provided by the distribution will always be installed,
non-security updates can optionally be allowed.

## Variables

| Variable | Description |
| --- | --- |
| `basics_autoupdate_blocklist` | List of packages that must not be automatically updated. |
| `basics_autoupdate_mail` | Email address to send unattended upgrade errors to. |
| `basics_autoupdate_non_security` | Install non-security updates provided by the distribution. |
| `basics_autoupdate_origins` | List of additional `Origins-Pattern` values. |
| `basics_autoupdate_reboot` | Allow automatic reboots for unattended upgrades. |
| `basics_autoupdate_update_calendar` | `OnCalendar` value for *apt-daily.timer*. |
| `basics_autoupdate_update_delay` | `RandomizedDelaySec` value for *apt-daily.timer*. |
| `basics_autoupdate_upgrade_calendar` | `OnCalendar` value for *apt-daily-upgrade.timer*. |
| `basics_autoupdate_upgrade_delay` | `RandomizedDelaySec` value for *apt-daily-upgrade.timer*. |
| `basics_hostname` | System hostname. |
| `basics_history_disabled` | Disable persistent history in Bash etc. |
| `basics_journald_maxfile` | *journald.conf* `MaxFileSec` override. |
| `basics_journald_maxretention` | *journald.conf* `MaxRetentionSec` override. |
| `basics_journald_storage` | *journald.conf* `Storage` override. |
| `basics_microcode_updates` | Install CPU microcode updates. |
| `basics_packages_install` | List of packages that are always installed. |
| `basics_packages_remove` | List of packages that are always removed. |
| `basics_services_disable` | List of services that are always disabled. |
| `basics_ssh_listen` | List of `ListenAddress` values for *sshd_config*. |
| `basics_ssh_match_blocks` | List of `Match` blocks for *sshd_config* (see below). |
| `basics_ssh_port` | `Port` value for *sshd_config*. |
| `basics_ssh_root_login` | `PermitRootLogin` value for *sshd_config*. |

Please see [defaults/main.yml](defaults/main.yml) for default values.

## SSH Match Blocks

Example:

```yaml
basics_ssh_match_blocks:
  - match: User sftpuser
    options:
      - ForceCommand internal-sftp
```

Resulting entry in *sshd_config*:

```
Match User sftpuser
  ForceCommand internal-sftp
```
