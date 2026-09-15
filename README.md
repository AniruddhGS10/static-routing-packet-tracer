# Static Routing and Proxy ARP

## Overview

This project is a Cisco Packet Tracer lab demonstrating static routing and Proxy ARP using three routers.

The lab covers directly connected static routes, recursive static routes, ARP, and Proxy ARP.

## Network Topology

R1 ---------------- R2 ---------------- R3
       192.168.1.0/24       192.168.2.0/24

## IP Addressing

| Router | Interface | IP Address |
|--------|-----------|------------|
| R1 | G0/0 | 192.168.1.1/24 |
| R2 | G0/0 | 192.168.1.2/24 |
| R2 | G0/1 | 192.168.2.1/24 |
| R3 | G0/0 | 192.168.2.2/24 |

## Static Routing

The lab demonstrates two types of static routing.

### Directly Connected Static Route

An exit interface can be used to configure a static route.

ip route 192.168.2.0 255.255.255.0 g0/0

### Recursive Static Route

A next-hop IP address can be used to configure a recursive static route.

ip route 192.168.1.0 255.255.255.0 192.168.2.1

## Proxy ARP

Proxy ARP allows a router to respond to an ARP request on behalf of another device when the destination can be reached through the router.

Proxy ARP can be checked using:

show ip interface g0/0

It can be enabled using:

ip proxy-arp

## Verification

The following commands were used to verify the configuration and connectivity:

show ip interface brief
show ip route
show ip arp
show ip interface
ping

These commands help verify interface status, routing tables, ARP entries, Proxy ARP, and connectivity between the networks.

## What I Learned

This lab helped me understand how static routing works and the difference between directly connected and recursive static routes.

I also learned how ARP operates in a routed network and how Proxy ARP allows a router to respond to ARP requests on behalf of another device.

## Tools Used

- Cisco Packet Tracer
- Cisco IOS
- IPv4
- Static Routing
- ARP
- Proxy ARP
