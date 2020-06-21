# stack-graylog
Gl, Elastic, Mongo e Nginx-TLS in Docker Swarm

- Elasticsearch
Set vm.max_map_count to at least 262144edit
The vm.max_map_count kernel setting must be set to at least 262144 for production use.

How you set vm.max_map_count depends on your platform:
The vm.max_map_count setting should be set permanently in /etc/sysctl.conf:

grep vm.max_map_count /etc/sysctl.conf
vm.max_map_count=262144

To apply the setting on a live system, run:
sysctl -w vm.max_map_count=262144
