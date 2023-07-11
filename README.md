# Introduction

Welcome to this comprehensive study guide designed to help you prepare for the Microsoft Azure Fundamentals (AZ-900) exam. This repository is a collection of structured notes covering a wide range of services and concepts within Microsoft Azure, all aligned with the AZ-900 exam objectives.

The notes include key details on various Azure services including, but not limited to, compute services like virtual machines, networking features, storage solutions, serverless computing offerings like Azure Functions and Logic Apps, as well as data management and DevOps tools offered by Azure. Additionally, it dives into important Azure management principles such as Azure Resources and Resource Groups.

Whether you're a beginner in cloud computing aiming to pass your AZ-900 exam, or an experienced professional seeking a refresher on Azure fundamentals, these notes serve as a valuable resource.

Each Azure service or concept is organized in its own section, enabling you to easily locate and focus on the specific areas you need. This format makes it a reliable quick-reference guide during your exam preparation and revision.

Dive in, study smart, and best of luck with your AZ-900 exam preparation! Your feedback is highly appreciated to improve this open-source Azure study guide.

## ☁️  Core Cloud Concepts in Azure

### Agility

Agility means that you can deploy and configure cloud-based resources quickly as app requirements change.

### Azure Resourse Hierarchy
![Management groups, subscriptions, resource groups and resources.](/images/resource-groups.png)
#### Management Groups

Management groups can be used in environments that have multiple subscriptions to streamline the application of governance conditions. This means you can manage access, policies and compliance across multiple subscriptions.
#### Azure Subscriptions

Azure Subscriptions are a logical unit of Azure services that are linked to an Azure account. In order to take advantage of Azure’s cloud-based services, you must have a subscription as it serves as a **single billing unit** for Azure resources used in that account.

- An Azure subscription is linked to a single account, the one that was used to create the subscription and is used for billing purposes. Within the subscription, resources can be provisioned as instances of the many Azure products and services.
- You can have more than one subscription, often for billing purposes, since each subscription generates its own set of billing reports and invoices.
- The person who creates an Azure subscription becomes the **global administrator** for that subscription and has **full access** to every aspect of that subscription hence separate subscriptions can also be a way to create a **division of responsibility** for Azure services.

#### Resource Groups

A Resource Group in Azure is essentially a logical container holding resources deployed within an Azure subscription. It typically encompasses resources intended to be managed as a collective entity.

Every resource within Azure must belong to a resource group, providing a structured way to manage and organize your Azure resources. Ideally, all the resources within a group should share the same lifecycle, meaning they are deployed, updated, and deleted collectively.

Allocation of resources to resource groups can be determined based on your organization's specific needs and logic. It is generally recommended to group resources with the same lifecycle together for efficient management. A resource group can include all resources for a given solution, or only those that you want to manage collectively.

Resource groups facilitate the application of consistent policies and access controls to the group's resources, enhancing security and governance.

#### Resources

Azure Resources are individual instances of services that you create within Azure, such as virtual machines (VMs), storage, or SQL Databases. Each resource is an exemplar of a particular resource type, represented by identifiers like Microsoft.Compute/virtualMachines or Microsoft.Storage/storageAccounts.

Resources offer operations for interacting with their associated data. For instance, a storage account resource would allow you to create or delete the account, list the account's keys, or modify its properties. Every resource carries a unique resource ID that includes details like subscription, resource group, provider namespace, resource type, and resource name for accurate identification.

Resources can also bear metadata, such as tags, which are name-value pairs that you can assign to resources. These tags facilitate the categorization of resources for management tasks like billing or monitoring.

Resources can only be associated with a single subscription. Subscriptions may be grouped into management groups. An account may be associated with multiple subscriptions.

### Defense-in-depth

A defense in depth strategy uses a series of mechanisms to slow the advancement of an attack that aims to gain unauthorized access to data. The principle of least privilege means restricting access to information to only the level that users need to perform their work. A DDoS attack attempts to overwhelm and exhaust an application's resources. The perimeter layer is about protecting an organization's resources from network-based attacks.

### **Elasticity**

Elasticity refers to the ability to dynamically adjust cloud resources to meet fluctuating application demands. By utilizing autoscaling, applications can ensure they always have the necessary resources to function optimally. This on-demand resource provision and de-provision enhances cost-effectiveness by ensuring you only pay for what you use. Moreover, elasticity enables applications to maintain performance during peak loads and conserve resources during periods of lesser demand.

### Expenditure Model

- **Operating Expenditure (OPEX)**: This refers to the costs that a business incurs as a result of performing its normal business operations. In the context of cloud computing, OPEX represents costs related to consumption or use of cloud resources. These costs are typically incurred monthly, based on actual usage.
    - Azure on-demand or pay-as-you-go pricing is an example of an OpEx model
- **Capital Expenditure (CAPEX)**: These are the funds used by a company to acquire or upgrade physical assets. In the traditional IT model, servers, storage, and network infrastructure are all CapEx. When a company shifts to cloud computing, these costs are often greatly reduced or eliminated as these resources are now provided by the cloud service provider, moving these costs into the OPEX model.
    - Azure Reservations is an example of a CapEx model

### Geo-distribution

You can deploy apps and data to regional data centers around the globe, thereby ensuring that your customers always have the best performance in their region. This is referred to as geo-distribution.

### **High Availability (Reliability)**

