# Week 06: Address Resolution and Management

## Task 1: Resolving IP Addresses to Hardware Addresses
## Outputs    

1. Host1 ARP    
![Screenshot ARP ](Images/ARP-Basics-12219173-Host1-Table.png)   


## Task 2: Default Gateways
## Outputs  
1. GNS3 VLAN File       
[VLAN GNS3 File](GNS3-Files/Default-Gateway-12219173.gns3project)   

2. Network Diagram    
![Screenshot Network VLAN](Images/Default-Gateway-12219173-Network.png)   

3. Ports and Tags    
Interface Details

| Device   | Interface | IP Address     | Subnet Mask     | Network     |
|----------|-----------|----------------|------------------|-------------|
| Host1    | eth0      | 10.1.1.73      | 255.255.255.0    | 10.1.1.0/24 |
| Host2    | eth0      | 10.1.1.74      | 255.255.255.0    | 10.1.1.0/24 |
| Router1  | eth0      | 10.1.1.1       | 255.255.255.0    | 10.1.1.0/24 |
| Router1  | eth1      | 10.1.3.73      | 255.255.255.0    | 10.1.3.0/24 |
| Router2  | eth0      | 10.1.2.1       | 255.255.255.0    | 10.1.2.0/24 |
| Router2  | eth1      | 10.1.3.74      | 255.255.255.0    | 10.1.3.0/24 |
| Host3    | eth0      | 10.1.2.73      | 255.255.255.0    | 10.1.2.0/24 |
| Host4    | eth0      | 10.1.2.74      | 255.255.255.0    | 10.1.2.0/24 |    

Route Details     
| Device   | Destination     | Next Hop         | Interface |
|----------|------------------|------------------|-----------|
| Router1  | 10.1.1.0/24      | directly connected | eth0 |
| Router1  | 10.1.3.0/24      | directly connected | eth1 |
| Router1  | 10.1.2.0/24      | 10.1.3.74          | eth1 |
| Router2  | 10.1.2.0/24      | directly connected | eth0 |
| Router2  | 10.1.3.0/24      | directly connected | eth1 |
| Router2  | 10.1.1.0/24      | 10.1.3.73          | eth1 |    


4. Ping to Other Network    
![Screenshot Network VLAN](Images/Default-Gateway-12219173-Ping.png)   
