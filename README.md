# pi-ansible-docker-cluster

## Introduction
Ansible project dedicated to the installation of docker-ce on a raspberry pi cluster while also activating the docker swarm mode.
In its current state, two nodes are defined as managers and two as workers.

## Requirements
Ansible must be installed and runnable. 


The raspberry pi nodes must have a running OS. 

This project was tested on Raspbian Jessie.

## How to run:
1. Update hosts file and change the ip/hosts to reflect your raspberry cluster
1. Change directory to the root of the project
1. `ansible-playbook -i hosts site.yaml`

## Roles
**common** Is basicaly a test used to learn the basics and edit files using **lineinfile**

**docker-swarm** main.yaml installs docker on every node then delegates the swarm setup to swarm_cluster.yaml

Note: There seems to be an incompatibility between docker.service and daemon.json for docker on Debian/Ubuntu/Raspbian where defining "hosts" variable is impossible because it's already defined by "-H" option in docker.service
 
 ## Lisence 
 Apache 2.0
 
 ## Author
 Adi Bajramov