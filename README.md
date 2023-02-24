
# Ansible Role:  `maven`

Ansible role to install maven.


[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/bodsch/ansible-maven/main.yml?branch=main)][ci]
[![GitHub issues](https://img.shields.io/github/issues/bodsch/ansible-maven)][issues]
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/bodsch/ansible-maven)][releases]
[![Ansible Quality Score](https://img.shields.io/ansible/quality/50067?label=role%20quality)][quality]

[ci]: https://github.com/bodsch/ansible-maven/actions
[issues]: https://github.com/bodsch/ansible-maven/issues?q=is%3Aopen+is%3Aissue
[releases]: https://github.com/bodsch/ansible-maven/releases
[quality]: https://galaxy.ansible.com/bodsch/maven


## Operating systems

Tested on

* Arch Linux
* Debian based
    - Debian 10 / 11
    - Ubuntu 20.10

## Contribution

Please read [Contribution](CONTRIBUTING.md)

## Development,  Branches (Git Tags)

The `master` Branch is my *Working Horse* includes the "latest, hot shit" and can be complete broken!

If you want to use something stable, please use a [Tagged Version](https://github.com/bodsch/ansible-maven/tags)!


## Example Playbook

```
- hosts: all
  vars
     maven_release: 3.6.3
  roles:
    - role: maven
```

## Role Variables

[defaults/main.yml](defaults/main.yml)

| *Variable*                    | *Default Value*                   | *Description* |
| :---                          | :---                              | :--- |
| `maven_cleanup`               | `false`                           | clean temporary directory after installation  |
| `maven_version`               | `3.6.3`                           | Version number |
| `maven_home_parent_directory` | `/opt`                            | `MAVEN_HOME` parent directory |
| `maven_mirror`                | `http://mirror.23media.de/apache` | default mirror (see [maven.apache.org](https://maven.apache.org/download.cgi)) |
| `maven_download_username`     | `''`                              | see ansible [get_url](http://docs.ansible.com/ansible/latest/get_url_module.html) `url_username` option |
| `maven_download_password`     | `''`                              | see ansible [get_url](http://docs.ansible.com/ansible/latest/get_url_module.html) `url_password` option |


----

## Author and License

- Bodo Schulz

## License

[Apache](LICENSE)

**FREE SOFTWARE, HELL YEAH!**
