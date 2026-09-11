# ROS 2 & Robotics Engineering Deep-Study Notebook

> A long-term, self-contained study repository for becoming a **ROS 2 / Robotics Systems Engineer**, from ROS 2 application development down to DDS/RTPS, networking, real-time systems, security, hardware integration, perception, SLAM and autonomous navigation.

## How to use this repository

Do **not** try to finish everything in one pass.

For every subject use this order:

1. Read the concept.
2. Read the official documentation.
3. Understand the architecture.
4. Trace what happens internally.
5. Implement a small example.
6. Break it intentionally.
7. Debug it.
8. Record what you learned.
9. Read one or more research papers.
10. Build a project combining the topic with previous topics.

### Core learning rule

For every technology answer these four questions:

- **Why does it exist?**
- **What problem does it solve?**
- **How does it work internally?**
- **How is it used in a real robot?**

---

# Master architecture

```text
                    YOUR ROBOT APPLICATION
                             |
                 +-----------+-----------+
                 |                       |
             rclcpp/rclpy            Actions
                 |                       |
                 +-----------+-----------+
                             |
                            rcl
                             |
                            RMW
                             |
              +--------------+--------------+
              |                             |
        rmw_fastrtps_cpp             rmw_cyclonedds_cpp
              |                             |
          Fast DDS                     Cyclone DDS
              |                             |
              +--------------+--------------+
                             |
                            DDS
                             |
                           RTPS
                             |
                 +-----------+-----------+
                 |                       |
                UDP                    SHM
                 |                       |
                 +-----------+-----------+
                             |
                         NETWORK
                             |
              +--------------+--------------+
              |                             |
          Ethernet                         Wi-Fi
              |                             |
          Robot A                       Robot B


Robot data pipeline:

Sensor
  -> Driver
  -> ROS message
  -> Timestamp
  -> TF
  -> Filtering / perception
  -> State estimation
  -> SLAM / localization
  -> Planning
  -> Controller
  -> ros2_control
  -> Hardware
```

---

# Study status

Legend:

- [ ] Not started
- [~] Studying
- [x] Completed
- [!] Needs revision

| Area | Status | Priority |
|---|---:|---:|
| Linux | [ ] | High |
| C++ | [ ] | High |
| Networking | [ ] | High |
| ROS 2 core | [ ] | High |
| Interfaces | [ ] | High |
| Actions | [ ] | High |
| Executors | [ ] | High |
| ROSIDL | [ ] | High |
| RCL / RMW | [ ] | High |
| DDS | [ ] | Critical |
| RTPS | [ ] | Critical |
| Fast DDS | [ ] | Critical |
| Cyclone DDS | [ ] | Critical |
| QoS | [ ] | Critical |
| DDS discovery | [ ] | Critical |
| ROS 2 networking | [ ] | Critical |
| Composition / IPC | [ ] | High |
| Real-time | [ ] | High |
| Security / SROS2 | [ ] | High |
| TF2 | [ ] | High |
| URDF / Xacro | [ ] | High |
| ros2_control | [ ] | Critical |
| Perception | [ ] | Medium |
| State estimation | [ ] | High |
| Sensor fusion | [ ] | High |
| SLAM | [ ] | High |
| Navigation / Nav2 | [ ] | High |
| Behavior Trees | [ ] | High |
| Planning | [ ] | Medium |
| Control | [ ] | High |
| Simulation | [ ] | Medium |
| Multi-robot systems | [ ] | Medium |
| micro-ROS | [ ] | Medium |
| Research methodology | [ ] | High |

---

# Recommended study order

## Phase 0 — Engineering foundations

See `00-prerequisites/`

- Linux
- C++
- Python
- Git
- CMake
- mathematics
- linear algebra
- probability
- networking

## Phase 1 — ROS 2 application layer

See `01-ros2-foundations/`

- Nodes
- Topics
- Services
- Actions
- Parameters
- Launch
- Packages
- Interfaces
- Executors
- CLI
- rosbag2
- lifecycle

## Phase 2 — ROS 2 internals

See `02-ros2-internals/`

```text
rclcpp/rclpy
     |
     v
    rcl
     |
     v
    rmw
     |
     v
middleware implementation
```

Study:

- rclcpp
- rcl
- rmw
- rosidl
- IDL
- type support
- generated code
- serialization
- CDR
- memory ownership

## Phase 3 — Actions and execution

See `03-actions/` and `04-executors/`

Study:

- custom `.action`
- action server
- action client
- goals
- result
- feedback
- cancellation
- goal handles
- asynchronous execution
- callback groups
- executors
- wait sets
- futures
- deadlocks
- race conditions

## Phase 4 — DDS and middleware

See `05-dds/` and `06-dds-implementations/`

Study:

- DDS architecture
- Domain
- DomainParticipant
- Topic
- Publisher
- Subscriber
- DataWriter
- DataReader
- QoS
- discovery
- SPDP
- SEDP
- RTPS
- GUIDs
- sequence numbers
- heartbeat
- ACKNACK
- fragmentation
- multicast
- unicast
- discovery servers

Then compare:

- Fast DDS
- Cyclone DDS

## Phase 5 — QoS and networking

See `07-qos/` and `08-networking/`

Study:

- reliability
- durability
- history
- depth
- deadline
- lifespan
- liveliness
- QoS compatibility
- IPv4
- IPv6
- subnetting
- routing
- UDP
- TCP
- multicast
- sockets
- firewalls
- Wireshark
- tcpdump

