# Docker Compose Stacks

Docker compose stacks ready to use

```sh
# Switch to stack directory
cd <stack>

# Start stack
docker-compose up -d

# Stop stack
docker-compose down
```

## Kafka

Sets up the following deployment:

|Container|Ports container -> host|Image repository         |
|---------|-----------------------|-------------------------|
|Zookeeper|2181 -> 2181           |confluentinc/cp-zookeeper|
|Broker   |9092 -> 9092           |confluentinc/cp-kafka    |
|Kafka UI |8080 -> 18080           |provectuslabs/kafka-ui   |

> UI is available on <http://localhost:18080>
## ElasticStack

Sets up the following deployment:

|Container    |Ports container -> host|Image repository                             |
|-------------|-----------------------|---------------------------------------------|
|Elasticsearch|9200 -> 9200           |docker.elastic.co/elasticsearch/elasticsearch|
|Kibana       |5601 -> 5601           |docker.elastic.co/kibana/kibana              |

> Open Kibana <http://localhost:5601>

## Jaeger tracing

Sets up the following deployment:

|Container|Ports container -> host|Image repository        |
|---------|-----------------------|------------------------|
|Jaeger   |5775 -> 5775 / udp <br> 6831 -> 6831 / udp <br> 6832 -> 6832 / udp <br> 5778 -> 5778 <br> 16686 -> 16686 <br> 14268 -> 14268 <br> 14250 -> 14250 <br> 9411 -> 9411|jaegertracing/all-in-one|

> UI is available on <http://localhost:16686>
