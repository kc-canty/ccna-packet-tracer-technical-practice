# Lab 00 — Portfolio Baseline and Packet Tracer Workflow

## Objective

The objective of this lab is to build a basic routed network in Cisco
Packet Tracer consisting of two LANs connected through two Cisco routers.
The lab establishes my standard workflow for planning, configuring,
verifying, troubleshooting, and documenting future CCNA labs.

## Topology

PC1 --- SW1 --- R1 --- R2 --- SW2 --- PC2

## Addressing Plan

| Device | Interface | IPv4 Address | Prefix | Gateway |
|---|---|---|---|---|
| PC1 | FastEthernet0 | 192.168.10.10 | /24 | 192.168.10.1 |
| SW1 | VLAN 1 | 192.168.10.2 | /24 | 192.168.10.1 |
| R1 | G0/0 | 192.168.10.1 | /24 | N/A |
| R1 | G0/1 | 10.0.0.1 | /30 | N/A |
| R2 | G0/1 | 10.0.0.2 | /30 | N/A |
| R2 | G0/0 | 192.168.20.1 | /24 | N/A |
| SW2 | VLAN 1 | 192.168.20.2 | /24 | 192.168.20.1 |
| PC2 | FastEthernet0 | 192.168.20.10 | /24 | 192.168.20.1 |
