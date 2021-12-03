Docker Role
=========

Install docker-engine and optionally docker-compose

Role Variables
--------------

- `docker_bridge_ip_cidr` (optional): IP to be assigned to the docker bridge. Using standard CIDR notation, e.g. 192.168.1.5/24
- `docker_bridge_mtu` (optional): override the maximum packet length on docker0
- `docker_dns` (list, optional): override DNS servers to use
- `docker_dns_search` (list, optional): sets the domain names that are searched
- `docker_regitry_mirror`( optional): URL of the registry mirror to be configured
- `docker_storage_driver` (optional): Storage driver to use
- `docker_log_driver` (optional): Log driver to use. Default: 'json-file'
- `docker_logs_opts` (optional): Log driver options. Default: { 'max-file': '3', 'max-size': '100m' }
- `docker_pip_package` (optional): The name of the packge to install to get pip on the system. For older systems that don't have Python 3 available, you can set this to `python-pip`. Default: `python3-pip`
- `docker_compose_version` (optional): if provided, docker-compose will be installed with the requested version. Default: "", i.e. docker-compose is not installed by default.

Dependencies
--------------
- geerlingguy.pip

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: indigo-dc.docker, docker_bridge_ip_cidr: "172.0.17.1/24" }

License
-------

Apache Licence v2 [1]

[1] http://www.apache.org/licenses/LICENSE-2.0
