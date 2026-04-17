# Week 04: Routing

## Task 1: View Routing Tables 
## Outputs
1. GNS3 Project file      
[View Route GNS3 File](GNS3-Files/View-Route-12219173.gns3project)   

2. Network Diagram   
![Network-Screenshot](Images/View-Routes-12219173-network.png)

3. Record of IP Routes
*An IP route is an entry in a routing table that tells a device:   
Destination network -where the packet wants to go   
Next hop -which router to send it to   
Outgoing interface -which port to use*

![Routes-Screenshot](Images/View-Routes-12219173-host1-route.png)   
![Routes-Screenshot](Images/View-Routes-12219173-host2-route.png)   
![Routes-Screenshot](Images/View-Routes-12219173-router-route.png)   
![Routes-Screenshot](Images/View-Routes-12219173-host3-route.png)   

5. Ping to other network       
![Ping-Screenshot](Images/View-Routes-12219173-ping.png)   

## Task 2: Dynamic Routing with OSPF

## Outputs

1. GNS3 File demonstrating OSPF    
[GNS3-Routing-OSPF](GNS3-Files/OSPF-Basics-12219173-Template.gns3project)   

2. Network Diagram demonstrating OSPF     
![Network-Screenshot](Images/OSPF-Basics-12219173-network.png)   

3. Neigbour routers of FRR1     
![OSPF-Route-Screenshot](Images/OSPF-Basics-12219173-neigbhor-router.png)   

4. Routing table for two routers       
![OSPF-Route-Table-Screenshot](Images/OSPF-Basics-12219173-routing-table-FFR2.png)     
![OSPF-Route-Table-Screenshot](Images/OSPF-Basics-12219173-routing-table-FFR3.png)    

5. Routing Table Summary    

FRR‑1
| Destination | Next Node |
|------------|-----------|
| 10.10.1.0/24 | Direct |
| 10.10.2.0/24 | FRR‑2 |
| 10.10.3.0/24 | FRR‑3 |
| 10.10.4.0/24 | FRR‑2 |
| 10.10.5.0/24 | FRR‑3 |
| 10.10.6.0/24 | FRR‑2 or FRR‑3 → FRR‑4 |

FRR‑2
| Destination | Next Node |
|------------|-----------|
| 10.10.2.0/24 | Direct |
| 10.10.4.0/24 | Direct |
| 10.10.1.0/24 | FRR‑1 |
| 10.10.3.0/24 | FRR‑1 or FRR‑3 |
| 10.10.5.0/24 | FRR‑1 → FRR‑3 |
| 10.10.6.0/24 | FRR‑1 → FRR‑3 → FRR‑4 |

FRR‑3
| Destination | Next Node |
|------------|-----------|
| 10.10.3.0/24 | Direct |
| 10.10.5.0/24 | Direct |
| 10.10.1.0/24 | FRR‑1 |
| 10.10.2.0/24 | FRR‑1 or FRR‑2 |
| 10.10.4.0/24 | FRR‑1 → FRR‑2 |
| 10.10.6.0/24 | FRR‑4 |

FRR‑4
| Destination | Next Node |
|------------|-----------|
| 10.10.6.0/24 | Direct |
| 10.10.3.0/24 | FRR‑3 |
| 10.10.5.0/24 | FRR‑3 |
| 10.10.1.0/24 | FRR‑3 → FRR‑1 |
| 10.10.2.0/24 | FRR‑3 → FRR‑1 → FRR‑2 |
| 10.10.4.0/24 | FRR‑3 → FRR‑1 → FRR‑2 |

6. Traceroute Command Output    
* Without stopping NETem      
![Traceroute-A-Screenshot](Images/OSPF-Basics-12219173-network-traceroute.png)   

* Stopping NETem 1     
![Traceroute-B-Screenshot](Images/OSPF-Basics-12219173-network-traceroute-linkdown.png)   
