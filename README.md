# Ansible Role: lxd-container

Simple role for creating lxd container and add sudo-user on RHEL/CentOS or Debian/Ubuntu servers.

## Requirements
---

* LXD >= 4.0
* Ansible >= 2.9
* Jinja2

## Role Variables
---

Available variables are listed below, along with default values (see `defaults/main.yml`):

* `image`: ubuntu/20.04  
  Image name, see [https://uk.lxd.images.canonical.com/](https://uk.lxd.images.canonical.com/)  

* `containers`: [image1]  
  List of containers for creating  

* `user`: vega  
  Name of sudo-user for creating   

## Dependencies
---

None.

## Example Playbook
---

    ---
    - hosts: localhost
      remote_user: user
      roles:
        - role: lxd-container
          vars:
            - user: user
            - image: "ubuntu/20.04"
            - containers:
              - testrole

## License
---

MIT / BSD

## Author Information
---

This role was created in 2022 by [Huongtx](https://github.com/trinhhuong244/) - Vega corp.
