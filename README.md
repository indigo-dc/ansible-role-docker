Docker Role
=========

Install docker-engine

Role Variables
--------------

- `docker_bridge_ip` : IP to be assigned to the docker bridge 

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: indigo-dc.docker, docker_bridge_ip: "172.0.17.1" }

License
-------

Apache Licence v2 [1]

[1] http://www.apache.org/licenses/LICENSE-2.0
