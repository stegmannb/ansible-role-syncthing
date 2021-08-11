# Ansible Template Role

[![License: MIT](https://img.shields.io/github/license/stegmannb/ansible-role-syncthing)](https://github.com/stegmannb/ansible-role-syncthing/blob/master/LICENSE)
![Continuous Integration](https://github.com/stegmannb/ansible-role-syncthing/workflows/Continuous%20Integration/badge.svg)
[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)](https://github.com/pre-commit/pre-commit)

## Requirements

This role expects a Debian based distribution.

## Role Variables

- `skip_unsupported_os` (Default: false): Skip the role if the host's OS is not supported.
- `syncthing_user` (Default: syncthing): The user running syncthing.
- `syncthing_address` (Default: 0.0.0.0:8384): The address Syncthing's web GUI is listining at.
- `syncthing_wait_for_zfs` (Default: false): If true the Syncthing systemd service waits for ZFS.
- `apt_cache_valid_time`: (Default: 0): Update the apt cache if it is older than the cache_valid_time. This option is set in seconds. [Ansible Documentation](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/apt_module.html#parameter-cache_valid_time)

## Example Playbook

    - hosts: servers
      roles:
         - role: stegmannb.syncthing

## License

MIT
