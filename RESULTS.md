Devices used to configure the network:
1. Four 2811 Routers
2. Four 2960-24TT Routers
3. 4 PCs
4. Serial DCE cable has used for connection type between routers
5. Copper straight-through cable has been used for connection type between PC and Switches & Routers


Screenshot of Network Topology:

![image](https://github.com/user-attachments/assets/713af240-8da2-46fc-9a37-e6c2a0121807)


Configured IP address checking by using ipconfig
Corporate Office PC:
By using the ipconfig command, we will get the ip configuration

  ![image](https://github.com/user-attachments/assets/50486268-2ae1-430f-9184-d9edd72ab04b)

Remote Office01_PC:
![image](https://github.com/user-attachments/assets/521dfe26-c5fe-4d78-8984-a8674d2987fd)

Remote Office02_PC:
![image](https://github.com/user-attachments/assets/75796b76-d7ab-4bc5-998d-423b606e16b9)

Remote Office03_PC:
![image](https://github.com/user-attachments/assets/850938e9-7132-4bb5-884f-031803cba825)


Corporate Office Router IP Configuration:
CO_R1#
Router>enable
Router#configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)#hostname CorporateOffice_R1
CO_R1 (config)#interface FastEthernet0/0
CO_R1 (config-if)#ip address 192.168.0.1 255.255.255.0
CO_R1 (config-if)#no shutdown
CO_R1 (config-if)#
%LINK-5-CHANGED: Interface FastEthernet0/0, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/0, changed state
to up
CO_R1 (config-if)#exit
CO_R1 (config)#interface Serial0/0/0
CO_R1 (config-if)#ip address 200.200.200.1 255.255.255.252
CO_R1 (config-if)#clock rate 64000
This command applies only to DCE interfaces
CO_R1 (config-if)#no shutdown
CO_R1 (config-if)#exit
CO_R1 (config)#interface Serial0/0/1
CO_R1 (config-if)#ip address 205.205.205.1 255.255.255.252
CO_R1 (config-if)#clock rate 64000
This command applies only to DCE interfaces
CO_R1 (config-if)#no shutdown
CO_R1 (config-if)#exit
CO_R1 (config)#interface Serial0/1/0
CO_R1 (config-if)#ip address 210.210.210.1 255.255.255.252
CO_R1 (config-if)#clock rate 64000
CO_R1 (config-if)#no shutdown
CO_R1 (config-if)#exit
CO_R1 (config)#


Remote Office01_Router IP Configuration:
Router>enable
Router#configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)#hostname R2
RO_R1(config)#interface FastEthernet0/0
RO_R1 (config-if)#ip address 192.168.1.1 255.255.255.0
RO_R1 (config-if)#no shutdown
%LINK-5-CHANGED: Interface FastEthernet0/0, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/0,
changed state to up
RO_R1(config-if)#exit
RO_R1 (config)#interface Serial0/0/0
RO_R1 (config-if)#ip address 200.200.200.2 255.255.255.252
RO_R1(config-if)#no shutdown
RO_R1 (config-if)#exit
%LINK-5-CHANGED: Interface Serial0/0/0, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface Serial0/0/0, changed
state to up
RO_R1(config)#


Remote Office02_Router IP Configuration:
Router>enable
Router#configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)#hostname RO_R2
RO_R2(config)#interface FastEthernet0/0
RO_R2 (config-if)#ip address 192.168.2.1 255.255.255.0
RO_R2 (config-if)#no shutdown
%LINK-5-CHANGED: Interface FastEthernet0/0, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/0,
changed state to up
RO_R2(config-if)#exit
RO_R2 (config)#interface Serial0/0/0
RO_R2 (config-if)#ip address 205.205.205.2 255.255.255.252
RO_R2(config-if)#no shutdown
RO_R2 (config-if)#exit
%LINK-5-CHANGED: Interface Serial0/0/0, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface Serial0/0/0, changed
state to up
RO_R2(config)#
Remote Office03_Router IP Configuration:
Router>enable
Router#configure terminal
Enter configuration commands, one per line. End with CNTL/Z.
Router(config)#hostname RO_R3
RO_R3(config)#interface FastEthernet0/0
RO_R3 (config-if)#ip address 192.168.3.1 255.255.255.0
RO_R3 (config-if)#no shutdown
%LINK-5-CHANGED: Interface FastEthernet0/0, changed state to up
%LINEPROTO-5-UPDOWN: Line protocol on Interface FastEthernet0/0,
changed state to up
RO_R3(config-if)#exit
RO_R3 (config)#interface Serial0/0/0
RO_R3 (config-if)#ip address 210.210.210.2 255.255.255.252
RO_R3(config-if)#no shutdown
RO_R3 (config-if)#exit
%LINK-5-CHANGED: Interface Serial0/0/0, changed state to up%LINEPROTO-5-UPDOWN: Line protocol on Interface Serial0/0/0, changed
state to up
RO_R3(config)#


Traffic testing/observations performed to ensure the network was running properly:
we will ensure that the network was running properly by using the ping command.
Corporate Office traffic testing/observation:
![image](https://github.com/user-attachments/assets/780f371b-57b0-4136-a943-fc7591e06f1f)

Remote Office01 traffic testing/observation:
![image](https://github.com/user-attachments/assets/5ae0625d-0a95-42b3-a98e-76f5a6d1c1d8)

Remote Office02 traffic testing/observation:
![image](https://github.com/user-attachments/assets/ed8d3910-2736-455b-84fd-f5ec11bcb8b9)

Remote Office03 traffic testing/observation:
![image](https://github.com/user-attachments/assets/445443b0-6120-48d8-ab83-724063f427c2)


