# ROS 2 & Robotics Reference Library

> Prefer official documentation and primary sources. Use third-party tutorials to clarify concepts, not as the final authority.

## 1. ROS 2

### Official
- ROS 2 documentation: https://docs.ros.org/
- Rolling documentation: https://docs.ros.org/en/rolling/
- ROS 2 GitHub: https://github.com/ros2
- ROS 2 repository: https://github.com/ros2/ros2
- ROS 2 examples: https://github.com/ros2/examples
- ROS package index: https://index.ros.org/
- ROS design: https://design.ros2.org/
- ROS design GitHub: https://github.com/ros2/design
- ROS Enhancement Proposals: https://github.com/ros-infrastructure/rep

### Book / practical material
- A Concise Introduction to Robot Programming with ROS 2:
  https://github.com/fmrico/book_ros2
- ROS 2 Zero to Robot:
  https://github.com/Pouya-Mansournia/ros2-zero-to-robot

---

# 2. ROS 2 internals

- rclcpp: https://github.com/ros2/rclcpp
- rcl: https://github.com/ros2/rcl
- rmw: https://github.com/ros2/rmw
- rosidl: https://github.com/ros2/rosidl
- rmw_fastrtps: https://github.com/ros2/rmw_fastrtps
- rmw_cyclonedds: https://github.com/ros2/rmw_cyclonedds
- ROS 2 internal interfaces documentation:
  https://docs.ros.org/en/rolling/Concepts/About-Internal-Interfaces.html

Study questions:
- What does rclcpp add over rcl?
- What does rcl expose to RMW?
- What is an rmw implementation?
- How is a ROS interface turned into generated code?
- Where is type support selected?
- Where is serialization performed?

---

# 3. Actions

- Actions tutorial:
  https://docs.ros.org/en/rolling/Tutorials/Intermediate/Writing-an-Action-Server-Client.html
- Topics/services/actions:
  https://docs.ros.org/en/rolling/How-To-Guides/Topics-Services-Actions.html

Study:
- .action syntax
- generated Goal/Result/Feedback
- action server
- action client
- goal handles
- cancellation
- feedback
- result
- action QoS
- concurrency

---

# 4. Executors

- Executors:
  https://docs.ros.org/en/rolling/Concepts/Intermediate/About-Executors.html
- Callback groups:
  https://docs.ros.org/en/rolling/How-To-Guides/Using-callback-groups.html

Study:
- spin
- wait sets
- SingleThreadedExecutor
- MultiThreadedExecutor
- callback groups
- reentrant groups
- mutually exclusive groups
- deadlocks
- race conditions

---

# 5. DDS

### OMG primary specifications
- OMG DDS:
  https://www.omg.org/spec/DDS
- OMG DDSI-RTPS:
  https://www.omg.org/spec/DDSI-RTPS
- OMG DDS Security:
  https://www.omg.org/spec/DDS-SECURITY

### Concepts
- Domain
- DomainParticipant
- Topic
- Publisher
- Subscriber
- DataWriter
- DataReader
- QoS
- discovery

### RTPS
Study:
- RTPS header
- GUID
- Entity ID
- locator
- sequence number
- DATA
- DATA_FRAG
- HEARTBEAT
- ACKNACK
- GAP
- SPDP
- SEDP

---

# 6. Fast DDS

- Documentation: https://fast-dds.docs.eprosima.com/
- GitHub: https://github.com/eProsima/Fast-DDS
- Fast DDS CLI: https://fast-dds.docs.eprosima.com/en/latest/fastddscli/cli/cli.html
- Fast DDS-Gen: https://fast-dds.docs.eprosima.com/en/latest/fastddsgen/usage/usage.html

Study:
- architecture
- QoS
- XML profiles
- transports
- UDP
- TCP
- shared memory
- discovery
- Discovery Server
- security
- performance
- Fast DDS Monitor / CLI where applicable

---

# 7. Cyclone DDS

- Documentation: https://cyclonedds.io/docs/
- Main docs: https://cyclonedds.io/docs/cyclonedds/latest/
- GitHub: https://github.com/eclipse-cyclonedds/cyclonedds

Study:
- DDSI
- configuration
- discovery
- SPDP
- SEDP
- multicast
- unicast
- peers
- network interfaces
- shared memory
- security
- tracing

---

# 8. QoS

- ROS 2 QoS:
  https://docs.ros.org/en/rolling/Concepts/Intermediate/About-Quality-of-Service-Settings.html

Study:
- Reliability
- Durability
- History
- Depth
- Deadline
- Lifespan
- Liveliness
- QoS compatibility
- sensor profiles
- action/service QoS

---

# 9. Networking

### Open textbook
- Computer Networking: Principles, Protocols and Practice:
  https://cnp3book.info.ucl.ac.be/

Study:
- Ethernet
- MAC
- ARP
- IPv4
- IPv6
- subnetting
- routing
- UDP
- TCP
- ICMP
- multicast
- sockets
- NAT
- firewall

### Tools
- Wireshark: https://www.wireshark.org/
- tcpdump: https://www.tcpdump.org/

ROS/DDS experiments:
- capture discovery
- capture RTPS data
- inspect UDP
- identify multicast
- test firewall effects
- test multiple interfaces

---

# 10. Performance and real-time

### ROS 2
- ROS 2 tracing:
  https://docs.ros.org/en/rolling/Tutorials/Advanced/ROS2-Tracing-Trace-and-Analyze.html
- Real-time programming:
  https://docs.ros.org/en/rolling/Tutorials/Demos/Real-Time-Programming.html

