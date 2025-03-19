# Week 1: Cloud and Edge Computing

## Lecture 1: Overview of Cloud Computing

This summary covers the key concepts from the "Lecture 01 - Overview of Cloud Computing" video.

### 1. Cloud Computing Hype and Growth

- Forecasting agencies predicted significant growth in cloud computing revenue (e.g., exceeding $150 billion by 2013).
- This led to increased investment and adoption by businesses and governments.

### 2. Evolution from Distributed Systems

- Growing demand for scalable computing and the rise of virtualization drove cloud computing's evolution.
- It emerged from earlier distributed systems like clusters, grids, and peer-to-peer networks.
- Cloud computing addresses large-scale problems and massive datasets.

### 3. Features of Cloud Services

- Massive Scale:
    - WUE = Annual Water Usage/IT Equipment Energy (low is good)
    - PUE = Total Facility Power/ IT Equipment Power (low is good)
- On-demand access
    - **Hardware as a Service(HaaS)**: Provides barebone hardware and machines.
    - **Infrastructure as a Service (IaaS):** Provides fundamental computing resources (virtual machines, storage, networking, load-balancing).
    - **Platform as a Service (PaaS):** Offers a platform for developers to build and deploy applications(Execution Runtime, DBs, Web Servers, Dev Tools)
    - **Software as a Service (SaaS):** Delivers applications over the internet.
    
![image](https://github.com/user-attachments/assets/86162dc3-8d54-4bc7-8153-0c84c8487fcc)

    
- Data Intensive:
    - Typically store data at datacenters and use compute nodes nearby. The focus therefore shifts from computation to data.
    - CPU utilization no longer the most important resource metric, instead I/O is (disk and/or network).
- New Cloud Programming Paradigms
    - MapReduce
    - Hadoop
    - NoSQL
 ![image](https://github.com/user-attachments/assets/5c1785dd-80ae-4c38-92f1-d31fd6d6861e)


- Moore’s law indicates that processor speed doubles every 18 months.

- Gilder’s law indicates that network bandwidth has doubled each year in the past.
### 4. Advantages of Cloud Computing

- **Cost Savings:** Reduced IT operational costs, no upfront hardware investments, pay-as-you-go pricing.
- **Scalability and Flexibility:** Easily scale resources up or down based on demand.
- **Increased Efficiency:** Improved resource utilization through shared infrastructure.
- **Improved Collaboration:** Enhanced collaboration and data sharing.

### 5. Cloud Computing Technologies

- **Virtualization:** Enables multiple virtual machines to run on a single physical server.
- **Hypervisors:** Manage and isolate virtual machines, enabling efficient resource allocation.

### 6. Public vs. Private Clouds

- **Public Clouds:** Provided by third-party vendors and accessible to the general public.
- **Private Clouds:** Built and maintained within an organization's data center.

### 7. Key Features of Cloud Computing

- **Massive Scale:** Large data centers with thousands of servers.
- **On-Demand Access:** Pay-as-you-go pricing and flexible resource provisioning.
- **Data-Intensive Nature:** Designed to handle large volumes of data.
- **New Cloud Programming Paradigms:** Frameworks like MapReduce and Hadoop.

### 8. Decision to Outsource or Own

- Factors to consider: cost, scalability, security, and control requirements.

## Lecture 2 : Cloud Computing and its Limitations to Support Low Latency and RTT

### **Key Topics Covered:**

- Understanding of today’s cloud scenario
- Different objectives of cloud computing
- Limitations of traditional cloud models
- Need for edge computing

### **Current State of Cloud Computing**

1. **Highly Centralized Architecture**
    - Cloud computing relies on a centralized infrastructure where data and compute resources are located far from end users.
    - This resembles the client-server model from the 90s.
2. **Compute Evolution**
    - The traditional cloud relied on Virtual Machines (VMs).
    - The current trend is shifting towards **containers**, which are more lightweight and efficient.
3. **Storage Enhancements**
    - Traditional cloud storage is complemented by **Content Delivery Networks (CDN)**.
    - Data is cached at various locations to improve response times.
4. **Programmable Network Stack**
    - Modern networks use **Software-Defined Networking (SDN)** and service mesh architectures.
    - Enables better traffic routing, security, and scalability.

### **Challenges of Cloud for IoT and AI**

1. **Latency Issues**
    - Cloud computing has high Round-Trip Time (RTT), making real-time processing difficult.
    - Critical applications (e.g., autonomous vehicles) require **low-latency responses**, which the cloud cannot always provide.
2. **Bandwidth Constraints**
    - Transmitting large amounts of data to cloud data centers consumes bandwidth and increases costs.
3. **Security Concerns**
    - Sensitive data may need to be stored locally rather than in the cloud.
4. If edge devices have connectivity issues or no internet connection it can not perform well.

### Edge Computing

- Edge computing makes the cloud truly distributed.
- Moves core cloud services closer to the origin of data
- Edge Mimics public cloud platform capabilities
- Delivers storage, compute, and network services locally.
- Reduces the latency by avoiding the round trip to the cloud
- Brings in data sovereignty by keeping data where it actually
belongs, savings on cloud and bandwidth usages

### Functionality of Edge

● Data Ingestion and M2M Brokers
● Object Storage
● Functions as a Service
● Containers
● Distributed Computing
● NoSQL/Time-Series Database
● Stream Processing
● ML Models

Why Move Cloud services to the Edge?
There are four main benefits of moving data centres to the edge,
1. Latency :edge data centres facilitate lower latency, meaning much faster response times. Locating compute and storage functions closer to end users reduces the physical distance that data packets need to traverse, as well as the number of network “hops” involved, which lowers the probability of hitting a transmission path where data flow is impaired

2. Bandwidth :edge data centres process data locally, reducing the volume of traffic flowing to and from central servers. In turn, greater bandwidth across the user’s broader network becomes available, which improves overall network performance

3.Operating Cost: because edge data centres reduce the volume of traffic flowing to and from central servers, they inherently reduce the cost of data transmission and routing, which is important for high-bandwidth applications. More specifically, edge data centres lessen the number of necessary high-cost circuits and interconnection hubs leading back to regional or cloud data centres, by moving compute and storage closer to end users

4. Security edge data centres enhance security by: i) reducing the amount of sensitive data transmitted, ii) limiting the amount of data stored in any individual location, given their decentralized architecture, and iii) decreasing broader network vulnerabilities, because breaches can be ring-fenced to the portion of the network that they compromise.

