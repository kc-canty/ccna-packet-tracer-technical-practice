## Troubleshooting Event 1 — Router Transit Link Down

### Symptom

The GigabitEthernet0/1 interfaces connecting R1 and R2 did not
establish connectivity. The interface status showed down/down,
preventing the 10.0.0.0/30 transit network from appearing as a
connected route.

### Investigation

I used:

show ip interface brief

to verify interface status on both routers.

The interfaces were enabled with `no shutdown`, but remained
down/down, indicating that the problem was likely physical rather
than an administrative shutdown or IP addressing issue.

### Root Cause

The physical Packet Tracer connection between R1 and R2 was
incorrect.

### Resolution

I removed the incorrect connection and reconnected R1
GigabitEthernet0/1 to R2 GigabitEthernet0/1 using the appropriate
Ethernet connection.

### Verification

After reconnecting the devices, both router interfaces transitioned
to up/up and the 10.0.0.0/30 network appeared in the routing table.
Connectivity was then verified using ICMP ping.
