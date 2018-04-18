# Telegraf Ansible role

This ansible role will install and configure telegraf on CentOS  and Debian systems

[Telegraf](https://github.com/influxdata/telegraf) is an agent written in Go for collecting, processing, aggregating, and writing metrics.

## How to use this role

All variables are stored on `defaults/main.yml``

Example Playbook:

```
$ cat telegraf.yml
---
- name: Install and configure telegraf
  remote_user: jmutai
  hosts: mysql-server-01
  become: yes
  become_method: sudo
  roles:
    - telegraf
```

Clone this repo to `./roles` directory, make modifications to role variables and execute it when done:

```
$ ansible-playbook -i hosts telegraf.yml
```


