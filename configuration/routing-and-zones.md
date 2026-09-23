\# Palo Alto Routing and Security Zones



\## Objective



Define the routing and security-zone structure used by the Palo Alto firewall.



\## Security Zones



| Zone | Network | Purpose |

|---|---|---|

| Trust | 10.10.10.0/24 | Internal users |

| DMZ | 10.10.20.0/24 | Public-facing services |

| Untrust | External | Internet connectivity |

| Management | 10.10.99.0/24 | Firewall administration |



\## Interface Design



| Interface | Zone | IP Address |

|---|---|---|

| ethernet1/1 | Untrust | 203.0.113.2/30 |

| ethernet1/2 | Trust | 10.10.10.1/24 |

| ethernet1/3 | DMZ | 10.10.20.1/24 |

| ethernet1/4 | Management | 10.10.99.1/24 |



\## Routing



The firewall uses a virtual router to determine the next hop for traffic.



\### Default Route



0.0.0.0/0 → 203.0.113.1



\### Internal Networks



10.10.10.0/24 → Trust

10.10.20.0/24 → DMZ



\## Traffic Flow



Internal User → Trust → Palo Alto Firewall → Untrust → Internet



\## Design Principles



\- Separate networks using security zones

\- Use explicit routing

\- Apply security policies between zones

\- Use a default route for external traffic

\- Keep management traffic isolated



> Note: 203.0.113.0/24 is documentation/test address space and is not a real public network.

