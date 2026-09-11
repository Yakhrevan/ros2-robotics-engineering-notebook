# ROS 2 / Robotics Glossary

| Term | Meaning | Layer |
|---|---|---|
| ROS 2 | Robot software libraries and tools | System |
| Node | Logical ROS computation unit | ROS |
| Topic | Named pub/sub communication channel | ROS |
| Service | Request/response communication | ROS |
| Action | Long-running goal/feedback/result communication | ROS |
| rclcpp | C++ ROS client library | ROS |
| rclpy | Python ROS client library | ROS |
| rcl | Common ROS client abstraction | ROS |
| RMW | ROS Middleware Interface | Middleware |
| rosidl | ROS interface definition/generation system | Interface |
| IDL | Interface Definition Language | Interface |
| Type support | Middleware/language type adaptation | Interface |
| CDR | Common Data Representation | Serialization |
| DDS | Data Distribution Service | Middleware |
| RTPS | Real-Time Publish-Subscribe protocol | Protocol |
| Domain | DDS communication partition | DDS |
| DomainParticipant | DDS entity participating in a domain | DDS |
| DataWriter | DDS data publication endpoint | DDS |
| DataReader | DDS data subscription endpoint | DDS |
| QoS | Quality of Service policies | DDS |
| SPDP | Simple Participant Discovery Protocol | DDS |
| SEDP | Simple Endpoint Discovery Protocol | DDS |
| GUID | Globally Unique Identifier | DDS/RTPS |
| ACKNACK | RTPS reliability control message | RTPS |
| HEARTBEAT | RTPS writer status message | RTPS |
| Executor | ROS callback scheduling/execution mechanism | ROS |
| Callback Group | Controls callback concurrency | ROS |
| TF2 | Transform and coordinate-frame system | Robotics |
| URDF | Robot model description format | Robotics |
| Xacro | XML macro system commonly used for URDF | Robotics |
| ros2_control | ROS 2 hardware/control framework | Control |
| EKF | Extended Kalman Filter | Estimation |
| UKF | Unscented Kalman Filter | Estimation |
| SLAM | Simultaneous Localization and Mapping | Robotics |
| ICP | Iterative Closest Point | Perception/SLAM |
| NDT | Normal Distributions Transform | Perception/SLAM |
| LIO | LiDAR-Inertial Odometry | SLAM |
| VIO | Visual-Inertial Odometry | SLAM |
| Nav2 | ROS 2 navigation framework | Navigation |
| Costmap | Spatial representation used for navigation | Navigation |
| Behavior Tree | Hierarchical behavior execution model | Planning |
| SROS2 | ROS 2 security tooling | Security |
| PREEMPT_RT | Linux real-time kernel technology | Real-time |
| SHM | Shared memory | Transport |
| IPC | Inter-process communication | OS |
| LTTng | Linux tracing framework | Observability |
| rosbag2 | ROS 2 data recording/replay system | Tooling |
| micro-ROS | ROS 2 ecosystem for microcontrollers | Embedded |
| XRCE-DDS | DDS protocol designed for constrained devices | Embedded |
