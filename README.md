# EK stack (Elasticsearch and Kibana)

> [Oficial Elasticsearch](https://www.elastic.co/guide/en/elasticsearch/reference/8.3/docker.html)
>
> [Oficial Kibana](https://www.elastic.co/guide/en/kibana/8.3/docker.html)
>
> If there are any errors with Elasticsearch see [this](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html#docker-prod-prerequisites).
>
> [Docker Compose 1](https://github.com/justmeandopensource/elk/blob/master/docker/docker-compose-v7.9.2.yml)
>
> [Docker Compose 2](https://github.com/shazforiot/Elasticsearch-logstash-Kibana-Docker-Compose/blob/main/docker-compose.yml)
>
> The drive needs to have at least 10GB of free space for the elasticsearch container to start.

## Instructions

```sh
# configure kernel
sudo vim /etc/sysctl.conf
> vm.max_map_count=262144
sysctl -w vm.max_map_count=262144

# navigate to localhost:5601
# generate kibana token
docker-compose exec elasticsearch bin/elasticsearch-create-enrollment-token --scope kibana
# generate the verification code for kibana
docker-compose exec kibana bin/kibana-verification-code
# generate the password for elastic
docker-compose exec elasticsearch bin/elasticsearch-reset-password -u elastic

```
