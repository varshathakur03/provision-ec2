docker
======

[![Build Status](https://travis-ci.org/dstanek/ansible-role-docker.svg?branch=master)](https://travis-ci.org/dstanek/ansible-role-docker)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-dstanek.docker-blue.svg)](https://galaxy.ansible.com/dstanek/docker/)

A simple role to install docker-engine and run the docker service. I'm just automating the installation steps from the [official Docker documentaton](https://docs.docker.com/engine/installation).

Requirements
------------

None

Role Variables
--------------

An optional list of users that should be added to the docker group. The default is the local username of the user running Ansible.

    docker_users:
      - username

Dependencies
------------

None

Example Playbook
----------------

Install and run docker using the defaults

    - hosts: servers
      roles:
         - dstanek.docker

Install and run docker with a custom user list

    - hosts: servers
      roles:
         - role: dstanek.docker
           docker_users:
             - david
             - tracy

License
-------

Apache 2.0

Author Information
------------------

David Stanek <dstanek@dstanek.com>
http://traceback.org