## Phase 6 — Performance, real-time and security

See `09-performance/`, `10-realtime/`, `11-security/`

Study:

- intra-process communication
- composition
- shared memory
- zero-copy
- loaned messages
- memory allocation
- latency
- jitter
- tracing
- real-time scheduling
- PREEMPT_RT
- CPU affinity
- DDS Security
- SROS2
- certificates
- authentication
- authorization
- encryption

## Phase 7 — Robot system engineering

See `12-robot-system/` and `13-ros2-control/`

- TF2
- coordinate frames
- URDF
- Xacro
- robot_state_publisher
- lifecycle nodes
- diagnostics
- rosbag2
- simulation time
- ros2_control
- hardware interfaces
- controllers
- controller_manager

## Phase 8 — Robotics algorithms

See `14-perception/` through `20-simulation/`

- camera models
- OpenCV
- LiDAR
- point clouds
- PCL
- object detection
- state estimation
- EKF
- UKF
- sensor fusion
- SLAM
- localization
- planning
- Nav2
- Behavior Trees
- control
- simulation

## Phase 9 — Distributed and embedded robotics

See `21-multi-robot/` and `22-micro-ros/`

- namespaces
- DDS domains
- fleet communication
- multi-robot discovery
- coordination
- XRCE-DDS
- micro-ROS
- embedded systems

## Phase 10 — Research and projects

See:

- `23-research/`
- `24-labs/`
- `25-projects/`

---

# The critical mental model

When a ROS 2 topic is not working, do not immediately assume it is a "ROS topic problem".

Debug down the stack:

```text
Application
   |
ROS API
   |
rclcpp / rclpy
   |
rcl
   |
RMW
   |
DDS
   |
Discovery
   |
QoS matching
   |
RTPS
   |
UDP / SHM
   |
Network interface
   |
Routing / firewall / multicast
```

---

# First practical sequence

Before moving into SLAM or Nav2, complete these labs:

1. Custom message
2. Custom service
3. Custom action
4. Action cancellation
5. Action feedback
6. Multi-threaded executor
7. Callback-group experiment
8. Intentional callback deadlock
9. QoS incompatibility
10. Fast DDS discovery
11. Cyclone DDS discovery
12. Two-machine ROS 2 network
13. Wireshark RTPS capture
14. Multicast failure experiment
15. Unicast discovery experiment
16. Fast DDS Discovery Server
17. ROS 2 security
18. Composition
19. Intra-process communication
20. Shared-memory communication
21. TF2 tree
22. Sensor fusion
23. SLAM
24. Nav2
25. Full autonomous robot

---

# Key source-code repositories

- ROS 2: https://github.com/ros2/ros2
- ROS 2 design: https://github.com/ros2/design
- rclcpp: https://github.com/ros2/rclcpp
- rcl: https://github.com/ros2/rcl
- rmw: https://github.com/ros2/rmw
- rosidl: https://github.com/ros2/rosidl
- Fast DDS RMW: https://github.com/ros2/rmw_fastrtps
- Cyclone DDS RMW: https://github.com/ros2/rmw_cyclonedds
- ROS 2 examples: https://github.com/ros2/examples
- ros2_control: https://github.com/ros-controls/ros2_control
- Nav2: https://github.com/ros-navigation/navigation2
- BehaviorTree.CPP: https://github.com/BehaviorTree/BehaviorTree.CPP
- book_ros2: https://github.com/fmrico/book_ros2
- ROS 2 Zero to Robot: https://github.com/Pouya-Mansournia/ros2-zero-to-robot

---

# Official documentation

- ROS 2 docs: https://docs.ros.org/
- ROS 2 Rolling docs: https://docs.ros.org/en/rolling/
- ROS 2 design: https://design.ros2.org/
- ROS package index: https://index.ros.org/
- ROS REP repository: https://github.com/ros-infrastructure/rep
- Fast DDS: https://fast-dds.docs.eprosima.com/
- Cyclone DDS: https://cyclonedds.io/docs/
- ros2_control: https://control.ros.org/
- Nav2: https://docs.nav2.org/
- BehaviorTree.CPP: https://www.behaviortree.dev/
- Modern Robotics: https://modernrobotics.northwestern.edu/

---

# Important references

See `REFERENCES.md` for the full library.

Core references:

- ROS 2 official documentation
- ROS 2 Design
- OMG DDS specification
- OMG DDSI-RTPS specification
- Fast DDS documentation
- Cyclone DDS documentation
- Modern Robotics
- Computer Networking: Principles, Protocols and Practice
- Probabilistic Robotics
- robotics research papers

---

# Personal notes

Use `NOTES.md` for short daily notes.

Use `QUESTIONS.md` for questions you cannot currently answer.

Use `GLOSSARY.md` for terminology.

Use `PROGRESS.md` for study tracking.

Use `LABS.md` to record experiments.

Use `PROJECTS.md` to track larger projects.

---

# Definition of "I know this"

A topic is not considered complete merely because I can use its API.

I consider a topic understood when I can:

- Explain it without documentation.
- Draw its architecture.
- Explain the internal data flow.
- Implement a minimal example.
- Diagnose a failure.
- Explain important performance implications.
- Explain important security implications.
- Relate it to a real robot.
- Read the relevant source code.
- Read the relevant specification or research paper.
- Modify the implementation safely.
