# Questions I Need to Answer

Use this as an active research notebook.

## ROS 2 architecture

- [ ] What exactly happens inside `publish()`?
- [ ] What does rclcpp provide that rcl does not?
- [ ] What does RMW abstract?
- [ ] How does ROSIDL generate types?
- [ ] What is type support?
- [ ] Where does serialization happen?
- [ ] What is CDR?

## Actions

- [ ] How is an action represented internally?
- [ ] How are goal requests handled?
- [ ] How does cancellation work?
- [ ] How do action feedback and results travel?
- [ ] How should concurrent goals be handled?

## Executors

- [ ] What exactly does `spin()` do?
- [ ] What is a wait set?
- [ ] How does a MultiThreadedExecutor schedule callbacks?
- [ ] How can callback groups deadlock?
- [ ] How do futures interact with executors?

## DDS

- [ ] What is a DomainParticipant?
- [ ] What is a DataWriter?
- [ ] What is a DataReader?
- [ ] How does SPDP work?
- [ ] How does SEDP work?
- [ ] How are endpoints matched?
- [ ] What is a GUID?
- [ ] What are RTPS DATA/HEARTBEAT/ACKNACK/GAP messages?
- [ ] How does reliable delivery work?
- [ ] How does fragmentation work?

## Networking

- [ ] Why does multicast matter to DDS discovery?
- [ ] What happens when multicast is blocked?
- [ ] Which interfaces does DDS use?
- [ ] How does a firewall affect ROS 2?
- [ ] How can Wireshark prove whether discovery is working?
- [ ] How can tcpdump distinguish discovery from data traffic?

## Performance

- [ ] Where are copies made?
- [ ] When is serialization performed?
- [ ] What is intra-process communication?
- [ ] What is shared-memory transport?
- [ ] What are loaned messages?
- [ ] What does zero-copy really mean?
- [ ] How do I measure latency and jitter?

## Security

- [ ] How does DDS Security authenticate participants?
- [ ] What is a CA?
- [ ] What is governance?
- [ ] What are permissions?
- [ ] How does SROS2 create and use enclaves?
- [ ] What exactly gets encrypted?

## Robotics

- [ ] How does TF2 resolve transforms at a timestamp?
- [ ] Why does SLAM drift?
- [ ] How does loop closure correct drift?
- [ ] How does EKF sensor fusion work?
- [ ] How do costmaps represent obstacles?
- [ ] How does Nav2 connect planning to control?
- [ ] How does a Behavior Tree invoke a ROS action?

## Hardware

- [ ] How does ros2_control communicate with real hardware?
- [ ] What is a SystemInterface?
- [ ] What is the real-time update loop?
- [ ] How do CAN/EtherCAT/serial drivers fit into the architecture?
