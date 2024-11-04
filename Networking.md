# What is a Computer Network?
A computer network is a collection of interconnected devices that share resources and information. These devices can include computers, servers, printers, and other hardware. Networks allow for the efficient exchange of data, enabling various applications such as email, file sharing, and internet browsing.

# Basic Terminologies of Computer Networks
- Network:  A network is a collection of computers and devices that are connected together to enable communication and data exchange.
- Nodes:  Nodes are devices that are connected to a network. These can include computers, Servers, Printers, Routers, Switches, and other devices.
- Protocol:  A protocol is a set of rules and standards that govern how data is transmitted over a network. Examples of protocols include TCP/IP, HTTP, and FTP.
- Topology:  Network topology refers to the physical and logical arrangement of nodes on a network. The common network topologies include bus, star, ring, mesh, and tree.
- Service Provider Networks:  These types of Networks give permission to take Network Capacity and Functionality on lease from the Provider. Service Provider Networks include Wireless Communications, Data Carriers, etc.
- IP Address:  An IP address is a unique numerical identifier that is assigned to every device on a network. IP addresses are used to identify devices and enable communication between them.
- DNS:  The Domain Name System (DNS) is a protocol that is used to translate human-readable domain names (such as www.google.com) into IP addresses that computers can understand.
- Firewall:  A firewall is a security device that is used to monitor and control incoming and outgoing network traffic. Firewalls are used to protect networks from unauthorized access and other security threats.

# Bridge
A Linux bridge behaves like a network switch. It forwards packets between interfaces that are connected to it. It's usually used for forwarding packets on routers, on gateways, or between VMs and network namespaces on a host. It also supports STP, VLAN filter, and multicast snooping.
![image](https://github.com/user-attachments/assets/316706a4-ac67-4c67-9d45-a6e6311c1e7f)

#  VLAN
A VLAN, aka virtual LAN, separates broadcast domains by adding tags to network packets. VLANs allow network administrators to group hosts under the same switch or between different switches.
![image](https://github.com/user-attachments/assets/97ed2a40-65bb-4f77-a9ca-8b8a85c54ba1)

# VXLAN
VXLAN (Virtual eXtensible Local Area Network) is a tunneling protocol designed to solve the problem of limited VLAN.With a 24-bit segment ID, aka VXLAN Network Identifier (VNI), VXLAN allows up to 2^24 (16,777,216) virtual LANs, which is 4,096 times the VLAN capacity.
  VXLAN encapsulates Layer 2 frames with a VXLAN header into a UDP-IP packet, which looks like this:
  ![image](https://github.com/user-attachments/assets/ebba2912-7a8f-40ad-9efa-7e1adc5bcb2e)

  # MACVLAN
With VLAN, you can create multiple interfaces on top of a single one and filter packages based on a VLAN tag. With MACVLAN, you can create multiple interfaces with different Layer 2 (that is, Ethernet MAC) addresses on top of a single one.

Before MACVLAN, if you wanted to connect to physical network from a VM or namespace, you would have needed to create TAP/VETH devices and attach one side to a bridge and attach a physical interface to the bridge on the host at the same time, as shown below. 
![image](https://github.com/user-attachments/assets/4d869eb6-a4af-4abd-b645-8588868aa7ee)

# IPVLAN
IPVLAN is similar to MACVLAN with the difference being that the endpoints have the same MAC address.
![image](https://github.com/user-attachments/assets/71f46b20-c7b5-4cdf-8c2d-3e5f0573936b)

# VETH
The VETH (virtual Ethernet) device is a local Ethernet tunnel. Devices are created in pairs, as shown in the diagram below.
Packets transmitted on one device in the pair are immediately received on the other device. When either device is down, the link state of the pair is down.
![image](https://github.com/user-attachments/assets/b4158b07-f8c4-4a4a-949e-007d8c1799e0)


# VCAN
Similar to the network loopback devices, the VCAN (virtual CAN) driver offers a virtual local CAN (Controller Area Network) interface, so users can send/receive CAN messages via a VCAN interface. CAN is mostly used in the automotive field nowadays.
Use a VCAN when you want to test a CAN protocol implementation on the local host.

# VXCAN
Similar to the VETH driver, a VXCAN (Virtual CAN tunnel) implements a local CAN traffic tunnel between two VCAN network devices. When you create a VXCAN instance, two VXCAN devices are created as a pair. When one end receives the packet, the packet appears on the device's pair and vice versa. VXCAN can be used for cross-namespace communication.