## Lecture 3: Introduction to Edge Computing

### **Key Topics Covered:**

- Evolution from Cloud to Edge
- Benefits of Edge Computing
- Building blocks of Edge Computing
- Three-tier architecture of Edge Computing

### **Why Edge Computing?**

- **Distributed Computing Model**: Unlike cloud computing, which is centralized, edge computing brings computation closer to data sources.
- **Latency Reduction**: Avoids the round-trip delay to the cloud.
- **Data Sovereignty**: Keeps sensitive data localized.
- **Efficient Bandwidth Utilization**: Reduces network congestion by processing data locally.

### **Building Blocks of Edge Computing**

1. **Data Ingestion**
    - Capturing high-velocity, high-throughput data from various sources.
    - Uses message queues like Kafka.
    
    ![image](https://github.com/user-attachments/assets/ba450752-4b5c-4ab0-b246-cd0de34d2f27)

    
2. **Machine-to-Machine (M2M) Brokers**
    - Facilitates real-time communication between IoT devices.
    - Example: MQTT for real-time sensor communication.
    
    ![image](https://github.com/user-attachments/assets/56e93647-22e2-4b3f-983d-bd6c0e48aa0a)

    
3. **Storage Layers**
    - **Object Storage**: Handles unstructured data (e.g., video feeds).
    - **NoSQL / Time-Series Databases**: Used for structured and time-sensitive data.
4. **Stream Processing**
    - Real-time event processing for applications like fraud detection and anomaly detection.
    
    ![image](https://github.com/user-attachments/assets/23eb69a7-40de-4676-b524-543523dceb2d)

    
5. **Function as a Service (FaaS)**
    - Lightweight, event-driven compute model.
6. **Machine Learning Models**
    - ML models deployed at the edge to enable intelligent decision-making.

### **Three-Tier Edge Computing Architecture**

1. **Data Source Layer**: Sensors and devices generating raw data.
2. **Intelligence Layer**: Edge computing infrastructure that processes data.
3. **Actionable Insights Layer**: Sends alerts, visualizations, or automatic control actions based on processed data.

## Lecture 4: Edge Computing Paradigms

### **Key Topics Covered:**

- Types of Edge Computing (Thick-Edge, Thin-Edge, Micro-Edge)
- Various paradigms: Cloudlet, Micro Data Centers, Fog Computing, Mobile Edge Computing (MEC)
- Latency models in Edge-Cloud systems

Compared with cloud computing only, the main advantages of edge computing combined with cloud computing are three folds:

1. backbone network alleviation, distributed edge computing nodes can handle a large number of computation tasks without exchanging the corresponding data with the cloud, thus alleviating the traffic load of the network;
2. agile service response, services hosted at the edge can significantly reduce the delay of data transmissions and improve the response speed;
3. powerful cloud backup, the cloud can provide powerful processing capabilities and massive storage when the edge cannot afford.

### **Types of Edge Computing**

1. **Thick Edge**
    - Located 1-10 km from the data source.
    - Used for **data aggregation and storage** at cell tower data centers or on-premise setups.
2. **Thin Edge**
    - Located 0.001-1 km from the data source.
    - Includes **local processing units, industrial PCs, and intelligent routers**.
3. **Micro Edge**
    - Located at the **sensor level** (<0.001 km).
    - Processing happens **directly on IoT devices**.

### **Edge Computing Paradigms**

1. **Cloudlet and Micro Data Centers**
    - Small, localized data centers that offload processing from the cloud.
    - Used for **real-time applications like facial recognition and AR/VR**.
    
    ![image](https://github.com/user-attachments/assets/9ce04aca-0ca0-4945-ae00-bb7bf67cd8f3)

    
2. **Fog Computing**
    - A **multi-tier** computing model where IoT devices process some data locally before sending it to the cloud.
    - Works best for **highly distributed IoT networks**.
    
    ![image](https://github.com/user-attachments/assets/b8c71bb1-d017-40bc-9ce0-5eee4f6f4aa5)

    
    ![image](https://github.com/user-attachments/assets/9db8cf87-db73-4e4a-a574-9f808ee8200a)


    
3. **Mobile Edge Computing (MEC)**
    - Deploys computing resources at cellular base stations.
    - Optimized for **low-latency mobile applications**.
4. **Collaborative End-Edge-Cloud Computing**
    - Balances computation between **end devices, edge infrastructure, and cloud servers**.
    - Used for **AI model training in the cloud and inference at the edge**.

### **Edge-Cloud System Architecture**

- Edge computing complements cloud computing.

![image](https://github.com/user-attachments/assets/176e3d90-4a66-4e3e-8238-56f6c3f2e417)


- **Key Challenges in Edge-Cloud Systems**:
    - Task allocation strategies for latency-sensitive applications.
    - Optimizing computational and communication resources.
    - Implementing AI-driven **task offloading** mechanisms.

### **Latency Models in Edge-Cloud Systems**

1. **Local Edge Processing**:
    - Data is processed at the edge without cloud involvement.
    - Offers the lowest latency.
    
    ![image](https://github.com/user-attachments/assets/cad1e448-9652-4094-bbe2-200876d1f67c)

    
    ![image](https://github.com/user-attachments/assets/1334d1a8-6d98-4828-b07f-28edf1b3ee7c)


    
2. **Edge + Cloud Collaboration**:
    - Part of the data is processed locally, while some tasks are sent to the cloud.
    - Balances compute efficiency and latency.
    
    ![image](https://github.com/user-attachments/assets/4781eabe-527b-4c8f-bf1e-2157133622a5)

    
    !![image](https://github.com/user-attachments/assets/e335880e-a7af-4f1d-9484-42e9804fecf3)

    
3. **Multi-Level Edge Processing**:
    - Tasks are dynamically distributed across multiple edge nodes and the cloud.
    - Best suited for **highly distributed IoT applications**.
    
    ![image](https://github.com/user-attachments/assets/5420fd9d-2cb0-46e9-bedf-99fd249c510b)

    
    ![image](https://github.com/user-attachments/assets/bb455323-1257-4c81-95c6-ba330b472dda)

