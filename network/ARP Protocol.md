# ARP Protocol

The Address Resolution Protocoll is a mapping of L3 address to L2 address
When a device on a network needs to send a message to another device that is reacheable from that particular network.
The device in this case only knows the IP address of the destination but nothing else, and it doesn't know how to get there.
The device will therefore send a `ARP Request` or in other words a broadcast request on the network with the ip address of the destination that asks for the MAC address of the destination.
All the devices that do not corrispond with the IP address will drop the packet and only the device with correct IP will send back its MAC address in a `ARP Response`. This information is then stored in the ARP table of the sender, that now knows which device should go next to reach the final destination.
