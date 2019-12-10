# ansible-role-redis-in-docker

Forked from novomatic-tech/ansible-role-redis-in-docker, to create a Redis cluster service on Docker containers.

Role Variables
--------------

All default variables are predefined in [defaults/main.yml](defaults/main.yml).

redis_user: "redis"
redis_group: "redis"
redis_service_name: "redis"
redis_image: "redis:5.0.7"
redis_port: "6379"

** Set persistence to yes if done in the config file.**

redis_persistence_enabled: true
redis_persistence_path: "/redis/data"

Number of total containers to set up. Min 6, to have 3 masters and 1 replica for each one.
redis_no_containers: 6

Number of "copies" for every master node.
redis_no_replicas: 1
redis_config_file: "/redis/config/redis.conf"
redis_network_name: "redisnet"

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