# Week 02: Encapsulation and Decapsulation

## Task 1: Setting Static IP Addresses
## Outputs
1. GNS3 File \
[GNS3-Setting IP](GNS3-Files/Setting-IP-12219173.gns3project)

2. Network Diagram \
DIAGRAM

3. IP Address of Hosts \

Host 1 

Host 2 \
The IP address are assigned manually from the configure menu in GNS3 by removing the # from some commands.\
The IP assigned are not interupted by restart of the device. \

Host 3 \
The IP is assigned using command ( *ip address add <ipaddress>/<mask> dev eth0* ) \
*ip address 10.1.1.4/24 dev eth0* \
The IP assigned is removed upon restart.

Host 4 \
The IP is assigned via terminal. Open host 4 terminal and edit the configuration file *interfaces* located in /etc/network directory.
The IP assigned is fixed and the restart doesnt removed the IP
