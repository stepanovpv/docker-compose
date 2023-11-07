Мониторинг хоста:
- prometheus
- node-exporter
- grafana

Мониторинг контейнеров:
- portainer

Конфигурация:
- prometheus/prometheus.yaml

Запуск:

**Ubuntu:**
```
sudo apt update -y && \
sudo apt install docker docker-compose git -y && \
git clone https://github.com/stepanovpv/docker-compose && \
cd docker-compose && \
sudo systemctl start docker && \
sudo systemctl enable docker && \
sudo docker-compose up -d
```


**CentOS, REDOS:**
```
sudo dnf update -y && \
sudo dnf install docker-ce docker-compose git -y && \
git clone https://github.com/stepanovpv/docker-compose && \
cd docker-compose && \
sudo systemctl start docker && \
sudo systemctl enable docker && \ 
sudo docker-compose up -d
```

Запущенные сервисы:
- http://<IP хоста>:3000 - grafana
- http://<IP хоста>:9090 - prometheus
- http://<IP хоста>:9000 - portainer

В grafana, при первом запусе, поменять пароль (креды по умолчанию admin/admin), добавить источник данных Prometheus (обязательно указать хостовой IP) и импортировать дашборд node exporter 1860.
 
В portainer поменять креды по умолчанию и добавить Environment (local).