High availability, also referred to as reliability in Azure, ensures continuous application availability and a seamless user experience, even when issues arise. It involves designing systems with redundant components and failover capabilities so that if one component fails, another can seamlessly take its place. In the Azure context, this might involve the use of multiple Azure regions, availability zones, and paired regions to ensure resilience against outages and disasters.

### Horizontal Scaling vs Vertical Scaling

**Horizontal Scaling (Scale Out/In)**

Horizontal scaling is the process of adding or removing instances from a system to increase or decrease capacity. In the context of cloud computing, this typically refers to adding or removing servers (virtual machines) from a system.

Key points:

- Horizontal scaling can provide increased capacity during high traffic periods, and then scale in when demand is lower to save on costs.
- Scaling out can help to improve redundancy and reliability by ensuring that a failure in a single instance does not impact the entire system.
- This strategy requires a load balancer to distribute traffic across multiple instances.

**Vertical Scaling (Scale Up/Down)**

Vertical scaling, on the other hand, involves increasing or decreasing the capacity of an existing server, such as upgrading the CPU, RAM, or disk capacity of a server. This is done without changing the number of servers.

Key points:

- Vertical scaling can be a more straightforward approach to handling increased demand, as it doesn't require complex architecture or distribution of workload.
- It can improve performance of a single instance, but it may have limitations due to the maximum capacity of a single server.
- Vertical scaling often requires downtime while the resources are being increased or decreased.
- It can provide an immediate solution for performance issues but lacks the redundancy benefits of horizontal scaling.

Both strategies can be used in conjunction for an effective scaling strategy, depending on the needs of the system and its workload. Cloud services like Azure make both horizontal and vertical scaling strategies easy to implement, giving you flexibility to optimize your resources based on your application's demand.

### Public Cloud

Azure operates as a public cloud computing platform, offering an array of online services including resources like virtual machines, data storage, networking capabilities, and more. This infrastructure operates on a multi-tenant model where various organizations, often referred to as 'tenants', share the same hardware, storage, and network devices. These services can be accessed and managed using a web browser.

Key aspects to consider:

- The public cloud model endows users with unprecedented scalability and resource sharing that is virtually impossible to achieve in a traditional data center or private cloud setup.
- Public cloud delivers services to numerous clients using the same shared infrastructure, maximizing efficiency and cost-effectiveness.
- The major strengths of the public cloud model revolve around its agility, scalability, and elasticity, providing an adaptable framework to cater to varying demand.


### Service Level Agreement (**SLA)**

A Service Level Agreement (SLA) is a commitment between a service provider and a client that defines the level of service expected. In Azure, SLAs outline the performance and availability standards that Azure promises to uphold. They provide guarantees on aspects such as uptime and connectivity, often expressed as a percentage (like 99.99% availability).

When combining multiple Azure services to deliver a solution, it's essential to consider the Compound SLA. This reflects the overall availability based on the combined SLAs of the individual services. Because each service has its own SLA, the resulting Compound SLA might be lower than the individual ones. Therefore, it's crucial to consider the impact of each service's SLA when designing multi-service solutions in Azure.

$$
SLA_{1} * SLA_{2} = Composite SLA
$$

### Service Model

- ******************************************************Infrastructure as a Service******************************************************
- ******************************************Platform as a service******************************************
- ******************************************Software as a Service******************************************

![Service model](/images/service-model.png)

### Single Sign-On (SSO)

SSO enables a user to sign in one time and use that credential to access multiple resources and applications from different providers. Azure AD is provides SSO.

### Virtual Network Peering

Virtual network peering is a feature in Azure that allows you to connect two Azure virtual networks in the same region or different regions using the Azure backbone network. It enables seamless connectivity and communication between the peered virtual networks as if they were part of a single network.

---

## 🛎️ ****Azure Services****

### **Azure App Service**

Azure App Service is a Platform-as-a-Service (PaaS) offering from Microsoft Azure, providing a managed environment for developers to host web applications, mobile app backends, RESTful APIs, and more. With this service, infrastructure management is abstracted, enabling developers to focus solely on the application's business logic. Some of its key features include auto-scaling, high availability, support for both Windows and Linux, and continuous deployment from Git repositories.

### Azure Bastion

Azure Bastion is a fully managed Platform as a Service (PaaS) offering in Microsoft Azure that provides secure and seamless remote access to virtual machines (VMs) within virtual networks. It eliminates the need for public IP addresses, network security groups, or VPN connections to access Azure VMs, offering a more secure and streamlined approach to remote management.

### **Azure Content Delivery Network**

Azure Content Delivery Network (CDN) is a robust, developer-centric network of distributed servers designed to deliver high-bandwidth content to users rapidly and efficiently. By caching content at strategically positioned physical nodes across the globe, Azure CDN ensures fast and reliable content delivery.

- **Edge Servers**
    - Azure CDN uses Edge Servers, also known as Points-of-Presence (PoPs), to cache content closer to the users, reducing load times significantly.
- **Content Variety**
    - Azure CDN supports the delivery of various types of web content, encompassing HTML pages, CSS files, JavaScript files, images, and videos.

### Azure Container Instances

Azure Container Instances (ACI) is a serverless container platform provided by Microsoft Azure. It allows you to easily run containerized applications without managing the underlying infrastructure or virtual machines. ACI offers a lightweight and flexible solution for deploying and scaling containers in the Azure cloud.

### Azure DevOps

Azure DevOps is a comprehensive suite of services designed to support the complete lifecycle of application development. These services are intended to facilitate planning, collaboration, building, and deployment of applications, providing a unified platform for DevOps processes.

Key Components:

