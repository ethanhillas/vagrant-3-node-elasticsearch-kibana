# Vagrant: 3-node Elasticsearch cluster and Kibana

This repository includes a vagrant deployment for a local non-production or development Elastic stack. The deployment includes 3 Elasticsearch nodes and 1 Kibana server which is deployed using Virtualbox and Vagrant. Elasticsearch and Kibana can be installed using ansible with this repository: [Ansible: 3-node Elasticsearch cluster and Kibana](https://github.com/ethanhillas/ansible-3-node-elasticsearch-kibana).

Vagrant will deploy 4 local virtual machines with Virtualbox using a centos7 vagrant box base image from [geerlingguy](https://app.vagrantup.com/geerlingguy/boxes/centos7). Each virtual machine is given 2GB RAM and is using the default vagrant ssh key and vagrant user. 

Each virtual machine is placed on a private network with static IP addresses and hostnames configured in the Vagrantfile. 

To start a deployment with vagrant:
1. Download this repository to your local machine and ensure vagrant (>2.2) is installed. 
2. Change to the working directory (directory with the Vagrantfile) and run `vagrant up`.

To suspend the deployment:
1. Run `vagrant suspend` in the working directory.

To remove the deployment:
1. Run `vagrant destroy` in the working directory.
    * When prompted, select which machines to destroy.
    * If you want to destroy all machines, run `vagrant destroy -f`.