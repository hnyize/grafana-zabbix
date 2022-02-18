# grafana-zabbix
 grafana with zabbix plugin preinstalled
 
 
docker build \
  --build-arg "GRAFANA_VERSION=latest" \
  --build-arg "GF_INSTALL_PLUGINS=grafana-clock-panel,alexanderzobnin-zabbix-app,marcusolsson-csv-datasource" \
  -t grafana-zabbix -f Dockerfile .

docker run -d -p 3000:3000 --name=grafana grafana-custom