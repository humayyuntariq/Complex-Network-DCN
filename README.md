# Abstract

This report provides a detailed explanation of the design and setup of a computer network for a hypothetical college environment. The design combines multiple network topologies—star, bus, ring, and mesh—to address diverse requirements. Subnetting is used to efficiently manage IP addresses, while the OSPF (Open Shortest Path First) protocol ensures seamless communication between the different local networks. Network analysis and troubleshooting are performed using tools like Cisco Packet Tracer.

# Introduction

Modern organizations require networks that are flexible, efficient, and capable of addressing a variety of needs. This report focuses on creating a reliable network for a college campus, with different buildings using specific topologies tailored to their unique requirements. Subnetting ensures effective IP address allocation, while dynamic routing simplifies communication across subnets. The report also highlights how tools like Wireshark and Cisco Packet Tracer can help analyze and optimize the network's performance.

# Cisco Packet Tracer

For the design and development of the project, Cisco Packet Tracer is used as the main tool. It is free and provided by Cisco, offering comprehensive networking simulation capabilities. Packet Tracer is renowned for its ease of use, simplicity, real-time simulation, and support for a wide range of Cisco devices.

## Reasons for Using Cisco Packet Tracer

1. **Student-Friendly Design:** Cisco Packet Tracer is designed for students learning networking.
2. **Ease of Use:** Its simple and intuitive interface helps students grasp network concepts and device configurations.
3. **Drag-and-Drop Interface:** This feature simplifies network design and development for beginners.
4. **Low Resource Requirement:** It is less resource-intensive compared to tools like GNS3.
5. **Real-Time Simulation:** Visualizing network activities in real-time enhances understanding.
6. **Versatility:** Supports multiple network devices and protocols.
7. **Collaboration:** Allows single and multi-user activities.

# Advantages and Disadvantages of Cisco Packet Tracer

## Advantages

- Beginner-friendly and easy to use.
- Runs on low-specification systems.
- Provides real-time packet and protocol visualization.
- Offers learning resources via Cisco's online academy.
- Enhances understanding of network activities through visualization.

## Disadvantages

- Limited to Cisco devices.
- Cannot simulate OS-level tasks like GNS3.
- Lacks features for large-scale network simulations.
- Cannot replicate real-world network complexities.

# Comparison with Other Networking Simulation Tools

## GNS3 vs Cisco Packet Tracer

| Feature                  | Cisco Packet Tracer          | GNS3                        |
|--------------------------|-----------------------------|-----------------------------|
| User-friendly            | ✔                          | ✖                           |
| Low resource requirement | ✔                          | ✖                           |
| Real-time simulation     | ✔                          | ✔                           |
| Advanced features        | ✖                          | ✔                           |
| Learning curve           | Low                        | Steep                       |

## EVE-NG vs Cisco Packet Tracer

| Feature                  | Cisco Packet Tracer          | EVE-NG                      |
|--------------------------|-----------------------------|-----------------------------|
| User-friendly            | ✔                          | ✖                           |
| Low resource requirement | ✔                          | ✖                           |
| Advanced scenarios       | ✖                          | ✔                           |
| Collaboration            | ✖                          | ✔                           |

## NS3 vs Cisco Packet Tracer

| Feature                  | Cisco Packet Tracer          | NS3                         |
|--------------------------|-----------------------------|-----------------------------|
| User-friendly            | ✔                          | ✖                           |
| Low resource requirement | ✔                          | ✔                           |
| GUI                      | ✔                          | ✖                           |
| Research suitability     | ✖                          | ✔                           |

# Network Design

## Topologies

- **Star Topology:** Used in administrative buildings for centralized control.
- **Bus Topology:** Deployed in older sections to minimize costs.
- **Ring Topology:** Applied in computer labs for sequential data flow.
- **Mesh Topology:** Implemented in critical areas for redundancy.

### Star Topology

In Cisco Packet Tracer, a star topology is created using one switch and five PCs, connected via copper straight-through cables.

### Mesh Topology

Devices have dedicated point-to-point connections. Four devices are connected using switches to achieve high data transfer rates and privacy.

### Ring Topology

Devices connect to their immediate neighbors using switches, ensuring sequential data flow.

### Bus Topology

A main cable connects multiple PCs using hubs and switches for cost-effective functionality.

# Complex Network Architecture

## Network Addressing and Subnetting

The network uses the 192.168.12.0/24 range, divided into 16 subnets with a subnet mask of 255.255.255.240, supporting up to 14 usable host addresses per subnet.

### Example Subnets

| Subnet ID     | Host IP Range      | Broadcast Address |
|---------------|--------------------|-------------------|
| 192.168.12.0  | 192.168.12.1-14   | 192.168.12.15     |
| 192.168.12.16 | 192.168.12.17-30  | 192.168.12.31     |

## Router and PC Configuration

- **Router Ports:** The first IP address in each subnet is reserved for the router interface.
- **PCs:** Each PC is assigned the next available IP address in the subnet, using the router’s IP as the default gateway.

# Technologies for Network Architecture

- **Routers:** Equipped with additional Fast Ethernet modules for sufficient ports.
- **Switches:** Used for interconnecting devices.
- **PCs:** Assigned specific IP addresses based on the subnet.

# Conclusion

The network design integrates various topologies and efficient subnetting, ensuring scalability, flexibility, and robust performance. Cisco Packet Tracer serves as an effective tool for visualization and testing, making the design process accessible and educational.
