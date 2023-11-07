# Promtail-Loki-Grafana-using-Docker-Compose
How to setup Grafana loki promtail using Docker compose

### Docker daemon settings
- Create a file in `/etc/docker/daemon.json` and add in the following config

```json
{
    "debug" : true,
    "log-driver": "loki",
    "log-opts": {
        "loki-url": "http://loki:3100/loki/api/v1/push",
        "loki-batch-size": "400"
    }
}```