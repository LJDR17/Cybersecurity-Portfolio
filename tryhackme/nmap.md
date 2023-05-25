---
description: >-
  This page will document the practical portion of the Further Nmap section on
  TryHackMe.
---

# Nmap

The first task given is to see if the target responds to ICMP ping requests. To perform a ICMP sweep we can use the -sn function: nmap -sn 10.10.107.102, and upon doing this to our target we can see the host is up and has responded with an ARP packet.

Secondly, we need to perform and Xmas scan on the first 999 ports of the target, which we can do using the -sX function: nmap -sX 10.10.107.102 --top-ports 999, and we can see that the first 999 ports are all open/filtered.

If we increase verbosity by adding -vv, we can see that there was actually no response for any of the requests, this is because no handshake is performed, the scan is stateless. A RST flag would be returned for closed ports.

Next, we need to do a TCP SYN scan on the first 5000 ports of the target, which we can do using the -sS function: nmap -sS 10.10.107.102 --top-ports 5000, and we can see that ports 21, 53, 80, 135, 3389, 5985 are open.

Finally, we need to run the ftp-anon script against the target, which was done using the command nmap 10.10.107.102 --script ftp-anon and the result shows us that anonymous ftp login is allowed which enables remote users to use the FTP server without an assigned user ID and password.
