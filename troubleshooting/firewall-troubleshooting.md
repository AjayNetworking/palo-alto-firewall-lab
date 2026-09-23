\# Palo Alto Firewall Troubleshooting



\## Troubleshooting Workflow



When traffic is not working, troubleshoot from the network foundation upward.



\### 1. Interface Status



Verify that the required firewall interface is operational.



Check:



\- Interface status

\- IP address

\- Assigned zone

\- Interface configuration



\### 2. Security Zones



Confirm that the source and destination interfaces belong to the expected zones.



Example:



```text

Trust → Untrust

Trust → DMZ

Untrust → DMZ