- **Azure Boards**: A powerful planning and tracking tool, Azure Boards enables you to manage, track, and prioritize work across the entire development effort. It's an excellent tool for handling backlogs, tracking bugs, and providing a visual overview of work progress through Kanban boards.
- **Azure Repos**: This service provides a secure and reliable platform for hosting Git repositories, offering version control capabilities and collaborative code development. Azure Repos is designed to handle everything from small projects to large scale enterprise software development.
- **Azure Pipelines**: As a key component for continuous integration (CI) and continuous deployment (CD), Azure Pipelines allows you to automate the build, testing, and deployment of your applications to any platform.
- **Azure Test Plans**: A tool for managing and running tests, Azure Test Plans provides a complete toolkit for tracking, planning, and managing tests as part of the development process. It supports both manual and exploratory testing and provides comprehensive test reporting.
- **Azure Artifacts**: This service allows you to create, host, and share packages with your team. Azure Artifacts integrates with your CI/CD pipeline, providing a secure and reliable way to share and consume software packages.

Together, these services enable teams to effectively plan work, collaborate on code development, and build and deploy applications seamlessly. This integrated approach ensures consistency, improves productivity, and enhances the overall quality of your software projects.

### Azure DevTest Labs

Azure DevTest Labs is a comprehensive service designed to simplify the provisioning and management of environments for testing and development. It provides an efficient, scalable, and cost-effective solution for creating virtual machines (VMs) and managing resources.

Key Features:

- **Load Testing**: Azure DevTest Labs supports load testing, ensuring your applications can perform well under expected user load. This aids in identifying potential performance bottlenecks before deployment, hence increasing the reliability and performance of your applications.
- **Azure Resource Manager Template Integration**: Azure DevTest Labs can leverage Azure Resource Manager templates to configure virtual machines, providing a highly repeatable and consistent process for VM setup. This feature reduces the manual effort and potential for error during VM configuration.
- **Rapid VM Provisioning and De-provisioning**: One of the major advantages of Azure DevTest Labs is its capability to quickly spin up and destroy environments as needed. This service can swiftly set up and tear down up to 100 VMs, making it an excellent choice for large-scale testing and development.

This scalability is incredibly beneficial for maintaining cost-efficiency, as environments can be created on-demand when needed, and decommissioned after use, thereby eliminating unnecessary costs associated with idle resources.

In summary, Azure DevTest Labs is a robust service that offers significant value for developers and testers, facilitating a seamless, efficient, and flexible testing and development process.

### **Azure Event Grid**

Azure Event Grid is a service that helps you build event-driven applications. It enables real-time event handling within your applications and provides a mechanism for responding to events from many different sources.

- **Event-Based Architecture**
    - Azure Event Grid is designed to support event-based architecture in your applications.
- **Integrated Support**
    - It has built-in support for events from Azure services and also supports custom topics for your own events.
- **Event Filtering**
    - Azure Event Grid allows you to filter specific events to route them to different endpoints, multicast to multiple endpoints, and ensures reliable event delivery.
- **Fault-Tolerant**
    - Azure Event Grid is designed for high availability, deployed across multiple fault domains in every region and Availability Zones (AZs).
- **Subscription**
    - To use Azure Event Grid, you subscribe to an Azure resource, providing an event handler or a WebHook endpoint to which the service sends events.

### **Azure Functions**

Azure Functions is a serverless, event-driven compute service that enables you to run code on-demand without having to explicitly provision or manage infrastructure. It allows for the creation of small, single-purpose functions that can respond to cloud events. This platform is highly scalable and only charges for the time your code is running, making it an economical choice for many cloud computing tasks.

Key Features:

- **Serverless & Event-Driven**: Eliminates the need for managing servers and enables automatic triggering of functions based on specific events.
- **On-Demand Compute**: Allows functions to run whenever they're needed, providing flexible and cost-effective compute solutions.
- **Scalability**: Auto-scales based on demand, capable of handling a large number of requests per second.

### **Azure Kubernetes Service**

Azure Kubernetes Service (AKS) is a managed container orchestration service provided by Azure, and is based on the open-source Kubernetes system. AKS simplifies the deployment and management of containerized applications, offering scalability and high availability out of the box. Other key features include serverless Kubernetes, integrated continuous integration/continuous deployment (CI/CD), and enterprise-grade security and governance, making it a suitable choice for production workloads.

### ****Azure IoT Hub****

Azure IoT Hub serves as the central messaging hub for bidirectional communication between IoT devices and Azure cloud services. This cloud-based service facilitates the secure connection, monitoring, and management of IoT assets at scale. IoT Hub supports various device connectivity and data exchange protocols, offering both device-to-cloud and cloud-to-device messaging capabilities. It integrates with other Azure services such as Azure Stream Analytics and Azure Functions, allowing real-time processing of IoT data and triggering actions based on IoT events. By offering advanced features like device management, data ingestion, and analytics, Azure IoT Hub simplifies the implementation and operation of comprehensive IoT solutions.

### **Azure Logic Apps**

Azure Logic Apps provide a robust, serverless solution to schedule, automate, and orchestrate tasks, business processes, and workflows across your enterprise or organization. They facilitate seamless integration of applications, data, systems, and services by providing an intuitive visual designer that allows you to define the order of steps and conditions. A compelling feature of Azure Logic Apps is the ability to send emails automatically upon occurrence of a specific event, allowing you to set up customizable notifications or actions based on your business needs.

Key Features:

- **Serverless Architecture**: Reduces the need for explicit resource management, allowing you to focus on designing and implementing business logic.
- **Workflow Automation**: Simplifies the process of coordinating tasks, workflows, and complex business processes across diverse systems and services.
- **Event-Driven Actions**: Enables automatic email dispatching based on specified triggers or events.

### **Azure Resource Manager**

Azure Resource Manager (ARM) is the deployment and management service provided by Microsoft Azure. It enables users to create, deploy, manage, and monitor all the resources within their Azure environment as a single, cohesive unit. ARM provides a consistent management layer that allows for the automation and orchestration of resource provisioning and configuration.

### Azure Service Bus

Azure Service Bus is a robust and secure cloud-based message broker service that enables the asynchronous transfer of data and state. The service is designed to facilitate communication between sender and receiver applications through a reliable publish/subscribe model.

Key Features:

- **Message Broker Functionality**: Acting as a queue, Azure Service Bus ensures that every message sent is successfully received by the intended recipient, thereby minimizing the risk of message loss.
- **Reliability and Security**: With the Azure Service Bus, you can rest assured that your data will be transmitted securely and reliably. Its resilient architecture is designed to resist system failures and maintain your data's integrity.
- **Asynchronous Communication**: By utilizing a publish/subscribe model, Azure Service Bus allows for decoupled and asynchronous communication between sender and receiver applications. This allows applications to send or receive messages at their own pace without having to wait for other processes to finish.
- **Topics and Subscriptions**: Azure Service Bus' topic and subscription feature offers a powerful way to route messages across multiple subscriber applications. Topics can be used to categorize messages, and subscriptions can be used to define what types of messages an application is interested in receiving.

### **Azure Stream Analytics**

Azure Stream Analytics is a real-time analytics and complex event-processing engine designed to analyze and process high volumes of fast-streaming data from multiple sources simultaneously. This powerful service can extract and identify patterns and relationships from a variety of input sources such as IoT devices, sensors, weblogs, clickstreams, and more.

The use cases for Azure Stream Analytics are wide-ranging:

- **Real-time IoT device analytics:** This service can analyze incoming data from IoT devices in real-time, making it invaluable for scenarios that require immediate response, such as anomaly detection in sensor data.
- **Weblogs/clickstream analytics:** Azure Stream Analytics can process user interaction data in weblogs or clickstreams in real-time, providing actionable insights into user behavior and website performance.
- **Geospatial analytics:** The service can process and analyze data with geographic attributes, enabling real-time tracking and geo-fencing for transportation, supply chain, and fleet management applications.
- **Remote monitoring:** Azure Stream Analytics can be used to monitor remote systems and devices, alerting to unusual behaviors or conditions that may need attention.
- **Inventory control data:** By analyzing real-time inventory data, Azure Stream Analytics can help businesses manage their inventory more effectively, flagging low stock levels or predicting future inventory needs based on trends.

These use cases make Azure Stream Analytics a versatile tool for organizations that require real-time insights for their decision-making processes.

### Azure Virtual Machine Scale Sets

Azure Virtual Machine Scale Sets (VMSS) is a feature in Microsoft Azure that allows you to deploy and manage a group of identical virtual machines (VMs) as a single entity. VMSS provides scalability, high availability, and easy management for applications that need to scale out and handle varying workloads.

### Azure Virtual Desktop

Azure Virtual Desktop is a desktop and application virtualization service that runs in the cloud. It enables your users to use a cloud-hosted version of Windows from any location. Azure Virtual Desktop works across devices such as Windows, Mac, iOS, Android, and Linux. It works with apps that you can use to access Remote Desktops and apps. You can also use most modern browsers to access Azure Virtual Desktop-hosted experiences.

---

## 🕸️ ****Azure Networking****

### **Azure Application Gateway**

Azure Application Gateway is a specialized load-balancing service that provides application-level routing. It enhances the scalability and security of your web applications by directing traffic based on multiple parameters, such as URL paths, host headers, and cookie values. Additional features include SSL/TLS offloading, session affinity, and web application firewall (WAF) capabilities for robust protection against common web-based threats.

### **Azure ExpressRoute**

Azure ExpressRoute offers a private, dedicated connection from your on-premises data centers to Azure, facilitated by a connectivity provider. It delivers greater reliability and predictability than conventional internet-based connections, offering higher security and lower latency. Each ExpressRoute circuit entails two connections to two Microsoft Enterprise edge routers (MSEEs) at an ExpressRoute Location from the connectivity provider or your network edge. It is worth noting that a redundant Layer 3 connectivity configuration is required for the service level agreement (SLA) to be valid.

![ExpressRoute](/images/express-route.png)

### **Azure Firewall**

Azure Firewall is a fully managed, cloud-based network security service protecting your Azure Virtual Network resources. It provides network-level protection for inbound and outbound traffic across multiple subscriptions and virtual networks. Azure Firewall is highly available and features built-in auto-scaling, and it integrates with Azure Monitor for advanced logging and analytics. As a stateful firewall-as-a-service, Azure Firewall possesses a static public IP address for VNet resources, allowing external firewalls to identify traffic originating from your virtual network. Used in conjunction with Network Security Groups, it provides defense-in-depth security.

![Azure Firewall](/images/firewall.png)

### **Azure Traffic Manager**

Azure Traffic Manager is a DNS-based traffic load balancer that allows for the distribution of traffic across numerous endpoints, such as web apps, VMs, and cloud services. It enhances application performance and availability through high availability, performance optimization, and automatic failover capabilities. Traffic can be routed to different endpoints based on geographic location, routing preference, or endpoint health.

