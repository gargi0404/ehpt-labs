⁠ bash
hashid <hash>
 ⁠

### john

⁠ bash
john --format=raw-md5 hash.txt
john hash.txt
john --show hash.txt
 ⁠

### hashcat

⁠ bash
hashcat -m 0 hash.txt /usr/share/wordlists/rockyou.txt
hashcat -m 100 hash.txt /usr/share/wordlists/rockyou.txt
 ⁠

### generate hashes

⁠ bash
echo -n "password" | md5sum
echo -n "password" | sha1sum
echo -n "password" | sha256sum