# redpanda-grafana
Docker Compose for Redpanda, Prometheus and Grafana

Sets up a three node Redpanda cluster with Prometheus for scraping metrics and Grafana for dashboards.
Requires `docker` and `docker-compose`.

## Instructions

```
git clone https://github.com/patrickangeles/redpanda-grafana
cd redpanda-grafana
docker compose up -d
```

To view your dashboard, go to http://localhost:3000/

To create a topic with 10 partitions and 3x replication:

```
docker exec redpanda1 rpk topic create mytopic -p 10 -r 3
```

## Cleanup

To shut down (run this command from the same working directory as before):

```
docker compose down
```
