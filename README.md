# Multi Node Kafka Cluster Setup Using Docker

This configuration builds a docker container to run a x3 node Kafka cluster powered by x3 Zookeeper nodes. This project is based on the official Confluent Kafka image.

## Configuration

Configuration is pretty straightforward - since this is a multi-node cluster, I kept the same ports throughout (because I can!). Long live Docker v3 as it allowed me to attach private network as well (ergo, no need for a DNS server).

## Run Kafka Cluster

    $ docker-compose up -d

This will spawn x6 Docker Containers (x3 Kafka + x3 Zookeeper) and another proxy container should you need to have direct access to any of these containers.

## Demo
![Kafka1](https://scontent.fmla3-1.fna.fbcdn.net/v/t31.0-8/24955708_828478520673469_7426113270188870801_o.jpg?oh=badc4d07b63cf4ce7a378cc29234c6ea&oe=5ACD8C33)

![Kafka2](https://scontent.fmla3-1.fna.fbcdn.net/v/t31.0-8/24958860_828478527340135_7766061999195725519_o.jpg?oh=d2ed994f0a97eaff23a63513604b4254&oe=5A937EF0)

![Kafka3](https://scontent.fmla3-1.fna.fbcdn.net/v/t31.0-8/25188981_828478550673466_56804955467429662_o.jpg?oh=61a1642b26100cf01177fed53e191c69&oe=5AD0B4F0)
