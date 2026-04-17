# Week 05: Switching and VLAN

## Task 1: Set Up VLAN Switch    
## Outputs    
1. GNS3 VLAN File       
[VLAN GNS3 File](GNS3-Files/Vlan-Basics-12219173.gns3project)   

2. Network Diagram    
![Screenshot Network VLAN](Images/Vlan-Basics-12219173-Network.png)    
*A VLAN is a logical grouping of devices that communicate as if they are on the same LAN, even when connected to different switches. VLANs reduce broadcast traffic, improve security, and allow flexible network design.*    

3. Ports and Tags    
![Screenshot Ports and VLAN ID](Images/Vlan-Basics-12219173-Ports.png)   

## Task 2: Setup VLANs on a Router
## Outputs  
1. GNS3 VLAN File       
[VLAN GNS3 File](GNS3-Files/Vlan-Router-12219173.gns3project)   

2. Network Diagram    
![Screenshot Network VLAN](Images/Vlan-Router-12219173-network.png)     

3. Ports and Tags    
![Screenshot Ports and VLAN ID](Images/Vlan-Router-12219173-ports.png)   
   
  
*Commands Learned    
$ovs-vsctl show   
$ovs-vsctl set port eth1 tag=10    
$ovs-vsctl set port eth0 trunks=10,20    
ovs-vsctl set port eth0 trunks=[]    
ip link add link eth0 name eth0.10 type vlan id 10     
ip address add 1.2.3.4/24 dev eth0.10*    


