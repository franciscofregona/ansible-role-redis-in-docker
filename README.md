# ansible-role-redis-in-docker

Forked from novomatic-tech/ansible-role-redis-in-docker to create a cluster of containers for the Redis service.

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
   redis_port: 6379
   redis_persistence_enabled: true
   redis_persistence_path: "/redis/data"
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

The original role was created in 2019 for the purposes of Novomatic Technologies Poland.

Modified for a technical test by [Francisco Fregona](franciscofregona@gmail.com).