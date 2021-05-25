# Steps to run this project


##  set data directory
    * open docker-compose.yml
    * go to logstash container setup section and update the data directory in volume. Example given below. only update host machine path     <host-machine>:<container-directory>
        volumes:
            - /home/amit/projects/elastic_workspace/docker_elk/fb_data/03-11:/usr/share/logstash/data


## update Elasticsearch host
    * open ldap.conf
    * update output section of the config file with ES host details


## update logstash.yml [optional]

    * Open logstash.yml and update elasticsearch address. example:
        monitoring.elasticsearch.hosts:
            - http://es01:9200