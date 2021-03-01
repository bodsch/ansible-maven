
ansible role to install maven


[![GitHub Workflow Status](https://img.shields.io/github/workflow/status/bodsch/ansible-maven/CI)][ci]
[![GitHub issues](https://img.shields.io/github/issues/bodsch/ansible-maven)][issues]
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/bodsch/ansible-maven)][releases]

[ci]: https://github.com/bodsch/ansible-maven/actions
[issues]: https://github.com/bodsch/ansible-maven/issues?q=is%3Aopen+is%3Aissue
[releases]: https://github.com/bodsch/ansible-maven/releases

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
| `maven_mirror`                | `http://mirror.23media.de/apache` | default mirror (see https://maven.apache.org/download.cgi) |
| `maven_download_username`     | `''`                              | see ansible [get_url](http://docs.ansible.com/ansible/latest/get_url_module.html) url_username option |
| `maven_download_password`     | `''`                              | see ansible [get_url](http://docs.ansible.com/ansible/latest/get_url_module.html) url_password option |


## Tests

```
$ tox -e py39-ansible29 -- molecule test
```
