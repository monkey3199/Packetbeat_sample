# Packetbeat_sample
This is the sample for monitoring server with packetbeat and elastic stack.
All component is installed in docker.
Environment: Amazon linux, Java 1.8, Docker, Elastic stack 5.4

## Install Docker

`sudo yum install -y docker`

You need to root authority to use docker.
In order to use docker as normal user, give an authority the user.

`sudo usermod -aG docker ${USER}`  
`sudo service docker restart`

## Install Elasticsearch

`docker pull docker.elastic.co/elasticsearch/elasticsearch:5.4.2`  

### Running Elasticsearch
`docker run -p 9200:9200 -e "http.host=0.0.0.0" -e "transport.host=127.0.0.1" \ docker.elastic.co/elasticsearch/elasticsearch:5.4.2`

X-pack is preinstalled in this image.Please take a few minutes to familiarize yourself with X-Pack Security and how to change default passwords. The default password for the **elastic** user is **changeme**.

## Install Kibana

## Install Packetbeat
