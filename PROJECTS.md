# Progressive Projects

## Project 1 — ROS 2 Interface Laboratory

Build:
- custom message
- custom service
- custom action
- action client/server
- feedback
- cancellation

Goal:
Understand the complete ROS interface lifecycle.

---

## Project 2 — ROS 2 Execution Laboratory

Build:
- timers
- subscriptions
- services
- actions
- multiple callback groups
- MultiThreadedExecutor

Measure:
- callback latency
- concurrency
- deadlock behavior

---

## Project 3 — Distributed ROS 2 Robot

Two computers:

```text
Computer A
  sensors
     |
     +---- ROS 2 / DDS ----+
                            |
Computer B                  |
  perception/navigation <---+
```

Implement:
- Ethernet
- DDS discovery
- QoS
- Wireshark
- failure recovery

---

## Project 4 — DDS Network Analyzer

Build a test environment that records:
- discovery traffic
- participant discovery
- endpoint discovery
- topic data
- reliability traffic

Analyze:
- SPDP
- SEDP
- DATA
- HEARTBEAT
- ACKNACK

---

## Project 5 — Secure ROS 2 Robot

Implement:
- keystore
- certificates
- authentication
- authorization
- encrypted communication

Test:
- authorized publisher
- authorized subscriber
- unauthorized node
- denied topic access

---

## Project 6 — Sensor Fusion Robot

Sensors:
- IMU
- wheel odometry
- GNSS or simulated GNSS

Build:
- state estimator
- EKF
- TF2
- covariance analysis

---

## Project 7 — LiDAR SLAM Robot

Pipeline:

```text
LiDAR
  |
scan
  |
preprocessing
  |
odometry / scan matching
  |
pose estimation
  |
loop closure
  |
pose graph
  |
map
```

---

## Project 8 — Autonomous Navigation Robot

Pipeline:

```text
Sensors
  |
TF2
  |
Localization
  |
Costmap
  |
Global Planner
  |
Controller
  |
Behavior Tree
  |
cmd_vel
  |
ros2_control
  |
Hardware
```

---

## Project 9 — Production ROS 2 Robot

Requirements:
- lifecycle
- diagnostics
- rosbag2
- tracing
- QoS
- DDS configuration
- security
- hardware abstraction
- watchdogs
- recovery
- logging
- performance monitoring

---

## Project 10 — Distributed Multi-Robot System

Build:
- multiple robots
- namespaces
- discovery strategy
- map sharing
- task allocation
- secure network
- centralized or decentralized coordination
