# vagrant-elasticsearch
Vagrant ElasticSearch box on Ubuntu 18.04

This uses Vagrant with VirtualBox to build an ELK stack in Ubuntu 18.04.

Simply drop this into your local vagrant locations and 'vagrant up'.

Machine
4CPUs
4GB RAM
It is using bridge mode and public_network so you may need to adjust the hard coded interface name.

Uses a shell provisioner for all the elk setup stuff.