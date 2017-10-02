Role Name
=========

Installs Docker Daemon and [optionally] configures HTTP proxy for the daemon.
On RHEL family, OS provided Docker is installed.
On Ubuntu, docker 1.12 is installed (the one recommended by Kubernetes community).

Requirements
------------

None

Role Variables
--------------

    # Proxy variables
    docker_http_proxy: none
    docker_https_proxy: none
    docker_no_proxy: none
    docker_insecure_registry: none

The variables are optional. If they are not defined, the role will not configure proxy for the Docker daemon.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: solval.docker , http_proxy: http://myproxy.company.io:986  }

License
-------

Apache 2.0

Author Information
------------------

Jakub Dlugolecki
