# ROS 2 & Robotics Deep Study Roadmap

## Stage 0 — Foundations

### Linux
- [ ] Processes
- [ ] Threads
- [ ] Signals
- [ ] IPC
- [ ] Shared memory
- [ ] Filesystems
- [ ] udev
- [ ] systemd
- [ ] permissions
- [ ] sockets
- [ ] scheduling

### C++
- [ ] references
- [ ] pointers
- [ ] smart pointers
- [ ] RAII
- [ ] templates
- [ ] STL
- [ ] move semantics
- [ ] threads
- [ ] mutexes
- [ ] atomics
- [ ] futures
- [ ] condition variables
- [ ] CMake

### Mathematics
- [ ] vectors
- [ ] matrices
- [ ] eigenvalues/eigenvectors
- [ ] coordinate transforms
- [ ] rotation matrices
- [ ] quaternions
- [ ] probability
- [ ] Bayes
- [ ] optimization
- [ ] calculus basics

### Networking
- [ ] OSI model
- [ ] Ethernet
- [ ] MAC
- [ ] ARP
- [ ] IPv4
- [ ] IPv6
- [ ] subnetting
- [ ] routing
- [ ] UDP
- [ ] TCP
- [ ] ICMP
- [ ] multicast
- [ ] sockets
- [ ] firewall
- [ ] Wireshark
- [ ] tcpdump

---

# Stage 1 — ROS 2

- [ ] Workspace
- [ ] Packages
- [ ] Nodes
- [ ] Topics
- [ ] Publishers
- [ ] Subscribers
- [ ] Services
- [ ] Clients
- [ ] Actions
- [ ] Parameters
- [ ] Launch
- [ ] Remapping
- [ ] Namespaces
- [ ] Interfaces
- [ ] rosbag2
- [ ] Lifecycle

---

# Stage 2 — ROS 2 internals

- [ ] rclcpp
- [ ] rclpy
- [ ] rcl
- [ ] rmw
- [ ] rosidl
- [ ] IDL
- [ ] type support
- [ ] generated code
- [ ] introspection
- [ ] serialization
- [ ] CDR
- [ ] memory ownership
- [ ] source-code tracing

---

# Stage 3 — Actions

- [ ] `.action` definition
- [ ] generated interfaces
- [ ] action server
- [ ] action client
- [ ] goal request
- [ ] goal response
- [ ] goal handle
- [ ] feedback
- [ ] result
- [ ] cancellation
- [ ] concurrent goals
- [ ] preemption concepts
- [ ] action QoS
- [ ] action debugging

---

# Stage 4 — Executors

- [ ] executor concept
- [ ] spin()
- [ ] spin_some()
- [ ] SingleThreadedExecutor
- [ ] MultiThreadedExecutor
- [ ] callback groups
- [ ] mutually exclusive
- [ ] reentrant
- [ ] wait sets
- [ ] futures
- [ ] timers
- [ ] callback scheduling
- [ ] race conditions
- [ ] deadlocks
- [ ] starvation

---

# Stage 5 — DDS

- [ ] data-centric pub/sub
- [ ] Domain
- [ ] DomainParticipant
- [ ] Topic
- [ ] Publisher
- [ ] Subscriber
- [ ] DataWriter
- [ ] DataReader
- [ ] QoS
- [ ] discovery
- [ ] SPDP
- [ ] SEDP
- [ ] RTPS
- [ ] GUID
- [ ] sequence numbers
- [ ] heartbeat
- [ ] ACKNACK
- [ ] GAP
- [ ] fragmentation
- [ ] reliability protocol

---

# Stage 6 — Fast DDS / Cyclone DDS

- [ ] Fast DDS architecture
- [ ] Fast DDS QoS
- [ ] Fast DDS XML
- [ ] Fast DDS transports
- [ ] shared memory
- [ ] Discovery Server
- [ ] Fast DDS CLI
- [ ] Cyclone architecture
- [ ] Cyclone configuration
- [ ] multicast
- [ ] unicast peers
- [ ] Cyclone shared memory
- [ ] compare both implementations

---

# Stage 7 — QoS

- [ ] reliability
- [ ] durability
- [ ] history
- [ ] depth
- [ ] deadline
- [ ] lifespan
- [ ] liveliness
- [ ] lease duration
- [ ] offered/requested compatibility
- [ ] sensor QoS
- [ ] action QoS
- [ ] service QoS
- [ ] debugging QoS

---

# Stage 8 — Distributed networking

- [ ] ROS_DOMAIN_ID
- [ ] DDS domains
- [ ] discovery traffic
- [ ] data traffic
- [ ] multicast
- [ ] unicast
- [ ] network interfaces
- [ ] UDP ports
- [ ] routing
- [ ] firewall
- [ ] Wi-Fi limitations
- [ ] Ethernet
- [ ] packet capture
- [ ] Wireshark RTPS
- [ ] tcpdump
- [ ] multi-machine ROS 2

---

# Stage 9 — Performance

- [ ] intra-process communication
- [ ] composition
- [ ] components
- [ ] shared memory
- [ ] zero-copy concepts
- [ ] loaned messages
- [ ] memory allocation
- [ ] serialization cost
- [ ] copies
- [ ] cache behavior
- [ ] CPU utilization
- [ ] latency
- [ ] jitter
- [ ] throughput
- [ ] benchmarking
- [ ] tracing

