# 08 — Networking for ROS 2

Learn general networking first.

Open textbook:
https://cnp3book.info.ucl.ac.be/

Then apply it to DDS.

Topics:
- IP
- subnetting
- routing
- UDP
- TCP
- multicast
- sockets
- firewall
- interfaces
- packet capture

Tools:
https://www.wireshark.org/
https://www.tcpdump.org/

ROS debugging flow:

```text
Application
 -> RMW
 -> DDS
 -> Discovery
 -> QoS
 -> RTPS
 -> UDP
 -> Interface
 -> Route
 -> Firewall
 -> Destination
```
