[![Build Status](https://travis-ci.org/novomatic-tech/ansible-role-redis-in-docker.svg?branch=master)](https://travis-ci.org/novomatic-tech/ansible-role-redis-in-docker) [![License](https://img.shields.io/badge/license-Apache%202-green.svg)](https://github.com/novomatic-tech/ansible-role-redis-in-docker/blob/master/LICENSE) [![Ansible Role Name](https://img.shields.io/ansible/role/42270.svg)](https://galaxy.ansible.com/novomatic-tech/kafka_in_docker) [![Ansible Role counter](https://img.shields.io/ansible/role/d/42270.svg)](https://galaxy.ansible.com/novomatic-tech/kafka_in_docker)
# ansible-role-redis-in-docker
A role to install and configure the Redis base on official containers and some community containers.
The role is used in our organization for different testing purposes and demo environments.


Role Variables
--------------

All default variables are predefined in [defaults/main.yml](defaults/main.yml).


Example Playbook
----------------

Example playbook usage:

```
- hosts: ubuntu18
  vars:
   redis_monitoring_enabled: true
   redis_port: 6379
   redis_password: "password"
   redis_persistence_enabled: true
   redis_persistence_path: "/redis/data"
   redis_compose_files_path: "/etc/compose-files"
   ansible_become: yes
  roles:
    - geerlingguy.docker
    - ansible-role-redis-in-docker
```

License
-------

Apache 2.0

Author Information
------------------

This role was created in 2019 for the purposes of Novomatic Technologies Poland.

