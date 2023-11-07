Мониторинг хоста:
- prometheus
- node-exporter
- grafana

Мониторинг контейнеров:
- protainer

Конфигурация:
- prometheus/prometheus.yaml

Запуск:

- Ubuntu:
   sudo apt install docker docker-compose git -y
   git clone https://github.com/stepanovpv/docker-compose
   cd docker-compose
   sudo docker-compose up -d

-CentOS, REDOS
  sudo dnf install docker docker-compose git -y \
  git clone https://github.com/stepanovpv/docker-compose \
  cd docker-compose \
  sudo docker-compose up -d

Запущенные сервисы:
- http://<IP хоста>:3000 - grafana
- http://<IP хоста>:9090 - prometheus
- http://<IP хоста>:9000 - portainer
