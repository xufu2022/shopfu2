# Big Picture

Elastic Search

-   Free and Open Source
-   Restful Api
-   Easy to Query
-   Very fast
-   Scalable
-   Easy to install

Kibana

    logstash -> elastic search -> kibana

Serilog -<> sink to elastic 

https://hub.docker.com/_/elasticsearch
https://hub.docker.com/_/kibana
https://github.com/thecarlo/elastic-kibana-netcore-serilog


add docker compose and also to the override file

  elasticsearch:
    image: docker.elastic.co/elasticsearch/elasticsearch:7.9.2

  kibana:
    image: docker.elastic.co/kibana/kibana:7.9.2

docker-compose -f docker-compose.yml -f docker-compose.override.yml up -d
docker-compose -f docker-compose.yml -f docker-compose.override.yml down -d

localhost:9200
localhost:9200/_aliases
localhost:9200/products/_bulk
localhost:9200/products/_search

localhost:5601
go to devtools

example 
    Get products/_search
    {
    }

    Get /products/_doc
    {
    "name":"iphone_y"
    }

Elastic search and kanbana and serilog integration

