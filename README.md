
# DNS-Exfil-Demo
# This is a DNS Tunneling Exfil Demo
# this is for demo purposes only. 


Client /n
data.txt = grama's muffins recipe :-)

dns_exfil_client.py = dns tunnel exfil script on client side. Point the DNS resolver to localhost (hosts file) or a local DNS proxy.

Server
data_exfiled.txt = this is the txt file that the dns server logs the exfiltrated encoded dns requests to on the attacker C2 infrastructure.

dns_exfil_server.py = python DNS server. listens for DNS requests to h4xh4xh4x.com (or any domain) and strips the hostname over the query and streams to a file using base 64 encoding.  

zones.txt = the attack dns zones. Make this whatever you want. Even a non malicious domain so it passes through the URL filtering. The DNS security on PAN can detect this attack.
