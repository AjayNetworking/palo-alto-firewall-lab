\# Palo Alto NAT Configuration



\## Objective



Demonstrate how NAT can be used to provide controlled connectivity between internal, DMZ, and external networks.



\## Source NAT



Source NAT allows internal users to access external networks using a translated public IP address.



\### Example



\- Source Zone: Trust

\- Destination Zone: Untrust

\- Source Network: 10.10.10.0/24

\- Destination: Any

\- Translation: Dynamic IP and Port

\- Translated Address: Firewall public IP



\## Destination NAT



Destination NAT allows external users to access an approved service hosted in the DMZ.



\### Example



\- Source Zone: Untrust

\- Destination Zone: Untrust

\- Destination Address: Public IP

\- Service: HTTPS

\- Translated Address: DMZ Web Server

\- Translated Port: 443



\## NAT Design Principles



\- Use specific NAT rules

\- Keep NAT rules organized by traffic flow

\- Review security policy together with NAT

\- Log and monitor important traffic

\- Avoid unnecessary exposure of internal services



\## Validation



When troubleshooting NAT, verify:



1\. Source and destination zones

2\. NAT rule matching

3\. Security policy matching

4\. Translated addresses

5\. Session information

6\. Traffic logs

