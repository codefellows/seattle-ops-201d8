# pfSense Install Guide
### Download pfSense iso:
  - You'll also need to extract it!
    - Open with extraction manager
    - Accept defaults 
### VM Settings:
  - FreeBSD 64-bit
  - Default memory and disk is fine
  - System / Pointing Device: USB Tablet
    - This should prevent mouse capture
  - Network:
    - Adapter 1: Bridged (NAT is also fine)
    - Adapter 2: Internal Network
### Installation:
  - Accept all defaults
  - Use <space> to select drive
  - No shell at end, just reboot
    - Will need to remove disk before reboot
### Configuration:
  - Set interface IP address
    - Choose LAN
    - Enter LAN IP (you can change it or keep it the same)
    - Subnet bit count: 24
    - No Gateway, no IPv6
    - Enable DHCP
      - Start address: * . * . * .100
      - End address: * . * . * .200
    - Revert web configurator to HTTP: yes
### Finish:
  - Export OVA backup
  - Take a snapshot
  - Connect a VM to the same Internal Network in order to access the pfSense Web Configurator
    - Username / password: admin / pfsense
  
