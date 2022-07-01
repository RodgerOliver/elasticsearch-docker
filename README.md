# EK stack (Elasticsearch and Kibana)

## Instructions

```sh
# configure kernel
sudo vim /etc/sysctl.conf
> vm.max_map_count=262144
sysctl -w vm.max_map_count=262144

# navigate to localhost:5601
# generate kibana token
docker-compose exec elasticsearch bin/elasticsearch-create-enrollment-token -s kibana
# generate the verification code for kibana
docker-compose exec kibana bin/kibana-verification-code
# generate the password for elastic
docker-compose exec elasticsearch bin/elasticsearch-reset-password -u elastic
```

## References

- [Set Password and user with Docker-compose](https://discuss.elastic.co/t/set-password-and-user-with-docker-compose/225075)
- [Oficial Kibana](https://www.elastic.co/guide/en/kibana/8.3/docker.html)
- [Oficial Elasticsearch](https://www.elastic.co/guide/en/elasticsearch/reference/8.3/docker.html)
- [Linux prerequisites](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html#docker-prod-prerequisites).
- [Docker Compose Example 1](https://github.com/shazforiot/Elasticsearch-logstash-Kibana-Docker-Compose/blob/main/docker-compose.yml)
- [Docker Compose Example 2](https://github.com/justmeandopensource/elk/blob/master/docker/docker-compose-v7.9.2.yml)
