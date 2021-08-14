# Docker Compose Stacks

Docker compose stacks ready to use

## Kafka

Sets up the following deployment:

|Container|Ports container -> host|Image repository         |
|---------|-----------------------|-------------------------|
|Zookeeper|2181 -> 2181           |confluentinc/cp-zookeeper|
|Broker   |9092 -> 9092           |confluentinc/cp-kafka    |
|Kafka UI |8080 -> 18080           |provectuslabs/kafka-ui   |

UI is available on <http://localhost:18080>

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

Open Kibana <http://localhost:5601>

```sh
# Start elasticstack cluster
docker-compose -f elasticstack.yml up -d

# Stop elasticstack cluster
docker-compose -f elasticstack.yml down
```

## Jaeger tracing

Sets up the following deployment:

|Container|Ports container -> host|Image repository        |
|---------|-----------------------|------------------------|
|Jaeger   |5775 -> 5775 / udp <br> 6831 -> 6831 / udp <br> 6832 -> 6832 / udp <br> 5778 -> 5778 <br> 16686 -> 16686 <br> 14268 -> 14268 <br> 14250 -> 14250 <br> 9411 -> 9411|jaegertracing/all-in-one|

UI is available on <http://localhost:16686>

```sh
# Start jaeger cluster
docker-compose -f jaeger.yml up -d

# Stop jaeger cluster
docker-compose -f jaeger.yml down
```
