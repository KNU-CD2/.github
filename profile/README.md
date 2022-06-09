![Title](https://user-images.githubusercontent.com/33932392/170961366-364eb7a5-fc30-4b9c-9b24-4e73ccc75ec4.png)


## Introduction
This project collaborates with the capstone design class at Kyungpook National University([KNU](https://knu.ac.kr)) and [CSP MOBILE LAB](http://cspmobilelab.com/).

We develop a `Real-time Data Distribution Pipeline System` with log data from KIOSK.

<br/>

## Demo Video
https://youtu.be/noJt1Ua8xsM

<br/>

## Architecture
### Hardware
![hardware_architecture](https://user-images.githubusercontent.com/33932392/170934202-9ec6365d-7a7f-4c8d-94ad-1f32aaf71da5.png)


### Software
![software_architecture](https://user-images.githubusercontent.com/33932392/170937471-1770d1fc-53d7-478e-a430-08de551db0bb.png)


## Tech Stack
- OS : Ubuntu server 20.04 LTS
- Log generator: python 3.8.10
- File Beats 8.1.0
- Kafka 3.1.0
- Logstash 8.1.0
- Elasticsearch 8.1.0
- Kibana 8.1.0

<br/>

## Cluster Configuration
### Elasticsearch Cluster
<img width="1287" alt="elasticsearch_cluster" src="https://user-images.githubusercontent.com/33932392/172815390-f0137057-20b0-4f02-a606-52d17feebde6.png">

> Elasticsearch consists of three nodes.

- c1-elastic (Data Node)
- c2-elastic (Master node)
- c3-elastic (Data Node)

If a node acting as a master is disconnected from the network or goes down, one of the other master candidate nodes is elected as the master node and acts as the master node instead. The master candidate nodes share the information of the master node from the beginning, so the master role can be performed immediately.

### Kafka Cluster
<img width="1321" alt="kafka cluster" src="https://user-images.githubusercontent.com/33932392/172584842-b2af8dfd-b75b-4ac0-8f05-a5a5946627f4.png">

> Kafka conssists of three nodes.

- c1-kafka
- c2-kafka
- c3-kafka

<br/>

## On-premise
### 
<p align="center">
  <img src="https://user-images.githubusercontent.com/33932392/170950962-8c608207-1031-4838-b9a8-1fee68f96384.png">
</p>

> We have built an on-premise server, and the following is a list of the components of the server.

- Raspberry Pi 4B - 4GB(1ea), 8GB(6ea)
- Disk - Sandisk Extreme 32GB MLC
- Router - iptime A3004T
- Switching hub - iptime H6008
- Raspberry Pi Power - 5V 3A C-type charger
- Etc - cat 6 LAN cable 30cm, Holder box case

More detailed information is written [here](https://knu-cd2.github.io/blog/on-premise/2022/05/05/on-premise-hardware.html).

<br/>

## Blogs
We create a blog and poste how to overcome the challenges, especially security settings, faced by developing the system. We think this can contribute a little bit to the open-source ecosystem.

[Here is the blog link.](https://knu-cd2.github.io/blog/)
