Router 2 1941
Switch0 2060-24TT
PC-PT PC0 IP address: 168.90.0.2
PC-PT PC1 IP address: 168.90.0.3
Laptop-PT Laptop0 IP address: 168.90.0.4
Server-PT Server0 IP address: 168.90.0.5

Switch1 2960-24TT
PC-PT PC3 IP address: 210.3.14.2
Server-PT Server1 IP address: 210.3.14.3
Server-PT Server2 IP address: 210.3.14.4

Update: PC-PT PC2 IP address:168.90.0.6 connected to Switch0, configured to use DHCP.
PC-PT PC4 IP address: 210.3.14.5 connected to Switch1, configured to use DHCP.
DHCP Configuration Details
The following steps were used to configure DHCP on the router:

Enter Privileged EXEC mode by typing enable and pressing Enter. This gives administrative access to the router.

Enter Global Configuration mode by typing configure terminal and pressing Enter. This mode allows changes to be made to the router's settings.

Set up DHCP for the first network, which is for devices connected to Switch0:

Create a DHCP pool named LAN1.
Specify that the network address is 168.90.0.0 with a subnet mask of 255.255.0.0.
Set the default gateway (router's address) for this network to 168.90.0.1.
Set up DHCP for the second network, which is for devices connected to Switch1:

Create a DHCP pool named LAN2.
Specify that the network address is 210.3.14.0 with a subnet mask of 255.255.255.0.
Set the default gateway (router's address) for this network to 210.3.14.1.
Exclude certain IP addresses from being assigned dynamically by DHCP:

Exclude the router's IP address 168.90.0.1 for the first network.
Exclude the router's IP address 210.3.14.1 for the second network.
This ensures that these IP addresses are reserved for the router and not assigned to other devices.
Exit Global Configuration mode by typing exit and pressing Enter.

Save the configuration so it is not lost when the router is restarted. 