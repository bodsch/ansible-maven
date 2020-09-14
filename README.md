# ansible role to install maven




## Example Playbook

```
 - hosts: all
   roles:
     - { role: maven, maven_release: 3.6.3 }
```

## Role Variables

[defaults/main.yml](defaults/main.yml)

|*Variable*  | *Default Value* | *Description* |
| --- | --- | --- |
| `maven_cleanup` | `false` | clean temporary directory after installation  |
| `maven_version` | `3.6.3` | Version number|
| `maven_home_parent_directory` | `/opt` | MAVEN_HOME parent directory |
| `maven_mirror` | `http://mirror.23media.de/apache` | default mirror (see https://maven.apache.org/download.cgi) |
| `maven_download_username` | `''` |see ansible [get_url](http://docs.ansible.com/ansible/latest/get_url_module.html) url_username option|
| `maven_download_password` | `''` |see ansible [get_url](http://docs.ansible.com/ansible/latest/get_url_module.html) url_password option|


## Tests

```
tox -e py37-ansible29 -- molecule test
```
