# stack-graylog
Graylog, Elastic, Mongo e Nginx-TLS in Docker Swarm

1. Set vm.max_map_count;
2. Put your certs and keys on nginx/ssl/;
3. Set server IP env GRAYLOG_HTTP_EXTERNAL_URI=http://192.168.1.196:9000/;
4. docker stack deploy -c docker-compose.yml graylog

## How set vm.max_count
- Elasticsearch
Set vm.max_map_count to at least 262144edit
The vm.max_map_count kernel setting must be set to at least 262144 for production use.

How you set vm.max_map_count depends on your platform:
The vm.max_map_count setting should be set permanently in /etc/sysctl.conf:

grep vm.max_map_count /etc/sysctl.conf
vm.max_map_count=262144

To apply the setting on a live system, run:
sysctl -w vm.max_map_count=262144
