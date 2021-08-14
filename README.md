# Docker Compose Stacks

Docker compose stacks ready to use

## Kafka

Sets up the following deployment:

|Container|Ports container -> host|Image repository         |
|---------|-----------------------|-------------------------|
|Zookeeper|2181 -> 2181           |confluentinc/cp-zookeeper|
|Broker   |9092 -> 9092           |confluentinc/cp-kafka    |
|Kafka UI |8080 -> 8080           |provectuslabs/kafka-ui   |

```sh
# Start kafka cluster
docker-compose -f kafka.yml up -d

# Stop kafka cluster
docker-compose -f kafka.yml down
```

## ElasticStack

Sets up the following deployment:

|Container    |Ports container -> host|Image repository                             |
|-------------|-----------------------|---------------------------------------------|
|Elasticsearch|9200 -> 9200           |docker.elastic.co/elasticsearch/elasticsearch|
|Kibana       |5601 -> 5601           |docker.elastic.co/kibana/kibana              |

```sh
# Start elasticstack cluster
docker-compose -f elasticstack.yml up -d

# Stop elasticstack cluster
docker-compose -f elasticstack.yml down
```
