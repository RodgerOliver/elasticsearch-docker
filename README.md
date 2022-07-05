# EK stack (Elasticsearch and Kibana)

[![version](https://img.shields.io/badge/Elasticsearch-8.3.1-FEC514)](https://www.elastic.co/elasticsearch)
[![version](https://img.shields.io/badge/Kibana-8.3.1-F04E98)](https://www.elastic.co/kibana)

## About

This project is a guide to start using the Elastic Stack with docker compose.

It can be run as a single node mode or as a multi-node cluster.

## Instructions

```sh
# configure kernel on linux
# If not on linux, check the reference 5
sudo vim /etc/sysctl.conf
> vm.max_map_count=262144
sysctl -w vm.max_map_count=262144

cp .env.example .env

docker-compose up -d
```

## References

- [Elastic on Docker Compose with Security](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html#docker-compose-file)
- [Set Password and user with Docker-compose](https://discuss.elastic.co/t/set-password-and-user-with-docker-compose/225075)
- [Oficial Kibana](https://www.elastic.co/guide/en/kibana/8.3/docker.html)
- [Oficial Elasticsearch](https://www.elastic.co/guide/en/elasticsearch/reference/8.3/docker.html)
- [System prerequisites](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html#docker-prod-prerequisites).

---

- [Docker Compose Example 1](https://github.com/shazforiot/Elasticsearch-logstash-Kibana-Docker-Compose/blob/main/docker-compose.yml)
- [Docker Compose Example 2](https://github.com/justmeandopensource/elk/blob/master/docker/docker-compose-v7.9.2.yml)
- [Docker Compose Example 3](https://github.com/shazforiot/Elasticsearch-logstash-Kibana-Docker-Compose/blob/main/docker-compose.yml)

---

- [Run ELK 8 on Docker with Auth](https://levelup.gitconnected.com/how-to-run-elasticsearch-8-on-docker-for-local-development-401fd3fff829)
- [ELK 8 on Docker Auth Error](https://stackoverflow.com/questions/71213784/unable-to-start-elastic-search-8-and-kibana-using-docker)
- [Impost CSV and Log Data On Kibana](https://www.elastic.co/blog/importing-csv-and-log-data-into-elasticsearch-with-file-data-visualizer)