![Azure Traffic Manager](/images/azure-traffic-manager.png)

### **Azure Virtual Network (VNet)**

Azure Virtual Network (VNet) is the cornerstone of your private network in Azure, providing a secure environment for resources like VMs to communicate with each other, the internet, and on-premises networks. VNets allow you to define your own private IP address space and segment the network into subnets, establishing a trusted boundary to host your compute resources.

### **Application Security Groups**

Application Security Groups streamline the management of network security group rules by grouping virtual machines and defining rules based on these groups. This eliminates the need for manual maintenance of explicit IPs and is only applied to the network interfaces that are members of the application security group.

### **Network Security Groups**

Network Security Groups (NSGs) serve to filter traffic to and from network interfaces in Azure. They encompass multiple inbound and outbound security rules that enable you to permit or deny traffic based on protocol, source IP address, or range, destination IP address or range, and port ranges. NSGs can be associated with subnets and individual network interfaces to control traffic within virtual networks (VNets) or between VNets and the internet. Rules are evaluated by priority using the 5-tuple information (source, source port, destination, destination port, protocol)

### **Point-to-Site VPN connection (P2S)**

A Point-to-Site (P2S) VPN connection allows a secure link from an individual client computer to a virtual network, facilitating remote work, for instance, from home.

### **Public Load Balancer**

A Public Load Balancer manages traffic from the internet to VMs, mapping public IPs to the private IPs and ports of VMs. For internal traffic within the Azure network, the Internal/Private Load Balancer is used.

### **Site-to-Site VPN (S2S)**

A Site-to-Site (S2S) VPN creates a secure, encrypted tunnel over the public internet to connect an on-premises network to an Azure network. This setup requires an on-premises VPN device with an externally facing public IP. Each virtual network can have one VPN gateway, but multiple connections to the same gateway are possible, sharing the gateway's bandwidth.

---

## 📦 ****Azure Storage and Databases****

### **Azure Blob Storage**

Azure Blob Storage is an essential service offering in Azure that's used for scalable, object storage of unstructured data. It can accommodate various types of data such as text, binary data, documents, media files, and application installers.

- **Access Tiers**
    
    These tiers provide cost-effective storage methods that are optimized for specific usage patterns. They allow for resource allocation depending on data frequency of access, storage duration, and latency requirements.
    
    - **Cool**
        - Designed for data that is infrequently accessed and has a minimum storage duration of at least 30 days.
        - Operates at the account level, so the configuration affects all blobs in the storage account.
    - **Hot**
        - Intended for data that is accessed frequently.
        - Also operates at the account level, meaning that the settings applied to this tier will affect all blobs under the storage account.
    - **Archive**
        - Suitable for data that is rarely accessed and needs to be stored for at least 180 days or more.
        - Acceptable to have high retrieval latency.
        - Operates at the blob level, allowing specific blobs to be archived, irrespective of the account level settings.
    - **Premium Performance**
        - Provides high-performance storage with single-digit millisecond latency.
        - Best suited for scenarios that require high transaction rates or fast access times. For example, interactive video editing, static web content, and online transactions.

### **Azure Cosmos DB**

Azure Cosmos DB is Microsoft's globally distributed, multi-model database service. It offers single-digit millisecond read and write latencies, 99.999% availability, and automatic and instant scalability. It supports various popular data models and APIs, including SQL API, MongoDB, Cassandra, Gremlin, and Table API.

- **NoSQL Database**
    - Offers flexible, schema-less data model designed for modern web, mobile, AI, and IoT applications.
- **Global Distribution and Scalability**
    - Cosmos DB can scale elastically and independently across any number of Azure regions worldwide. This means you can add or remove regions from your Cosmos DB account at any time, scaling the throughput or storage of your database independently in each region.
- **Comprehensive Service Level Agreements (SLAs)**
    - Cosmos DB provides industry-leading, comprehensive SLAs encompassing throughput, latency, availability, and consistency guarantees. These commitments to performance and reliability make it a compelling choice for mission-critical applications.
- **Data Replication**
    - With Cosmos DB, data can be automatically and transparently replicated across multiple Azure regions. This ensures that users can interact with a copy of the data that is closest to them, thereby reducing latency and improving app responsiveness.

Cosmos DB is an excellent choice when building applications with a globally distributed user base, requiring low latency, high availability, and elastic scalability.

### **Azure Database Migration Service**

Azure DMS is a fully managed service designed to enable seamless migrations from multiple database sources to Azure data platforms with minimal downtime.

- **Support for Various Migration Scenarios**
    - The service supports a variety of source and target pairs, accommodating different migration needs.
- **Offline and Online Migration**
    - DMS provides the flexibility of performing a one-time migration (offline) or setting up continuous synchronization of your databases (online).
- **Data Migration Assistant**
    - DMS integrates with the Data Migration Assistant tool, which generates assessment reports to provide recommendations for the migration process, thereby ensuring a smoother transition.
- **End-to-End Migration Execution**
    - Once the migration plan is prepared and finalized, DMS performs all the necessary steps to execute the migration, reducing the manual efforts involved.

### **Azure Files**

Azure Files is a fully managed service providing cloud-based file shares that can be accessed using the industry standard Server Message Block (SMB) protocol.

- **Network File Shares**
    - Azure Files allows for the setup of highly available network file shares. This facilitates multiple virtual machines to share the same files with both read and write access.
