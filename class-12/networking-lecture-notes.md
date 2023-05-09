# Networking Lecture Notes:

## Networking Basics: 
- Bottom of the OSI model:

| Layer | address | data | device/protocol |
| --- | --- | --- | --- |
| 4) Transport | Port number   | Segment | TCP, UDP |
| 3) Network   | IP addresses  | Packet  | Router, L3 switch |
| 2) Data Link | MAC addresses | Frame   | L2 switch, bridge |
| 1) Pysical   | port ID       | Bit     | cabling, hub, repeater |
- Subnets
- Network Devices 
  - Switches and Hubs
    - Hub: 
      - Always the wrong answer
      - Have a single broadcast domain
    - Switch:
      - Has individual broadcast domain for each physical port
      - More private
      - Scalable
  - Routers 
  - Firewalls 
    - Network perimeter firewall
    - Simple SoHo routers have simplistic firewalls
    - Enterprise grade routers tend to have higher firewall capabilities
      - Unified Threat Management (UTM) appliances are popular
  - Wireless Access Points (WAP)
    - Wireless access for a network
      - Enterprise grade routers won't have Wi-Fi because you'll deploy Wireless Access Points (WAPs) instead
    - Access Points (APs) create a mesh network over a corporate campus
- DHCP
  - Automatically assigns IP addresses to hosts
  - Sometimes this is hosted on a Windows or Linux server instead
- DNS
  - Resolves local and internet domain names into IP addresses
  - Sometimes this is hosted on a Windows or Linux server instead

SoHo routers:
- Combine multiple functions/roles:
  - Router
  - Switch
  - Firewall
  - WAP
    - Some home Wi-Fi appliances now support meshed AP infrastructure



VirtualBox Network Types:
- https://www.nakivo.com/blog/virtualbox-network-setting-guide/
- Not Attached
- NAT - can access the LAN, but cannot be accessed by other devices
- NAT Network - as above, but can be accessed by other devices which share the same NAT Network*
- Bridged Adapter - shares the host’s network connection
- Internal Network - connected to an isolated virtual network*
- Host-only Adapter - can connect only to the host and other devices on the Host-only Network
  - Must be created in Host Network Manager
  - Has a built-in DHCP Server
- Not Used By Us:
  - Generic Driver and Cloud Network

pfSense:
- Open source firewall and router
  - Helmed by Netgate, who foots a lot of bills
  - When that happened, OPNsense was spun off as a fork
- Built on BSD, not linux
  - BSD is Unix, not linux
  - Specifically, FreeBSD
  - Not a significant difference for how we use it (linux is "unix-like" after all)
- Can be virtualized or deployed to an appliance
  - Netgate produces appliances designed for pfSense
  - But any old computer will do
  - Does not run on consumer routers
- *Why pfSense?*
  - Community choice for open source firewall/router solution for home lab
    - Alternatives include OPNsense, DD-WRT, or OpenWRT
      - The WRT family can be flashed onto some consumer routers
  - Also used in smaller commercial applications!
  - Free
- Why virtualize?
  - Because we are building virtual networks!
  - But even if we were putting it into production, there are still benefits to virtualizing
    - You can bridge hardware NICs to the VM
    - All that we do with VM backups, etc.

