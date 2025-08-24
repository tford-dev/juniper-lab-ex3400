In this lab I am using my Asus ROG GU603 laptop as a router/default gateway.
My GU603 is connected to my home WiFi and I’ve set up my connection to share internet access downlink on the NIC. 
The NIC is connected to an SFP on ge-0/2/0 on FORD-JUN-SW1.
FORD-JUN-SW1 has a default route pointing to the NIC on GU603.
FORD-JUN-SW1 has DHCP services for VLAN 10 and 20 and has 3 access ports for VLAN 10.
FORD-JUN-SW1 connects to FORD-JUN-SW2 through an etherchannel trunk bundled with 2 cables into SFPs on ports ge-0/2/1-2.
FORD-JUN-SW2 is mainly layer 2 and has 3 access ports for VLAN 20.
FORD-JUN-SW1 and FORD-JUN-SW2 can both be SSHd via the Asus ROG GU603 using VLAN 99.
FORD-JUN-SW2 has a static route pointing to the VLAN 99 interface of FORD-JUN-SW1
Both switches have an Admin and Viewer account with different levels of privilege.
Asus ROG GU603 has routes pointing to VLAN 10,20, and 99 from the NIC. 
