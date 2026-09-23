\# Palo Alto Firewall Design Overview



\## Purpose



This lab demonstrates an enterprise firewall architecture using Palo Alto Networks security concepts.



\## Network Architecture



```text

&#x20;                   Internet

&#x20;                      |

&#x20;                   Untrust

&#x20;                      |

&#x20;             +------------------+

&#x20;             | Palo Alto Firewall|

&#x20;             +------------------+

&#x20;                /            \\

&#x20;             Trust           DMZ

&#x20;              |               |

&#x20;       Internal Users      Web Server

&#x20;       10.10.10.0/24     10.10.20.0/24