- **Seamless Integration with On-Premise Servers**
    - The service can create a file share that is directly mounted or mapped on-premise Windows servers, providing a seamless solution for document sharing across different environments.
- **Secure Access with Shared Access Signature (SAS)**
    - Azure Files uses a Shared Access Signature (SAS) token to grant specific, time-bound access to private assets, ensuring security and controlled access to the file shares.
- **Use Cases**
    - Azure Files is versatile, fitting several use cases such as migrating on-premises file shares to Azure, storing resource logs, metrics, crash dumps, and sharing configuration files across deployments.
- **High Availability and Durability**
    - Built for robustness, Azure Files offers high availability and durability, making it a reliable choice for storing important file data.

---

## ⚙️ ****Azure Management and Governance****

### **Azure Advisor**

Azure Advisor acts as your personalized cloud consultant, providing recommendations for optimizing Azure resources based on high availability, security, performance, and cost. It uses your resource configuration and usage data to offer actionable insights and best practices for efficiently running your workloads in Azure.

### **Azure Blueprint**

Azure Blueprint is a declarative way to orchestrate the deployment of various resource templates and other artifacts such as:

- **Policy Assignments**
    - Enforce rules for resource types or assign specific values during deployment.
- **Role Assignments**
    - Designate access to resources based on specific job functions.
- **Resource Groups**
    - Container for resources deployed within an Azure subscription.
- **ARM templates**
    - Declarative syntax for deploying resources.

### **Azure Cloud Shell**

Azure Cloud Shell is an interactive, authenticated, browser-accessible shell for managing Azure resources. It provides the flexibility to choose between Bash or PowerShell environments and works independently of the local operating system. 

### **Azure Cost Management + Billing**

Azure Cost Management + Billing is a suite of tools designed to provide a comprehensive view of your cloud costs. It facilitates cost analysis, bill payment, cost access management, spending threshold settings, and identification of cost optimization opportunities. It can also help you create and manage budgets.

### **Azure Reservations**

Azure Reservations provide an advantageous pricing model that allows you to commit to one-year or three-year terms for Azure resources, thereby securing a significant discount over the standard pay-as-you-go pricing. By leveraging Azure Reservations, you can achieve savings of up to 72% compared to the standard pricing model.

- **Discounted Pricing**
    - Azure Reservations offer an opportunity for cost-saving by providing discounted prices on select Azure products and resources.
- **Flexibility**
    - Reserved VM Instances under Azure Reservations are highly flexible, allowing for easy exchanges or returns when your business needs change.

### **Azure Resource Manager Locks**

Azure Resource Manager Locks offer an added layer of protection to your Azure resources. These can be applied at different levels - subscriptions, resource groups, or individual resources - to prevent accidental modifications or deletion.

- **CanNotDelete**
    - Users can read and modify the resource but cannot delete it.
- **ReadOnly**
    - Users can only read the resource; modifications are disallowed.

### **Azure Resource Manager Templates**

Azure Resource Manager (ARM) Templates act as the management layer for resource groups and their contained resources. They are pivotal for automating the deployment and configuration of resources.

- **Infrastructure as Code (IaC)**
    - Utilizing tools like PowerShell, Azure CLI, Azure portal, REST API, and client SDKs, ARM Templates allow you to describe and manage your infrastructure using code.
- **JSON Format**
    - ARM Templates are written in JSON, ensuring a human-readable and editable structure for your configurations.

### Azure Resource Manager Template vs Blueprint

Both Azure Blueprint and Azure Resource Manager (ARM) Templates are effective in automating the deployment and configuration of resources. However, Azure Blueprint provides a comprehensive governance model with policy and role definitions while ARM Templates are best suited for bundling and deploying resources as a group.

### **Azure Support Options**

Azure provides various support options to cater to different customer needs:

- **Basic Plan**
    - Free for all Azure customers. Includes 24/7 access to self-help resources, best practice guides, and Azure health status notifications. However, it lacks technical support for critical issues.
- **Standard Plan**
    - Suitable for production environments. Offers 24/7 technical support.
- **Developer Plan**
    - Designed for trial and non-production environments. Offers a response time of 8 hours.
- **Professional Direct Plan**
    - Ideal for mid-sized to large companies with business-critical dependency on Azure. Offers 24/7 support with less than a 1-hour response time for critical issues.
- **Premier Plan**
    - Tailored for large or global enterprises. Offers a response time of 15 minutes.

### **Microsoft Compliance Manager**

Microsoft Compliance Manager is a risk assessment tool available on the Microsoft Service Trust Portal. It helps manage regulatory compliance activities for Microsoft cloud services. It provides a centralized dashboard to manage and track compliance assessments across Azure services and regulatory requirements like ISO 27001, NIST 800-53, and GDPR.

### **Modern Lifecycle Policy**

Microsoft's Modern Lifecycle Policy covers products and services that are serviced and supported continuously. Under this policy, Microsoft commits to providing a minimum of 12 months' notice prior to ending support if no successor product or service is available.

Key Elements:

- **Continuous Servicing and Support**: The Modern Lifecycle Policy guarantees ongoing updates and support for the product or service, which can include bug fixes, security patches, and feature updates. This ensures that the product remains secure and efficient in the ever-changing technological landscape.
- **Customer Requirements**: This policy is contingent upon customers staying current with updates, with specific requirements varying by product and service. This is essential to ensuring that users can take full advantage of the continuous servicing model and the latest product improvements.
- **Advance Notification**: Microsoft provides a minimum of 12 months' notice if a product governed by the Modern Lifecycle Policy is to be discontinued without a successor. This gives customers ample time to plan transitions and ensure there's no disruption to their operations.