Study:
- latency
- jitter
- executor scheduling
- memory allocation
- page faults
- thread priority
- CPU affinity
- PREEMPT_RT
- tracing
- intra-process
- composition
- shared memory
- zero-copy
- loaned messages

---

# 11. Security

- ROS 2 Security:
  https://docs.ros.org/en/rolling/Tutorials/Advanced/Security/Introducing-ROS2-Security.html
- ROS 2 Security tutorial:
  https://docs.ros.org/en/rolling/Tutorials/Advanced/Security/
- OMG DDS Security:
  https://www.omg.org/spec/DDS-SECURITY

Study:
- PKI
- CA
- certificates
- authentication
- authorization
- governance
- permissions
- encryption
- enclaves
- threat modeling

---

# 12. Robot system

### TF2
- https://docs.ros.org/en/rolling/Tutorials/Intermediate/Tf2/Tf2-Main.html

### URDF
- https://docs.ros.org/en/rolling/Tutorials/Intermediate/URDF/URDF-Main.html

### ros2_control
- https://control.ros.org/
- https://github.com/ros-controls/ros2_control

Study:
- TF tree
- timestamps
- coordinate frames
- URDF
- Xacro
- robot_state_publisher
- joint states
- lifecycle
- diagnostics
- rosbag2
- controller_manager
- hardware interfaces
- command/state interfaces

---

# 13. Perception

### OpenCV
- https://opencv.org/
- https://docs.opencv.org/

### PCL
- https://pointclouds.org/
- https://github.com/PointCloudLibrary/pcl

Study:
- camera model
- intrinsics
- extrinsics
- distortion
- projection
- stereo
- depth
- LiDAR
- point clouds
- filtering
- segmentation
- clustering
- object detection
- tracking

---

# 14. Robotics mathematics

### Modern Robotics
- https://modernrobotics.northwestern.edu/
- GitHub/code: https://github.com/NxRLab/ModernRobotics

Study:
- rigid-body motion
- rotations
- homogeneous transforms
- exponential coordinates
- forward kinematics
- inverse kinematics
- Jacobians
- dynamics
- trajectory generation
- control

---

# 15. State estimation

Study:
- probability
- Bayes
- Gaussian distributions
- covariance
- state-space models
- Kalman filter
- EKF
- UKF
- complementary filters
- error-state filters
- IMU
- wheel odometry
- GNSS
- sensor fusion

ROS package:
- robot_localization:
  https://github.com/cra-ros-pkg/robot_localization

---

# 16. SLAM

Study before packages:
- probability
- transformations
- odometry
- sensor models
- state estimation
- optimization
- graph theory

Then:
- occupancy grids
- EKF SLAM
- FastSLAM
- Graph SLAM
- scan matching
- ICP
- NDT
- pose graphs
- loop closure
- factor graphs
- LiDAR SLAM
- visual SLAM
- VIO
- LIO
- IMU preintegration

Useful projects:
- GTSAM: https://github.com/borglab/gtsam
- Cartographer: https://github.com/cartographer-project/cartographer
- RTAB-Map: https://github.com/introlab/rtabmap
- SLAM Toolbox: https://github.com/SteveMacenski/slam_toolbox

---

# 17. Navigation

- Nav2 docs: https://docs.nav2.org/
- Nav2 GitHub: https://github.com/ros-navigation/navigation2

Study:
- localization
- costmaps
- global planning
- local control
- obstacle layers
- inflation
- footprint
- recovery
- lifecycle
- navigation actions
- Behavior Trees

---

# 18. Behavior Trees

- BehaviorTree.CPP:
  https://www.behaviortree.dev/
- GitHub:
  https://github.com/BehaviorTree/BehaviorTree.CPP

Study:
- Sequence
- Fallback
- Reactive nodes
- Parallel
- Decorators
- Conditions
- Actions
- SubTrees
- Blackboard
- Ports
- asynchronous execution
- ROS action integration

---

# 19. Planning and control

Study:
- Dijkstra
- A*
- RRT
- RRT*
- PRM
- path smoothing
- trajectory generation
- PID
- pure pursuit
- Stanley
- MPC
- kinematics
- dynamics

---

# 20. Simulation

- Gazebo: https://gazebosim.org/
- Gazebo GitHub: https://github.com/gazebosim
- ROS/Gazebo integration:
  https://github.com/ros-controls/gz_ros2_control

Study:
- physics
- sensors
- noise
- plugins
- controllers
- simulation time
- sim-to-real
- domain randomization

---

# 21. Multi-robot systems

Study:
- ROS namespaces
- DDS domains
- discovery
- network segmentation
- map sharing
- multi-robot TF
- task allocation
- fleet management
- distributed planning
- security

---

# 22. micro-ROS

- Documentation: https://micro.ros.org/docs/
- GitHub: https://github.com/micro-ROS

Study:
- architecture
- XRCE-DDS
- agent
- client
- transports
- embedded memory
- RTOS
- MCU integration

---

# 23. Research

### General
- Robotics: Science and Systems:
  https://roboticsconference.org/
- arXiv:
  https://arxiv.org/

Search terms:
- ROS 2 DDS
- DDS RTPS
- ROS 2 real-time
- ROS 2 security
- LiDAR SLAM
- visual SLAM
- LIO
- VIO
- sensor fusion
- autonomous navigation
- multi-robot systems

### Research reading workflow

```text
Survey
  ->
Foundational paper
  ->
Modern paper
  ->
Implementation
  ->
Experiment
  ->
Own notes
```
