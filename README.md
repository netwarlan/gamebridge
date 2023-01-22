# gamebridge
LAN Game Server Rebroadcaster over VLANs

Created by Travis Kreikemeier @ NETWAR (http://www.netwar.org)

Gamebridge allows you to carve up your LAN party network into many VLANs.  Usually this is a no-no for LAN parties due to the broadcasts needed to find local LAN game servers.  Gamebridge rebroadcasts those game server finding beacons across many VLANs without passing anything else (ARP, BPDU, other non-game server broadcasts, etc.).

# INSTALL
* Follow steps in gamebridge_setup.txt

# REQUIREMENTS
* Tested at large LAN events with Debian 11 as a guest on VMWare ESX 7
* Any other distros may require modifications
* Two NICS: One connected to a single VLAN for management
* The other NIC connected to a trunk port on your switch with all VLANs tagged
* If using VMWare vSwitch, the trunk port group needs to have VLAN 4095 set so that it passes all VLANs tagged to the guest vNIC.

# TODO
* Create installer script to simplify installation
