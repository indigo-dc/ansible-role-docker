Docker Role
=========

Install docker-engine

Role Variables
--------------

- `docker_bridge_ip` : IP to be assigned to the docker bridge 
- `docker_mirror_host`: if defined, the role configures docker-engine with option --registry-mirror={{docker_mirror_protocol}}://{{docker_mirror_host}}:{{docker_mirror_port}}
- `docker_mirror_protocol`: default to "http"
- `docker_mirror_port`: default to 5000

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: indigo-dc.docker, docker_bridge_ip: "172.0.17.1" }

License
-------

Apache Licence v2 [1]

[1] http://www.apache.org/licenses/LICENSE-2.0
