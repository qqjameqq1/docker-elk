# docker-elk
elasticsearch, logstash, kibana, filebeat, nginx on docker

## How to use
- Step 1. sudo sysctl -w vm.max_map_count=262144
- Step 2. chmod -R 0777 html/
- Step 3. chmod -R 0777 datas/
- Step 4. docker-compose up -d --build
