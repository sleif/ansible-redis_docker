sleif.redis_docker
============

This role runs redis in a Docker container.

Requirements
------------

Use it on a machine setup with ansible role sleif.docker.

Role Variables
--------------

- redis_container_name
- docker_network_name (can be defined in sleif.docker)

Dependencies
------------

Needs geerlingguy.docker to make sure Docker is available.
Needs sleif.docker to make sure Docker is configured as needed.

Example Playbook
----------------

    - hosts: "server"
      user: root
      vars:
        docker_network_name: 'custom_docker_network'
      roles:
        - { role: sleif.redis_docker, tags: "redis_docker",
                                      redis_container_name: "redis_for_cusom_service" }

License
-------

MIT

Author Information
------------------

Created in 2021 by Sebastian Berthold