The Modern Lifecycle Policy reflects Microsoft's commitment to its customer base, as it guarantees regular updates, provides transparency about product lifecycles, and ensures customers are not left unsupported or uninformed about any changes. This approach aligns well with today's fast-paced technology ecosystem where software products and services need to evolve continually to remain relevant and secure.

### **Microsoft Privacy Statement**

The Microsoft Privacy Statement is a document that provides information on how Microsoft collects, uses, and protects your personal data. It details the types of data Microsoft collects, how this data is used, stored, and protected, and the controls you have over its use. This transparency aims to build trust with users by adhering to data privacy laws and ensuring users' personal data is handled responsibly.

### **Microsoft Trust Central**

Microsoft Trust Central is a comprehensive platform providing customers with an authentic and thorough understanding of Microsoft's security, privacy, and compliance practices. It serves as a single source of truth, offering comprehensive information about how Microsoft implements and manages security, privacy, and compliance controls across its range of products and services.

- **Regional Compliance**
    - Trust Central can assist organizations in adhering to regional compliance requirements by providing relevant and detailed information.

### **Severity Classes**

- **Severity A:** Critical business impact. Business has significant loss or degradation of services and requires immediate attention
- **********************Severity B:********************** Moderate business impact. Moderate loss or degradation of services, but work can reasonably continue in an impaired matter
- **********Severity C:********** Minimum business impact. Customer’s business is functioning with minor impediments of services.

---

## 🔐 ****Azure Identity and Security****

### **Authentication (AuthN) vs Authorization (AuthZ) in Azure**

Authentication and authorization are key security processes in Azure. 

- **Authentication (AuthN)** involves confirming the identity of a user, device, or system. It typically involves validating credentials like usernames and passwords.
- **Authorization (AuthZ)** occurs after successful authentication, determining the permissions or privileges of the authenticated entity, i.e., determining what actions the authenticated user or device is allowed to perform.
    
    ![AuthN vs AuthZ](/images/authn-vs-authz.png)
    

### **Azure Active Directory (Azure AD)**

Azure AD is a robust, cloud-based identity and access management service. It simplifies user access to various cloud and on-premises applications via single sign-on and multi-factor authentication.

- **Centralized Access Management**
    - Azure AD enables organizations to centrally manage and secure resource access.
- **Enhanced Security Features**
    - Offers identity protection, access management, and self-service password reset capabilities.
- **Authentication Flow**
    - Provides security tokens for the authentication flow of cloud-based applications.
- **Resource Access**
    - Users can sign in and access external resources such as Microsoft Office 365, the Azure portal, internal resources like corporate network and intranet, as well as your organization's cloud apps.
- **Microsoft Online Business Services**
    - Services like Office 365 or Microsoft Azure require Azure AD for sign-in and identity protection. Azure AD is automatically integrated when subscribing to any Microsoft Online business service.

![Azure AD](/images/azure-ad.png)

### **Azure AD Connect**

Azure AD Connect is a tool that synchronizes your on-premises directories, like Active Directory, to Azure AD, creating a common identity for on-premises and cloud resources.

- **Directory Synchronization**
    - Synchronizes on-premises directories to Azure AD, enabling single sign-on and self-service for both cloud and on-premises applications.
- **Password Synchronization**
    - Synchronizes passwords from your on-premises environment to Azure AD for easier user access to cloud resources with existing credentials. Azure AD Connect also enables password writeback, facilitating password resets in the cloud with the new password being updated in your on-premises environment.

### **Azure AD Connect Health**

Azure AD Connect Health provides monitoring capabilities and insights for your on-premises Active Directory Domain Services (AD DS) and Azure Active Directory (Azure AD) environments.

- **Monitoring and Insights**
    - Gain insight into the health and performance of your AD DS and Azure AD environments. It provides synchronization data and alerts about potential problems before they escalate.
- **Issue Diagnostics**
    - Offers tools for diagnosing and resolving issues.

### **Azure Information Protection (AIP)**

Azure Information Protection (AIP) is a solution that helps organizations classify and protect documents and emails using labels.

- **Integration and Protection**
    - Integrates with Microsoft Office and other applications for document and email classification and protection, either at the time of creation or automatically based on policies.
- **Protection Options**
    - Provides multiple protection options, including encryption, watermarks, and rights management, and uses Azure Active Directory for fine-grained access control.
- **Label Application**
    - Labels can be applied automatically, manually by users, or via a combination of both methods.

### **Azure Security Center**

Azure Security Center is a unified infrastructure security management system that enhances your data centers' security posture.

- **Threat Protection**
    - Provides advanced threat protection across your hybrid workloads in the cloud and on-premises.
- **Continuous Assessment**
    - Gives a centralized view of the security state of all your Azure resources, performs continuous assessments, and offers recommendations to improve your security posture.

### **Azure Key Vault**

Azure Key Vault is a cloud service that ensures the secure storage and centralized management of keys, secrets, and certificates.

- **Cryptographic Key Management**
    - Cryptographic keys used for authentication and encryption in applications and services can be securely stored and managed.
- **Certificates**
    - Certificates can be created, managed, and automatically renewed. The Key Vault can be used to create/store TLS/SSL certificates.
- **X.509 Standard**
    - X.509, a standard for public key certificates used for secure data exchange over the internet or other networks, can be managed using Azure Key Vault.

