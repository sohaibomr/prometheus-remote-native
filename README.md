# prometheus-remote-native

Introduction
============
A small repo to verify Prometheus(v2.11.1) Remote Read &amp; Write Natively in InfluxDB(1.7.7).

Spin-up Application
======
* Start Prometheus, InfluxDB, nodeexporter.
```
$ docker-compose up
```
This should now bring up these docker containers-
```
$ docker ps
CONTAINER ID        IMAGE                        COMMAND                  CREATED             STATUS              PORTS                                      NAMES
b57b324fa6b2        prom/prometheus:v2.11.1      "/bin/prometheus --c…"   6 seconds ago       Up 5 seconds                                                   prometheus
31c56ec6114d        prom/node-exporter:v0.18.1   "/bin/node_exporter …"   6 seconds ago       Up 6 seconds                                                   nodeexporter
bc86ee71238a        influxdb:1.7.7               "/entrypoint.sh infl…"   6 seconds ago       Up 6 seconds                                                   influxdb
```


* Prometheus is now hosted on [localhost:9090](localhost:9090).



Refference
======
1. [https://www.influxdata.com/blog/influxdb-now-supports-prometheus-remote-read-write-natively/](https://www.influxdata.com/blog/influxdb-now-supports-prometheus-remote-read-write-natively/)
2. [https://github.com/gdmello/prometheus-remote-storage](https://github.com/gdmello/prometheus-remote-storage)

**Note:** If prometheus gives error "can not load config from /tmp/prometheus" delete docker volume ``` docker volume prune ``` and restart.
