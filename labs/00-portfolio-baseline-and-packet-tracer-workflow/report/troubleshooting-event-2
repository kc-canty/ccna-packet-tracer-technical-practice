## Troubleshooting Event 2 — Incorrect Default Gateway

### Symptom

PC1 could no longer communicate with PC2 across the routed network.
The routers and transit connection remained operational.

### Investigation

I tested connectivity incrementally instead of immediately modifying
the network.

PC1 could reach its local gateway, and R1 could reach R2. Both routers
had operational interfaces and valid routes.

R2 could successfully communicate with PC2, indicating that the
192.168.20.0/24 LAN was operational.

PC2 could communicate with local devices but could not reach devices
outside its subnet.

I used `ipconfig` on PC2 and compared its configuration with the
network addressing plan.

### Root Cause

PC2's default gateway was incorrectly configured as 192.168.20.254
instead of 192.168.20.1.

### Resolution

I corrected PC2's default gateway to 192.168.20.1.

### Verification

I verified local and remote connectivity from PC2 and then repeated
the original end-to-end test from PC1.

PC1 successfully reached PC2 with 0% packet loss and traceroute again
showed the expected path through R1 and R2.