### **Azure Sentinel**

Azure Sentinel is a cloud-native security information and event manager (SIEM) platform that leverages built-in AI to analyze large data volumes across an enterprise.

- **Threat Detection**
    - Detects threats early, reduces false positives, and streamlines investigations.
- **Security Analytics**
    - Provides intelligent security analytics at cloud scale with built-in AI to identify and prioritize incidents and threats.

Security Orchestration Automated Response (SOAR)

### **Azure Service Health**

Azure Service Health offers personalized alerts and guidance when Azure service issues impact your resources.

- **Customizable Dashboard**
    - Shows the health of your resources and services along with relevant alerts and events.
- **Alerts**
    - Allows you to set up alerts to notify you of an issue occurrence and also provides a history of past incidents for better understanding.

### **Azure DDoS Protection Standard**

Azure DDoS Protection Standard is a managed service that offers network-level protection for your Azure resources against DDoS attacks.

- **Monitoring and Mitigation**
    - Provides always-on monitoring and automatic mitigation of DDoS attacks, and integrates with Azure Monitor and Azure Security Center for logging and alerting.
- **Scalability**
    - Azure DDoS Protection Standard is scalable and adaptive, automatically tuning and recommending policies based on changing attack patterns.
- Automatically generate post-attack mitigation reports for compliance
- Two tiers: Basic and Standard

### **Azure Active Directory Identity Protection**

Azure Active Directory Identity Protection enables organizations to automate the detection and remediation of identity-based risks, investigate risks using data in the portal, and export risk detection data to third-party utilities for further analyses.

- **User Prompt**
    - Can prompt users to change their passwords if they're signing in from a new IP.

---

## 🔍 ****Azure Monitoring and Reporting****

### Azure Activity Log

Azure Activity Log is a service in Microsoft Azure that provides visibility into the operations performed on resources within an Azure subscription. It captures a comprehensive set of log data, including details about resource provisioning, configuration changes, management operations, and system events.

### **Azure Application Insights**

Azure Application Insights is a service that helps you monitor the performance and usage of your applications. It collects telemetry data and provides tools for analyzing and understanding this data.

- **Application Monitoring**
    - Azure Application Insights helps monitor the performance and usage of your applications, allowing you to detect and diagnose issues and understand user behavior.
- **Cross-Platform Compatibility**
    - It supports several languages, including JavaScript, .NET, Node.js, Java, and Python, and can be used with applications deployed on-premises, in hybrid environments, or in any public cloud.
- **DevOps Integration**
    - It integrates with the DevOps process, allowing for better coordination between development and operations teams.
- **SDK or Agent**
    - To use Azure Application Insights, install the SDK in your application or enable Application Insights using the Application Insights Agent. Telemetry data is then directed to an Azure Application Insights resource through an Instrumentation Key.

### **Azure Monitor**

Azure Monitor is a service that provides real-time visibility into the performance and health of your applications and infrastructure. It uses a range of data collection, analytics, and insights presenting tools to give you a comprehensive understanding of your computing environments.

- **Data Collection**
    - Azure Monitor collects data from a wide range of sources, including Azure services, on-premises systems, third-party applications, and custom data sources.
- **Unified Dashboard**
    - The service provides a unified dashboard that presents collected data in an actionable, easily understood format.
- **Monitoring and Analysis**
    - You can use Azure Monitor to track and analyze metrics, logs, and traces from your applications and infrastructure.
- **Alerts and Notifications**
    - It allows setting up alerts and notifications based on specific conditions or thresholds to proactively address issues.
        
        

### **Azure Synapse**

Azure Synapse (formerly known as Azure SQL Data Warehouse) is an integrated analytics service that accelerates the process of deriving insights from your data. It brings together enterprise data warehousing and big data analytics technology into a single unified and limitless service.

- **Four Key Components**
    - Synapse SQL
        - Provides you with two options for on-demand or provisioned resources, i.e., SQL pool (pay per Data Warehousing Units provisioned) and SQL on-demand (pay per terabyte processed).
    - Spark
        - Offers a deeply integrated Apache Spark environment for big data analytics.
    - Synapse Pipelines
        - Provides a seamless data integration experience in a hybrid environment.
    - Studio
        - Gives a unified user experience for managing, preparing, and monitoring your data.
- **Unlimited Analytics Service**
    - Azure Synapse brings together the best of SQL Data Warehouse and big data analytics technology, providing a limitless analytics service.
- **Node-based Architecture**
    - It uses a node-based architecture where T-SQL commands are sent to a Control node that is a single point of entry. The Massively Parallel Processing (MPP) engine optimizes queries and passes operations to Compute nodes to perform tasks in parallel.
    - Compute nodes store all user data in Azure Storage, while the internal Data Movement Service (DMS) moves data across the nodes as necessary.
    - The separation of computing from storage allows for independent scaling, and you can pause compute capacity while leaving data intact to reduce costs. You only pay for storage during this paused state.
- **Integration**
    - Azure Synapse integrates seamlessly with various other services like Power BI for visualizing data, Azure Data Factory for orchestrating and automating data movement, Azure Machine Learning for building predictive models, Azure Stream Analytics for real-time analytics, and more.
- **Security and Compliance**
    - Azure Synapse provides advanced security and compliance measures, ensuring your data is securely stored and processed.
- **Flexibility**
    - With Azure Synapse, you can query data on your terms at scale, choosing between on-demand or provisioned resources, thus offering flexibility and optimizing costs.