---

# Stage 10 — Real-time

- [ ] hard vs soft real-time
- [ ] determinism
- [ ] scheduling
- [ ] priorities
- [ ] CPU affinity
- [ ] page faults
- [ ] dynamic allocation
- [ ] mutex behavior
- [ ] lock-free structures
- [ ] PREEMPT_RT
- [ ] ROS 2 real-time
- [ ] control-loop timing

---

# Stage 11 — Security

- [ ] threat model
- [ ] DDS Security
- [ ] SROS2
- [ ] keystore
- [ ] CA
- [ ] certificates
- [ ] authentication
- [ ] authorization
- [ ] governance
- [ ] permissions
- [ ] encryption
- [ ] enclaves
- [ ] secure multi-machine ROS

---

# Stage 12 — Robot systems

- [ ] TF2
- [ ] coordinate frames
- [ ] timestamps
- [ ] transform tree
- [ ] URDF
- [ ] Xacro
- [ ] robot_state_publisher
- [ ] joint_state
- [ ] lifecycle nodes
- [ ] diagnostics
- [ ] rosbag2
- [ ] simulation time
- [ ] clocks

---

# Stage 13 — ros2_control

- [ ] controller_manager
- [ ] hardware interface
- [ ] SystemInterface
- [ ] ActuatorInterface
- [ ] SensorInterface
- [ ] state interfaces
- [ ] command interfaces
- [ ] controllers
- [ ] joint trajectory controller
- [ ] controller lifecycle
- [ ] real-time update loop
- [ ] hardware communication
- [ ] CAN
- [ ] EtherCAT
- [ ] serial
- [ ] custom hardware plugin

---

# Stage 14 — Perception

- [ ] camera geometry
- [ ] intrinsics
- [ ] extrinsics
- [ ] distortion
- [ ] projection
- [ ] OpenCV
- [ ] stereo
- [ ] depth
- [ ] LiDAR
- [ ] point clouds
- [ ] PCL
- [ ] filtering
- [ ] clustering
- [ ] detection
- [ ] segmentation
- [ ] tracking

---

# Stage 15 — State estimation

- [ ] probability
- [ ] Bayes
- [ ] Gaussian
- [ ] covariance
- [ ] motion model
- [ ] measurement model
- [ ] Kalman Filter
- [ ] EKF
- [ ] UKF
- [ ] complementary filter
- [ ] error-state filtering
- [ ] IMU
- [ ] odometry
- [ ] GNSS
- [ ] robot_localization

---

# Stage 16 — SLAM

- [ ] localization vs mapping
- [ ] occupancy grids
- [ ] sensor models
- [ ] odometry
- [ ] scan matching
- [ ] ICP
- [ ] NDT
- [ ] EKF SLAM
- [ ] FastSLAM
- [ ] graph SLAM
- [ ] pose graphs
- [ ] loop closure
- [ ] graph optimization
- [ ] factor graphs
- [ ] LiDAR SLAM
- [ ] visual SLAM
- [ ] VIO
- [ ] LIO
- [ ] IMU preintegration

---

# Stage 17 — Navigation

- [ ] localization
- [ ] costmaps
- [ ] obstacle layer
- [ ] voxel layer
- [ ] inflation
- [ ] footprint
- [ ] global planning
- [ ] local control
- [ ] path tracking
- [ ] recovery
- [ ] lifecycle
- [ ] Nav2 actions
- [ ] Nav2 Behavior Trees

---

# Stage 18 — Behavior Trees

- [ ] Sequence
- [ ] Fallback
- [ ] Parallel
- [ ] Decorator
- [ ] Condition
- [ ] Action
- [ ] SubTree
- [ ] Blackboard
- [ ] Ports
- [ ] asynchronous actions
- [ ] ROS action integration
- [ ] Nav2 BT architecture

---

# Stage 19 — Planning and control

- [ ] kinematics
- [ ] dynamics
- [ ] PID
- [ ] trajectory generation
- [ ] A*
- [ ] Dijkstra
- [ ] RRT
- [ ] RRT*
- [ ] MPC
- [ ] path smoothing
- [ ] trajectory tracking
- [ ] differential drive
- [ ] Ackermann
- [ ] aerial vehicle basics

---

# Stage 20 — Simulation

- [ ] Gazebo
- [ ] physics
- [ ] robot model
- [ ] sensors
- [ ] plugins
- [ ] controllers
- [ ] simulation clock
- [ ] sensor noise
- [ ] domain randomization
- [ ] sim-to-real

---

# Stage 21 — Multi-robot / distributed robotics

- [ ] namespaces
- [ ] DDS domains
- [ ] discovery
- [ ] network segmentation
- [ ] multi-robot TF
- [ ] map sharing
- [ ] fleet management
- [ ] coordination
- [task allocation]
- [ ] distributed planning

---

# Stage 22 — Embedded / micro-ROS

- [ ] micro-ROS architecture
- [ ] XRCE-DDS
- [ ] agent
- [ ] client
- [ ] transports
- [ ] RTOS
- [ ] memory constraints
- [ ] MCU integration
