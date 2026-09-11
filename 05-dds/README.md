# 05 — DDS

Do not treat DDS as a black box.

Study:
- data-centric publish/subscribe
- domain
- participant
- topic
- publisher
- subscriber
- DataWriter
- DataReader
- QoS
- discovery
- SPDP
- SEDP
- RTPS
- GUID
- sequence numbers
- heartbeat
- ACKNACK
- GAP
- fragmentation

Primary references:
https://www.omg.org/spec/DDS
https://www.omg.org/spec/DDSI-RTPS

Mental mapping:

```text
ROS Node / context
      ↓
DDS DomainParticipant

ROS Publisher
      ↓
DDS DataWriter

ROS Subscription
      ↓
DDS DataReader
```
