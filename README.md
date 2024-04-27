# Learning-AZ900

Explore Microsoft Azure Core Services

Azure regions:
Example: Japan West

Gives customers the flexibility and scale needed to bring the applications closer to the end user

Azure has most number of regions
![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/fbad41ed-3e21-4b0b-87a6-6b16d954bbf7)


	• At least 300 miles distance between data centers in region pairs
	• North Central US paired with South Central US and so on,, ( as seen in above pic)
![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/163f8eeb-a841-4e92-b774-72e1fa88aaab)
![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/8aec649d-79ec-4a70-8a93-a0cba29de52d)

![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/e13f1c2f-baa7-4b1a-846f-c21743688f64)






Data can be replicated between AZ there could be cost for it

Availability Zone vs Availability sets: While availability sets are used to protect applications from hardware failures within an Azure data center, availability zones, protect applications from complete Azure data center failures. 

An Availability Set  lets you spread your virtual machines across physical hardware in different fault domains and update domains

Update domains indicate groups of virtual machines and underlying physical hardware that can be rebooted at the same time for any Maintenace activity by Azure like driver update or underlying platform patch update.

Fault domains define the group of virtual machines that share a common power source and network switch. By default, the virtual machines configured within your availability set are separated across up to three fault domains


To get 99.9SLA we have to attach a premium disk to the VM. Choose premium not standard


Resource Groups
	• Each resource should only reside in one and only one resource group 
	• An RG can contain resources that reside in different regions
	• You decide how to allocate resources to a RG based on how it makes sense to your organization
	• You can move resources from one RG to another
	• Resources for an application does not have to reside in the same RG but it is recommended to keep them in same RG

![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/acda0813-2f0e-4167-b6c7-30f8899e5f02)


Azure resource Manager
	• Is a management layer in which RGs, and all the resources within it is created, configured, managed and deleted. It provided a consistent management layer which allows you to automate the deployment and configuration of these resources using different automation and scripting tools such as PowerShell, Azure CLI, Azure portal, Rest APIs or client SDKs

With Azure Resource Manager
	• Deploy application and resources
		○ Update manage delete resources within a solution with a  single coordinated operation
	• Organize Resources
		○ See what resources are linked by a dependency
		○ Apply tags to resources to categorize them for management tasks such as billing
	• Control Access to resources
		○ Control who in your org can perfom actions in the resources
		○ Manage permissions by defining roles
		○ Adding users or gropups to the roles
		○ Applying policies at the resource group level

#8: Explore Microsoft Azure Core Services
Module 02: Define Core Azure services and products

Azure compute is an on demand computing service for running cloud based applications.
	• Provides computing resources such as disks, processors,  memory,networking, and OS
	• These resources available on demand and available readily in minutes

Two most common services
	• VMs and containers


Azure VMs
	• Lets you create and use VMs in the cloud
	• Provides Iaas and can be used in a variety of different ways
	• When you need total control over an OS and an environment Azure VMs are an ideal choice
	• Just like a physical computer you are able to customize all the software running on a VM
	• This ability is helpful when you are running custom software and custom hosting configurations

VM Scale Sets
	• Are an Azure compute resource that you can use to deploy and manage a set of identical VMs
	• All VMs are configured the same within Azure VM Scale Sets
	• VM scale sets are design to support a true auto-scale, No pre-provisioning of VMs are required
	• Makes easier to build large scale servers targeting big compute, big data and containerized workloads 
	• As demand goes up more VMs can be added and VMs can be removed as demand goes down. This process can be manual automated or a combination of both

App Services
	• With App Services you can quickly build, deploy and scale enterprise grade web and mobile applications
	• You can create API apps running on any platform as well
	• Is a PaaS offering
	• You can meet rigorous performance, scalability, security and compliance requirements while using a fully managed platform 

Azure Functions
	• Perform compute actions based on an event

Module 02: Define Core Azure services and products
#11: Define Container services
	• If you wish to run multiple instances of an application on a single host machine, containers are an excellent option
	• Container orchestrator can start, stop and scale out container instances as needed 
	• Contrianers are an virrualuzation environment. Unlike virtual machines you do not manage the OS
	• Containers are lightweight and are designed to be created scaled out and stopped dynamically
	• Axure support docker containers as well

There are two ways to manage both Docker and Microsoft based containers in Azure
	• First one is called Azure Container Instances
		○ Offers the fasest and simplest way to run a container in Azure without having to manage any VM or adopt any additional services
		○ It is a PaaS offering that allows you to upload your conainers which it will run for you
	• The second option is Azure Kubernetes Service
	• The task of automating, managing and interacting with large numbers of containers is known as orchestration 
		○ AKS is a complete orchestration service for containerss with distributed architectures and large volume of containers
	
	• Containers are often used to create solutions using microservice architecture. 
		○ This architecture is where you break solutions into smaller independent pieces
		○ For example, you may split a website into a container for hosting your front end another hosting your backend and the third for your storage
		○ This split allows you to create a different portion of your application into logical sections that it can be maintained, scaled and updated independently
ACI - Azure Container Instance

Module 02: Define Core Azure services and products
#13: Explore Azure Network Services

Azure networking allows you to connect cloud and on-prem infrastructure and services to provide your customers and users the best possible experience

Once the resources are moved to Azure they require same networking functionalities as an on prem deployment

In specific scenraios they may even require some level of network isolation as well

Some of the most Azure networking services are discussed below

Azure Virtual Network
	• Enables many types of azure resources such as Azure VMs to securely communicate with each other through internet and on prem networks as well
	• A virtual network is scoped to a single region however multiple virtual networks from different regions can be connected using virtual network peering 
	• With Azure Virtual Network, you can provide isolation, segmentation, communication with on-prem and cloud resources, routing and filtering of network traffic

Azure Load Balancer![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/52e598a4-f59a-4231-8529-df6e41f51c7d)


	• Automatically scales to create highly avaialble access to applications or resources
	• Load balance supports inbound and outbound scenarios
	• This provides low latency and high throughput and scales to millions of flows of TCP and UDP applications
	• Can be used with incoming internet traffic, internal traffic across Azure services, port forwarding for specific traffic or outbound connectivity for VMs in your virtual network as well

VPN Gateway
	• A specific type of virtual network gateway that is used to send encrypted traffic between Azure virtual network and an on prem location over public internet. More secure connection from on prem to Azure 

Azure Application Gateway![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/2644680d-ef26-4442-9533-86fb245a04bd)



	• Is a web traffic load balancer. This enables you to manage traffic to your web applications.
	• It is the connection through which users connect to your application 
	• With AAG, you can route traffic based on source IP address and port to destination IP address and port 

Content Delivery Network
	• CDN is a distributed network of servers that can effectively deliver web content to users
	• Is a way to get content to users in their local region to minimize latency
	• CDN can be hosted in Azure or any other location. You can cache content at a strategically placed physical node across the world  and provide better performance to end users
	• Typical usage scenario include web applications containing multimedia content, a product lounge even in a region or any event where you can expect a high bandwidth in a region

While removing VMs the disks have to be removed as well separately

Module 02: Define Core Azure services and products
#15: Explore Azure Storage Services
When you think about data categories you can simply thin of data as
	• Structured data
		○ Adheres to a Schema so all the data has the same fields or properties. Eg: Sensor data and financial data
		○ Cab be stored in a database table with rows and columns
		○ Relies on keys to indicate how one row in a table relates to data in another row of another table
		○ Aka relational data
		○ Easier to enter,query and analyze because all of the data follows  the same format
	• Semi-structured data
		○ Is less organized than structured data
		○ Not stored In a rational format meaning the field do not neatly fit into table rows and columns
		○ Contains tags that make the origanization and hierarchy of the data apparent
		○ Aka non relational or non-sql data
		○ Examples are book, HTML documents, JSON, blogs
	• Unstructured data
		○ Has no designed structure
		○ Can hold any kind of data
		○ Is becoming more prominent asa businesses try to tap into more data sources
		○ Examples PDFs, JPGs, Videos
	
	Lets explore different Azure storage products to support each different data type
	
Azure Storage
	• Is a service that you can use to store files, messages, tables and other types of information
	• You can use Azure storage on its own for example as a fileshare but developers also often use it to store their working data
	• Such stores can be used  used by websites , mobile apps desltop apps and many other custom solutions
	• Azure storage is also used by IaaS virtual machine and PaaS cloud offerings as well

Some of the most common storage types in Azure are
	• Disk 
	• Files
	• Objects
	• Queues
	• Tables

![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/564ddb56-9cbf-413a-b0c6-3a930091c334)


Disks              --IaaS
	• Disk storage provides disk for virtual machines, applications and other services to acceess and use as they need similar to how they are used in an on-prem scenario
	• Allows data to be persistently stored and accessed from an attached virtual harddisk
	• A disk can be managed or unmanaged by Azure therefore managed and configured by the user
	• Disks come in many different sizes and performance levels- SSDs HDDs and varying perfomance abilitiees

Azure  Files       ----IaaS
	• Enables you to set  up a highly available network files share that can be accessed by using the SMB protocol meaning that multiple VMs can share the same files with both read and write access
	• One thing that distinguishes Azure Files from files on  a corporate file share is that you can access the files from anywhere in the world using URL
	• Some of the most common scenarios where you can use Azure Files are: 
		○ Many on-prem apps use file share this feature makes it easier to migrate those applications to the shared data to Azure
		○ Another scenario is you can use the Azure fileshare for storing the diagnostic logs, metrics and crash dumps

Blobs or Containers      ----PaaS
	• Microsoft's object storage solution for the cloud
	• Is optimized for storing massive amount of unstructured data such as text or binary data
	• Ideal for 
		○ serving images or documents directly to a browser
		○ Storing files for distributed access
		○ Streaming video or audio
		○ Storing data for backup and restore
		○ Disaster recovery and archiving 
		○ Storing data for analysis by an on-premises or an Azure hosted services

Tables    --PaaS
	• Stores large amount of structured data
	• Ideal for storing structured non-relational data
	• Common use:
		○ Storing TBs of structured data capable of serving web scale applications
		○ Storing data set that does not require complex joins
		○ Store and query huge sets of structured and non-relational data 
		○ Your tables will scale as demand increases

Queues   ---PaaS
	• Used to store and retrieve messages
	• Can be held up to 64Kb in size
	• Can contain millions of messages


Azure Dashboard can be customized
Delete resources immediately if not needed 
Monitor storage account at Monitor>Insight

Module 02: Define Core Azure services and products
#17: Explore Azure Database Services

Azure Database  Service
	• Is a fully managed PaaS database service that free up valuable time that you would otherwise spend managing your database
	• Developers can take advantage of industry leading innovation such as:
		○  built in security with automatic monitoring 
		○ Threat protection
		○ Automatic tuning for improved performance
		○ Turnkey global distribution

Common database services in Azure are:

Azure CosmosDB
	• Microsoft Azure cosmosDB is a globally distributed database service that enables you to elastically and independently scale throughput and storage across any number of Azure geographic regions
	• It supports schema-less data that lets you build high responsive and always on application to support constantly changing data
	• You can use CosmosDB to store data that is updated and maintained by users around the world
	• It makes it easy to build scalable highly responsive applications at global scale


Azure SQL Database ---PaaS
	• Is a Relational Database As A Service(Daas)
	• Is based on the latest table version of Microsoft SQL database engine 
	• SQL database is a high performance, reliable, fully managed and secure database that you can use to build data driven applications and websites
	• You can use programming language of your choice without needing to maintain infrastructure

Azure Database Migration
	• Is a fully managed service designed to enable seamless migrations from multiple database sources to Azure data platforms with minimal downtime 
	• The services uses Microsoft data migration assistant to generate assessment report that provide recommendations to help guide you through required changes prior to performing a migration.
	• Once you assess and perform any remediation required you are ready to begin the migration process
	• The Azure databases migration service performs all the required steps

Walkthrough at https://youtu.be/j26eNpUU0zM?si=QzFANfUNZTYWcv7u&t=7339
	• Create the database
	• Query the database


Module 02: Define Core Azure services and products
#19: Explore Azure Marketplace

Azure Marketplace
	• Is a service on Azure that helps connect end users with Microsoft partners
	• ISV are independent software vendors and startups that are offering  their solutions and services which are optimized to run on Azure
	• Allows customers mostly IT professionals and cloud developers to find,try ,purchase  and provision applications and services from hundreds of leading service providers all certified to run on Azure
	• Using Azure Marketplace you can provision end-to-end solution quickly and reliably

Module 03: Identify Azure solutions
#20: Define Internet of Things

Internet of Things
	• Personal computers used to be the norm and now the internet allows any item that is online capable to access valuable information 
	• The internet of Things is the ability for devices to garner and then relay information for data analysis

Azure IOT Central
	• Is a fully managed global SaaS solution
	• Makes it easier to connect, monitor and manage your IOT assets at scale
	• Node cloud expertise is required to use IOT central
	• As a result you can bring your connected product to market faster  while staying focused on your cutomers

Azure IoT Hub
	• Is a managed service hosted in the cloud that acts as a central message hub for bi-directional communication between your IoT application and the devices it manages
	• You can use IoT hub to build IoT solutions with reliable and secure communications between millions of IoT devices and a cloud hosted solutions backend
	• You can connect virtually any device to your IoT hub
	• IoT hub supports communication form both the IoT device to the cloud and cloud to the IoT device as well
	• Also supports multiple messaging patterns such as :
		○  device to cloud telemetry 
		○ File upload from devices
		○ And request relay methods to control your devices from the cloud
	• IoT monitoring helps  you maintain the health of your solution by tracking events such as device creation, device failures and device connections
	• IoT hub's capabilities helps you  build scalable full featuread IoT solutions such as managing industrial equipments used in manufacturing, tracking valuable assets in health care and monitoring office building usage

These are just two of Azure's IoT offering

Use the IoT product selector to determine what product is best for your situation

Walkthrough at https://youtu.be/j26eNpUU0zM?si=OGxw63FFF7GFISa8&t=8107
	Create an Azure IoT Hub in Azure Portal and configure the
	hub to authenticate a connection to an IoT device using the
	Raspberry Pi device simulator.
	1. Create an IoT Hub.
	2. Add an IoT device.
	3. Test the device using the Raspberry Pi Simulator.
	
Module 03: Identify Azure solutions
#22: Explore Big data and analytics
Explore Artificial Intelligence
Define Serverless computing

Data comes in all types of forms and formats, when we talk about big data we are referring to large volumes of data
	• Data from weather systems communication systems, imaging platforms and many other scenarios generate large amounts of data
	• This amount of data becomes increasingly hard to make sense of and make decisions around
	• The volumes are so large that traditional forms of processing and analysis are no longer appropriate

Azure Synapse Analytics
	• Formerly known as Azure SQL data warehouse
	• Is a limitless analytics service that brings together enterprise data warehousing and big data analytics
	• All in one compared to SQL, monitor, security,etc

Azure HD insight
	• Is a fully managed open source analytics service for enterprises. It is a cloud service that makes it easier, faster and more cost-effective to process massive amounts of data
	• HD insight allows you to run popular opensource frameworks and create cluster types such as Apache spark Apache Hadoop Apache Kafka Apache HBase Apache storm and machine learning services
	• HDInsight also supports a broad range of scenarios such as extraction, transformation, loading, data warehousing, machine learning and IoT

Azure Data Lake Analytics
	• Is an on-demand analytics jobs service that simplifies big data, instead of deploying configuring tuning hardware you write queries to transform your data and extract valuable insights
	• The analytics service can handle jobs of any scale instantly by setting the dial for how much power you need, you only pay for your job when it is running making it more cost effective than other services

![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/95981db6-b942-4a2b-847e-202759138716)

	² Artificial intelligence in the context of cloud computing is based around broad range of services the core of which is machine learning. 
	² Machine learning is a data science technique that allows computers to use existing data to forecast future behaviors, outcomes and trends 
	² Using machine learning computers learn without being explicitly programmed

Azure Machine Learning Service
	• Provides a cloud based environment you can use to develop, train, test,deploy, manage and track machine learning models
	• It fully supports open source technologies. So you can use tens of thousands of open source Python packages with machine learning components such as transfer and skin clone
	• Azure Machine Learning Services also include features that automate model generation and tuning to help you create models with ease, efficiency  and accuracy
	• The Azure machine learning service can auto generate a model and auto tune it for you as well

Azure Machine Learning Studio
	• Collaborative drag and drop visual workspace where you can build test and deploy machine learning solutions without needing to write a code
	• It uses pre-built and pre-configured machine learning algorithms and data handling models
	• Use Machine Learning Studio when you want to experiment with machine learning models quickly and easily
	• Built in machine learning algorithms are enough for your solutions
	• Does not provide as much control over algorithms as Machine Learning Services

A full list of AI and ML solutions are available so you should check out that list before selecting the right one for you

Serverless Computing  is a cloud hosted execution environment that runs your code but abstracts the underlying hosting environment
	• You create an instacne of a service and you add your code
	• No infrastructure configuration or maintenance is required or even allowed
	• You configure your serverless app to respond to events, an event could be a REST end point, a periodic timer or even a message received from another Azure service
	• The serverless app runs only when it is triggered by an event

Azure Functions
	• Are ideal when you are only concerned about the code running your service and not the underlying platform or infrastructure
	• Commonly used when you need to perform work in response to an event often via a REST request, timer or a message or from an Azure service
	• Azure functions scale automatically and change happen only when the function is triggered so there is solid choice when demand is variable
		○ For example, you may be receiving message from an IoT solution that monitos a fleet of delivery vehicles, you will likely have more data arriving during business hours so Azure function can scale out to accommodate these busier times
	• Azure Functions are stateless, they behave as if they are restarted everytime they respond to an event, this is ideal for processing incoming data and if state is required they can be connected to an Azure storage solution 

Azure Logic Apps
Introduction to Azure Logic Apps


	• A way to connect all the apps and services your business relies on
	• Is a cloud service that help you automate and orchestrate tasks, business processe and workflows when you need to integrate apps, data, systems and services across enterprise or organizations
	• Logic app simplifies how you design and build scalable solutions whether in the cloud, on-prem or both 
	• logic apps are designed in a web based designer and can execute logic triggered in  Azure services without writing any code
	• To build enterprise integration solutions with Azure logic apps, you can choose from a growing gallery of over 200 connectors these include services such as Salesforce, SAP, oracle DB and file shares

Azure Even Grid
An overview of Azure Event Grid


	• Even grid allows you to easily build application  with Event based architectures, it’s a fully managed intelligent Event routing service that uses a public subscriber model for uniform event consumption
	• Event grid has built in support for events coming from Azure services such as storage blob and resource groups
	• You can use event grid to support you own non-azure based events in near real time
	• Using custom topics you can use filters to route specific events to different endpoints as well and ensure your events are reliably delivered

Walkthrough Microsoft Azure Fundamentals [Exam AZ-900] Full Course




Explore Microsoft Azure Core Services
Module 03: Identify Azure solutions
#24: Explore DevOps
Explore Azure App Service

Azure DevOps Services
	• Brings together people, process and technology
	• Allow you to create, build and release pipelines that provides continuous integration, delivery and deployment for your applications
	• You can integrate repositories and application tests, perform application monitoring  and work with build artifacts
	• You can also work with an backlog items for tracking, automate infrastructure deployment and integrate a range of third party tools and services such as jenkins and chef
	• All these fuctions and many more are closely integrated with Azure to allow for consistent repeatable deployment for your applications to provide streamlined build and release processes

Some of the main devops services available in Azure are Azure DevOps services and Azure Dev Test labs

Azure DevOps Services
	• Provides development collaboration tools including 
		○ high performance pipelines
		○ Free private git repositories
		○ Configurable kanban boards
		○ Extensive automated and cloud based load testing
	• DevOps services are formerly known as visual studio team services or VSTS

Azure DevTest Labs/Lab services
	• Is a service that helps developers and testers quickly create environments in Azure while minimizing waste and controlling cost
	• Users can test their latest application versions by quickly provisioning Windows and Linux environment using reusable artifacts and templates
	• You can easily integrate your deployment pipeline with dev test labs to provision on demand environments
	• With DevTest labs you can scale up your load testing by provisioning multiple test engines and create pre-provisioned environment for training and demos

Explore Azure App Service
	• Azure App Services Is a collection of four services
		○ Web apps
		○ Mobile apps
		○ API apps
		○ Logical Apps or Logic Apps
	• Easily and quickly build web and mobile app for any platform or any device
	• Azure App Service enable you to build and host web apps, mobile backends and RESTful APIs in programming language of your choice without managing infrastructure
	• It offers autoscaling and high availability
	• Supports both Windows and Linux
	• Enables automated deployment from GitHub, Azure DevOps or any other git repository
	• Some of the key features of Azure app service are multiple languages and frameworks
	• Has first class support for ASP.net, ASP.net core Java Ruby Node JS PHP or Python
	• You can also run powershells  and other scripts or executables as background services
	• Global scale and high availability
		○ Scale up or out manually or automatically 
		○ Host your app anywhere in Microsoft global data center infrastructure
		○ App service SLAs promise high availability
	• Security and compliance
		○ App services ISO,SOC and PCI compliant
		○ Authenticate users with Azure Active Directory ot with social sign ins like google
		○ You can create IP address restrictions and manage service identities
	• Visual Studio Integration
		○ Dedicated tools in visual studio streamline the work of creating, deploying  and debugging 

Walkthrough Microsoft Azure Fundamentals [Exam AZ-900] Full Course
Create a web app



#26: Module 04: Differentiate Azure management tools
	• Review Azure Management Tools
	• Explore Azure Advisor
	• Create Azure resources using different tools


Azure Management Tools
![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/ceb4d0ac-9f58-4d2b-b641-a8609cf67903)

You can configure and manage Azure using a broad range of tools and platforms
	• There are tools available for command line
	• Language specific Software Development Kits (SDKs)
	• Developer tools
	• Tools for mugration
	• And more

One of the tools is Azure portal
 
Azure Portal
	• Is a public website that you can access with any web browser
	• After you sign in with your Azure account you can create manage and monitor any available Azure sercvices
	• You can identify a service you are looking for, get links to help on a topic and deploy manage and delete resources
	• It also guide you through complex administrative tasks using wizards and tooltips
	• The dashboard tool	Provides high level details about the Azure environment
		You can customize the portal view as you need by customizing and resizing tiles
		• Displaying particular services of interest
		• Accessign links for help and support 
		• Provide feedback
		

	• The portal doesn’t provide any way to automate repetetive task. For example, to set up multiple VMs you would need to create them one by one at a time
		○ Completing a wizard can be time consuming and error prone for complex tasks


Azure PowerShell for instance is a module that you can add to Windows PowerShell or PowerShell core that enables you to connect to your Azure subscription and manage resiurces
	• Azure powershell requires Windows PowerShell to function

The powershell provided services such as shell window and command parsing. Azure PowerShell then adds the Azure specific commands.
	• For example, Azure PowerShell provides new-az vm command that creates a new virtual machine for you inside your Azure subscription

PowerShell core is a cross platform version of PS that runs on Win, Linux or Mac

AzureCLI
	• Is a cross platform command line program that connects to Azure and executes Azure administrative commands on Azure resources
	• Can be run on Win,Linux or Mac
	• For example, to create a VM, you would open a command prompt window, sign in with Azure such as az login command, create a resource group then use commands

Azure CloudShell
	• Is a browser based scripting environment in your portal
	• It Provides the flexibility of choosing the shell experience that best suite the way you work
		○ Linux users can opt in for bash experience, while Windows users can opt in for PowerShell
	• A storage account is required to use the cloudshell.  And you will be prompted to create one when you access this Cloud Shell from Azure portal

Azure Mobile App
	• Allows you to access, manage and monitor all your Azure accounts and resources from your iOS and Android phone or tablet
	• Once installed you can 
		○ check the status of important metrics of your services,
		○  stay informed with notification and alerts about important health issues, 
		○ quickly diagnose and fix issues anytime and anywhere,
		○ Review the latest Azure alerts
		○ Start, stop or restart VMs or web apps 
		○ Connect to your Azure VMs
		○ Manage permissions with role based access control
		○ Use the Azure Cloud Shell to run saved scripts or perform unplanned administrative tasks etc

Azure REST API
	• REST APIs are service end points that support sets of HTTP operations methods which provide create, retreive update or delete access to the service resources
	• A REST API defines a set of functions which developers can perform, request and receive responses via HTTP protocol such as GET and POST 


Azure Advisor
	• Analyses your deployed Azure resources and recommends ways to improve availability, security, performance and costs
	• Free service built into Azure
	• You can access Azure Advisor through Azure portal, after you sign into the portal, you just selcet Advisor from the navigation menu or search for it in the all services menu
	• With Advisor you can get proactive, actionable and personalized best practices recommnedations
	• Improve performance, security and high availability within your resources as you identify opportunities to reduce the overall Azure cost
	• Recommnedations with proposed inline actions as well
	• Reports can be downloaded in PDF format or CSV 
		○ You would be able to share this report with your security team 

Walkthrough 27:
Create gallery image using Azure ARM(Azure Resource Manager) template
Microsoft Azure Fundamentals [Exam AZ-900] Full Course



	• Templates can automate lot of tasks for you
	• https://azure.microsoft.com/en-in/products/arm-templates link for ARM templates
	• They are in JSON format
	• The templates can be edited, customized, appended with extra code,
		○ Example, in a template to deploy a VM, the name of the VM can be edited
	• Templates are basically codes for performing certain actions
	• While using template to create VM, Usernames and Password for the VM are to be given


Walkthrough 28:
Create a VM with PS Microsoft Azure Fundamentals [Exam AZ-900] Full Course



	• When a VM is stopped and deallocated (can be checked at Status) you do not have to pay for the compute, but for the storage

Walkthrough 29:
Create VM with Azure CLI Microsoft Azure Fundamentals [Exam AZ-900] Full Course





Answers to questions of prev. module
Azure Geographies is a  region or group of regions that maintains compliance and data residency boundaries. Geographies allow customers to keep their data and applications close by

Geographies allow customers with specific data residency and compliance to keep their data and applications close
Geographies ensure that data residency, sovereignity,clients and resilience requirements are honored within the geographical boundaries

As part of the best practice, all resources that are part of an application and share the same lifecycle should be placed in the same resource group

Availability set is something which will give you high availability from fault tolerance and update domain
Availability zone will give you high availability from data center disaster point of view

Virtual machine scale set lets you deploy and manage a set of identical virtual machines 

Azure App servie is a PaaS, which you can use to create web apps, mobile apps, APIs etc

Azure functions are ideal when you are concerned only about code running your service and not the underlying platform or infrastructure

Azure resource manager templates use JSON format
Cosmos DB is a globally distributed highly available database service

Azure content Delivery network or CDN is a distributed network of servers that can effectively deliver web content to users

Blobs 
	• Is where you keep unstructured data and it supports massive amount of data as well
	• Object storage solution for the cloud by Microsoft
	• Blobs are optimized for storing massive amounts of unstructured data such as text binary data photos and videos

Files  is where you create a SMB protocol fileshare
Ques  is where you create applications that require messaging services

HD insight is part of Azure database services
Azure DevTest labs is part of Azure DevOPs services
Azure Machine Learning service provide a cloud based environment that you can use to develop train, test, deploy manage and track machine learning models

Azure DevOps services include development collaboration tools including high performance pipeline, free private git repositories and configurable kanban boards

Azure data centers are organized and made available by regions

Scale set is used to scale up and scale down the number of instances of VM
Availability Zones will give you high availability interms of failure of a datacenter

Availability set provides VM redundancy and availability, this configuration within a data center ensures that during either a planned or unplanned maintenance event  at least one VM is available and meets the 99.95 Azure SLA

Azure Load Balancer distributes traffic among similar systems, making your service more highly available
	• If one system is unavailable Azure Load Balancer stops sending traffic to it and then directs traffic to one of the responsive servers
It works with internal as well as external traffic
	• It is not necessary to use Azure Load Balancer if you want to distribute traffic among your VMs running in Azure

AzureCLI is the best management tool to for Android phone with the least amount of administrative effort




Third learning path
#31: Examine Microsoft Azure Security, Privacy,
Compliance, and Trust
Module01: Securing Network Connectivity

We shall learn about:
	• The security responsibility is shared between you and the cloud service provider which is Microsoft
	• How to identify management porvider's protection even outside your network
	• Learn about encryption capabilities built into Azure that can protect your data

Exploring defense in depth
	• A strategy that employs a series of mechanisms to slow the advance of an attack aimed at aquiring unauthorized access to data
	• The objective of defense in depth is to predict and prevent the information being stolen by individuals not authorized to access it
	• The common principles used to define a security posture are confidentiality, integrity and  availability known collectively as CIA
	• Defense in depth can be visualised as a set of layers with the data to be srcured at the center, each layer provide protection so that if one layer is breached, a subsequel layer is already in place to prevent further exposure
	• This approach removes reliance on any single layer of protection and acts to slow down an attack  and provide alert telemetry that can be acted upon either automatically or manually
![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/160acfac-b8b6-405e-80da-f27e5443ca2d)


Physical security - First line of defense to protect computing hardware in the data center
Identity and access  - controls, access to infrastructure and change control
Perimeter - this layer uses DDoS protection to filter large scale attacks before they can cause any denial of service for end users
Network - Networking layer limits communication between resources through segmentation and access controls
Compute - this layer secures accesss to virtual machines
Application - ensures that applications are secure and free of vulnerabilities
Data - attackers are after the data, which are stored in a database or stored in a disk inside the virtual machine or stored in a SaaS application such as office 365 or stored in a cloud storage, it is the responsibility of those storing and controlling access to the data to ensure that it is properly secured. Often there are regulatory requirements that dictates the commands and process that must be in place to ensure the confidentiality, integrity and availability of the data
![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/71e5ecb9-3b27-4461-881c-58449a3d3b70)


Saas require less from CX point of view
On-prem requires allf from CX point of view

Explore Azure Firewall
	• Service that grants server access based on originating IP address of each request
	• You create firewall rules and specify IP address, only clients from these generated IP addresses will be allowed to access the server
	• Firewall rules also include specific network protocol and port information as well
	• Azure firewall is a managed cloud based network security service that protects your Azure network resources
	• It is a fully stateful firewall as a service with built in high availability and unrestricted cloud scalability
	• You can create enforce and log applications and network connectivity policies across subscriptions
	• Azure firewall uses a static public IP address for your network resources which allows outside firewalls to identify traffic originating from your virtual network
	• The service is fully integrated with Azure monitor for logging and analytics
	• Azure firewall provides many features including built In high availability unrestricted cloud scalability, inbound and outbound filtering rules and Azure monitoring logging as well
	• With Azure firewall you can configure application rules that define FQDNs, network rules that define source address protocol, destination port and destination addresses

Azure application gateway also provides a firewall called web application firewall or WAF
	• Provides centralized inbound protection for your web applications against common exploits and vulnerabilities

Explore DDoS protection
	• DDoS makes app slow or unresponsive to legitimate users
	• Can be targeted at any end-point that is publicly reachable through the internet
	• Any resource exposed to internet is potentially at risk from DDoS attack

	• Azzure DDoS protection identifies the attacking traffic and blocks it, legitimate traffic from CX still flows through, without an interruption of services

Azure DDoS protection provides different tires Basic and Standard
	• Basic tier is automatically enabled as part of the Azure platform.
		○ Always on traffic monitoring and realtime mitigation of common network level attacks provides the same defenses that Microsoft onlline services use
	• Stanadad Tier
		○ Provides additional mitigation capabilities that are tuned specifically to Microsoft Azure virtual network resources
		○ Is simple to enable and requires no application changes
		○ Protection  policies are tuned through dedicated traffic monitoring and machine learning algorithms
		○ Policies are applied to public IP addesses which are asssociated with resources deployed in virtual network such as Azure load balancer and application gateway

Network Security Groups(NSGs)
	• Allows you to filter network traffic to and from Azure resources in an Azure virtual network
	• An NSG can contain multiple inbound and outbound security rules that enable you to filter traffic to and from resources by source and destination IP address, port and protocol

Application Security Groups
	• Enable you to configure network security as a natural extension of an application structure
	• Allowing you to group virtual machines and define network security policies based on those groups
	• This feature allows you to reuse your security policy at scale without manual maintenance or explicit IP addresses
	• The platform handles security od explicit IP addresses and mutliple rule sets allowing you to focus on your business logic

When considering Azure security solutions, consider all the elements of defense in depth

Perimeter layer
	• Protects your networks' boundaries with Azure DDoS protection and Azure firewall
	• Is about protecting organizations from network based attack against your resources
	• Identifying these attacks, alerting and eliminating their impact is importanat to keep your network secure

Network Layer
	• At this layer the focus is on limiting network connectivity across all your resources to only allow what is required
	• Segment ypur resources and use network network level controls to restrict communication to only what is needed
	• By restricting connectivity you reduce the risk of  lateral movement throughout your network

#32 Walkthrough
Secure network traffic
	• Create and configure inbound and outbound security port rules7
	1. Deploy a custom template to create a virtual machine.
	2. Create a network security group.
	3. Create an inbound security port rule to allow RDP.
	4. Configure an outbound security port rule to deny Internet
	access.
Microsoft Azure Fundamentals [Exam AZ-900] Full Course




We are gonna  create a Windows server 2019 virtual machine
	1. Select your subscription
	2. Select resource group
		a. Needed before creating any resource in Azure
	3. Name your virtual machine
	4. Choose region 
	5. Image select windows server 2019
	6. Give username and password for windows

By default there are lots of options where you can configure to allow any ports within your VM
In this instance because we are trying to secure the network and test it I am not going to allow any inbound port
That means to connections to and from the VM

In the netwoking tab we are gonna set nic 'NIC network security group' to None

Finally we validate all settings and create VM

During deployment of the VM what happens is 

	• It creates a VM
	• Beofre that it creates a brand new vnet and a default subnet to place this VM, and a NIC and a public IP for connecting to the VM as well

Once the VM is created we go to that resource
There you can see its status 
Where it hosted location of it
Whats the iP addess etc

While looking at the networking tab we can see there are no inbound and outbound rules and no applictaion security groups as well, as seen below:
![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/2f43d2ec-0e72-427b-83ce-6ceeeb13a890)



Next step: Create a new NSG, network security group and assign it to the VM

You can go to all services and type in network security group
Select NSG
We can see there are no NSGs at the moment
	• Click on ADD
	• Select subs and resour grp
	• Name the NSG
	• Same region as VM?
	• Create
	• NSG is a PaaS offering
	• It is created quickly theres no much background work needed

Once the NSG is created, when we go to the resource we can see there are some default inbound and outbound rules created
	• You wont be able to modify or delete these rules

Now we have the NSG created we are gonna associate this NSG to the NIC of the VM we created 
Go to Network interfces in NSG
![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/2940de17-9584-49b1-90eb-c6dca7f7103f)


Click on associate as can be seen above and click on the NIC

So now if we go to the VM > networking tab
	• We can see all the port rules of the NSG are now part of the VM as well, as seen below:
	• 
![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/81ee2774-358a-478c-bee0-35db4d22001b)


Now go and try to connect to the VM via RDP
	• Will not be successful as all inbound port traffic is denied

Click on 'Add Inbound Security Rule'
	• Select 'source' as any
	• Source port ranges - *
	• Desitnation - any
	• Destination port trange - 3389  for RDP
	• Protocol - TCP
	• Action - Allow 
	• We gonna select lower priority, so that lower priority take precedence of all the other numbers, here we choose - 300
	• Name the rule - Allow RDP

Now connect via RDP - sucessful

Now we shall go ahead and create outbound port rules to restrict outbound access to internet

In VM>networking tab we click onoutbound port rules tab
So we annot change the exisitng port rules, note the priority number
![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/59ed257b-cf0a-4e68-af0f-85a48c6fdeb2)


We see default internet  outbound allowed
So we shall create new outbound rule to deny internet access
We set priority number to lower than the existing 65001 for AllInternetOutBound
The lower the number the higher the priority


#33: Examine Microsoft Azure Security, Privacy,
Compliance, and Trust

Module 02: Core Azure Identity Services

Learning objectives:
Review authentication versus authorization
Explain Azure Active Directory
Explore Azure Multi-factor authentication (MFA)


Two concepts are fundamental to understanding identity and access: Authentication and Autherization
![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/09e6db9d-8088-4432-b33d-fac3e72a3c80)


They underpin everything else that happens and occurs sequentially in any identity and access process

Authentication
	• Process of establishing the identity of a person or service looking to access a resource
	• It involves the act of challenging a party for legitimate credentials and provided the basis for creating a security principle for identity and access control use
	• Sometimes shortened as Auth n
	

Authorization
	• Is the process  of establishing what level of access an authenticated person or service has
	• It specifies what data they are allowed to access and what they can do with it 
	• Shortened as Auth z

Explore Azure Active Directory (AD)
	• Is mircrosofts cloud based identity and access management service
		○ Authentication (employees sign-in to access resources).
			§ Verifying identity to access applications and resources 
			§ Provide functionalities such as self-service password reset, multi-factor authentication, a custom band password list, and smart lock out features as well
		○ Single sign-on (SSO).
			§ Enables users to remember only one ID  and password to access multiple apps
			§ A single identity is tiered to a user simplifying the security models
			§ As users change roles or leave an organization access modification are tied to that identity greatly reducing the afford to need, to change or disable accounts
		○ Application management.
			§ You can manage your cloud and on-prem app using Azure AD application proxy, single sign-on, myapps portal also referred to as access panel and SaaS apps
		○ Business to Business (B2B).
			§ Is an identity services allows to manage your guest users and external partners while maintaining control over your own corporate data
		○ Business to Customer (B2C) identity services.
			§ Is also an identity services, which will help you customize and control how users sign up, sign in and manage their profiles when using your apps with services
		○ Device management.
			§ Let you manage how your cloud, or on prem devices access your corporate data
	AD can be used for external or internal resources as well
	

	
	
	When AzureAD is accessed in Azure, we can see many options:
	• Users
		○ You can see both your cloud borne users, your guest users like invited user or Windows Server AD users those are the users which is migrated or moved from your on-prem AD to your Azure AD
	• Groups
		○ Includes groups that you created within the Azure AD or the groups which is migrated over to Azure AD from your on-prem as well
		○ You can enable self-service group management to your users as well
	• Enterprise applications
		○ You can allow users to access multiple other vendor applications to use a single identity which is your azure AD or your office 365 identity
		○ You can click on new application to add an app which you wanna integrate with your Azure AD, this can be a gallery app or something you are developing as well
	• Security
		○ Here you can configure lot of additional things like conditional access, MFA etc
	• MAM and MDM
		○ Configure device enrollment policy
	• Custom domain
		○ Add a custom domain name
	• Licenses
		○ You can manage your licenses within Azure AD, 
		○ Licneses>all products lists down all the available licenses and who it has been assigned to , expiry etc

And there are lot of other things in Azure AD, for az900 this is enough


Explore Azure Multi-Factor Authentication
	• Provides additional security for your identities by requiring two or more elements for full authentication
	• These elements fall into three categories
		○ Something you know
			§ Could be a password
			§ Or answer to a security question
		○ Something you possess
			§ Mobile app that recieves a notification or a token generating device
		○ Something you are
			§ Biometrics

MFA comes as a part of following Microsoft Azure Service Offerings
	1. Azure AD premium licenses
	2. For your Office 365 services
	3. Azure AD global administrators because global administrators accounts are highly sensitive, a subset of Azure MFA capabilities are available to protect these accounts

When in Azure AD, go to Users and theres a tab for MFA
You get to this page once clicked on it

	• Depending on the license you have you can see which users have MFA and which ones don’t
	• You can enable and disable MFA for each user
	• In service settings tab as can be seen above
		○ You can configure trusted IP, users who are part of that IP address will not be prompted for a dual factor auth
		○ In this tab you can also choose how many verification methods users should complete eg: call to phone, text message to phone, notification through mobile app
		○ In this tab we can also configure to remember  multi factor auth  for how many number of days so that users will not be prompted for a second MFA if they have already gone through a verification  within the number of days you choose there



Examine Microsoft Azure Security, Privacy, Compliance,
and Trust

Module 03: Security Tools and Features
#34: AIP & ATP

Two very important concepts and lessons for security AIP and ATP

AIP: Azure information protection
ATP: Azure advances threat protection or Azure ATP

We shall also look into Azure security center and Azure Key Vault as well

AIP:
	• Is a cloud based solution that help organizations classify and protect its documents and emails by applying labels
	• Labels can be applied automatically, manually or with the combination of both, guided by recommendations
The following screencapture is an example of Microsoft Azure Information protection

In this example the administrator has configured a label with rules that detect sensitive data
When the user saves a microsoft word document containing a credit card number, a custom tooltip is displayed, the tooltip recommends labelling the file as confidential, all employees etc

	• AIP can be purchased either as a standalone solution or through on eof the following Micorosft licensing suite
		○ Enterprise mobility plus security
		○ Microsoft 365 enterprise

ATP:
	• Azure Advanced Threat Protection
	• Is a cloud based security solution that identifies, detects and helps you investigate advanced threats, compromise identities and malicious insider actions directed at your organization
		○ Capable of detecting known malicious attacks and techniques, security issues and risk against your network

Some of the Azure ATP components include
	• Azure ATP portal
		○ Azure ATP has its own portal through which you can monitor and respond to suspicious activity
		○ The portal Allows you to create your Azure ATP instance and view the data received from Azure  ATP sensors
		○ The portal can also be used to monitor, manage and investigate threat in your network environment
	• Azure ATP sensor
		○ These sensors are installed directly on your domain controller
		○ The sensors monitor domain controller traffic without requiring a dedicated server or port mirroring
	• Azure ATP cloud service
		○ The ATP cloud service runs on Azure infrastructure and is currently deployed in united states, Europe and Asia
		○ Is connected to Microsoft intelligent security graph.


Module 03: Security Tools and Features
#35: Examine Azure Security Center

Azure Security Center
	• Is a monitoring service that provides protection across all your services both in Azure and on prem

What security center can do?
	• Provide security recommendations based on your configuration, resources and networks
	• Can monitor security settings across on-prem and cloud workloads
	• And automatically apply required security to new services as they come online
	• Can continuously monitor all your services and perform automatic security assessments to identify potential vulnerabilities before they can be exploited
	• Uses machine learning to detect and block malware from being installed on a virtual machine and services
	• You can define a list of allowed applications to ensure that  only the apps you validate can execute
	• Can analyze and identify potential inbound attacks and any post breach activity that might have occurred
	• Can provide just in time access, control for ports reducing your attack surface by ensuring the network only allows traffic that you require

#36: Walkthrough
Azure Security Center Usage Scenarios
Microsoft Azure Fundamentals [Exam AZ-900] Full Course




When you come to a particular service that you are going to frequently access, if you hover your mouse over its icon you can see a star on the corner of the  overlay, click on it  and it will feature on your control pane on the left so you don’t have to search for that option every time



Security center provides recommendations based on your configurations, resources and networks



Can continuously monitor all your services and perform automatic security assessments to identify potential vulnerabilities before they can be exploited
It uses ML to detect and block malware from being installed on your virtual machine and services,
You can also define a list of allowed application to ensure that only the apps you validate can execute here

It shows the overall secure score at the top
If you scroll down to the 'Controls' title, you can see recommendations like enable MFA, how to do that and if you enable how much points you will gain and things like that

The plans to get security center, there are two tiers
	1. Free tier
		a. Available as part of your Azure subscription
		b. It is limited to assessment and recommendation of your Azure resources only
	2. Standard tier
		a. Provides a full suite of security related services including continuous monitoring, threat detection, just in time access control for ports and more
		b. A 30 day free trial available


Module 03: Security Tools and Features
#36: Azure Key Vault

Azure Key Vault
	• Is a centralized cloud service for storing your application secrets
	• Helps you control your application secret by keeping them in a single central location and by providing secure access, permission control and access locking capabilities

Usage scenarios of Azure Key Vault are
	• Secret management
		○ To securely store and tightly control access  to tokens, passwords, certificates, application programming interface or API keys and other secrets as well
	• Key management
		○ You can use Azure Key Vault as your key management solution
		○ Key Vault makes it easier to create and manage encryption keys used to encrypt your data
	• Certificate management
		○ Lets you provision manage and deploy your public SSL and TLS certificates for your Azure and internally connected resources more easily
	• Storing secrets backed by HSMs (Hardware Security Modules)

Benefits of Azure Key Vault
	• Centralizing storage for application secrets allow you to control their distribution and reduces the chance that secrets may be accidentally leaked
	• Centralized storage rather than distributed
	• Azure uses  industry standard algorithms, key lengths and HSM and access require proper auth n and auth z that’s how it can securely store secrets and keys
	• Monitor and control to access your company secrets
	• Azure key vaults makes It easier to enroll and renew certificates from public certificate authorities like CAS
	• You can also scale up and replicate content within region and use standard certificate management tools
	• You can integrate Key Vault with Storage accounts, container registries, even hubs and many more Azure services


#38: Walkthrough:
Implement Azure Key Vault

Microsoft Azure Fundamentals [Exam AZ-900] Full Course



Creating Key vault
	• Search In all services
	• Click key vault
	• Click add
	• Give sub and rg name
	• Provide unique name for key vault
	• Region
	• Pricing tier
	• Select recovery options
	• Options like recovery options come with a cost
	• And then create

If you go to settings title on the left, under it you can see keys, secrets and certificates
Keys are where keys are stored
	• Here you can generate or import a key

Certificate
	• This is where you can generate a new certificate
	• Or you can import and store certs for other authentication

Access policies
	• Shows who has got access to your vaults
	• Or you can provide your other Azure services allow/disallow access
	• And for a user what sort of control you want to have for your key vault, what sort of key permissions control permissions certificate permissions etc
	• You can narrow down filter it out and give  a least privilege for a user to access your key vault as well

For our task, we are going to add a secret to the key vault
	1. Click on add secret
	2. In upload options select manual
	3. Give a name
	4. Provide a value
		○ You can keep your secret keys or passwords or things like that
	5. Leave the rest of the values as it is and click on create
	• Only the user who is allowed to use your vault will be able to do that and access this information
	• The allowed user can login to key vault and click on a secret and check the current version or the latest one 
 

Examine Microsoft Azure Security, Privacy, Compliance,
and Trust
Module 04: Azure Governance Methodologies

#39:Define Azure Policy

Azure Policy
	• Is a service in Azure that you can use to create assign and manage policies
	• These policies enforce different rules and effects over your resources, so those resources stay compliant with your corporate standards and standard SLAs
	• Azure policies does this by using policies and initiatives and run evaluation for your resources and scans for those non-compliant with the policies you have created
	• For example, if you have a policy to allow only a certain- skew size of virtual machines in your environment, once you implement this policy it evaluates resources when you create new ones or update existing one
	• It also evaluates your existing resources as well
	• Azure policy comes with a number of built in policies
	• You can pick any of these built in policies and initiate definition that you can use under categories such as storage, networking, compute, security center and monitoring
	• Azure policies can also integrate with your Azure DevOps by applying any continuous integration and delivery pipeline policies that apply to your pre-deployment and post deployment for your application

Azure resources can automatically remedy resources and configuration that are deemed non-compliant

There are three steps to creating and implementing an Azure policy
	1. Create a new policy definition
		○ A policy definition expresses what to evaluate and what actions to take
		○ For example, you could prevent a VM from being deployed if they are exposed to public IP address
		○ Every policy definition has containers under which it has been enforced. Things like allowed Skews, allowed resource types, allowed locations, allowed VM skills etc.
	2. Second step of implementing Azure policy is assigning definition to a scope of your resources
		○ To implement your policy definitions, you assign them to resources
		○ A policy assignment is a policy definition that has been assigned to take place within the specific scope. This specific scope can range from a management group to a resource group
		○ Policy assignments are inherited by all child resources. 
		○ You can exclude a sub-scope from a policy assignment
	3. Review the policy evaluation results
		○ When a condition is evaluated against your existing resources, it is marked compliant or non-compliant
		○ You can review the non-compliant policy results and take action that is needed

These policy initiatives work with Azure policies. The first one is initiate definition and second one is initiate assignments.
An initiate definition is a set of policy definition to help track your compliance state for a larger goal
Like a


#40: Walkthrough:
Create an Azure Policy
Microsoft Azure Fundamentals [Exam AZ-900] Full Course



We will create an Azure policy to restrict deployment of Azure resources to a specific location
Azure Portal > All Services > Azure Policy

Within the policy configurator, you can see all the policy that you have created

Based on the policy you would be able to see your overall compliance because once you apply these policies to a scope, a scope could be your resource group or it could be your subscription and then these policies are going to go and check the compliance of these or whatever the condition you put apply on top of your policy

	• If you go to the Definitions tab on the left, we can see the definitions already available in Azure Policy by default, you can filter these by types, categories etc
	• You can go and create your own definition as well

Lets see a particular Azure Policy, it is Azure virtual machine size SKUs will prevent anybody from creating any other virtual machine SKUs that the one which you mention in the template.
So the use case scenario for this is, you apply this on a particular resource group and give control to your particular team and they wont be able to create any other family or any other type of virtual machines apart from what you have mentioned before

The Assignments tab, here you can see all the assignments you have made within your subscription or you can create a new initiative or a new policy as well

We are gonna create a new policy,(click on Assign Policy in the Assignments tab) within the policy we have a scope, exclusions and the policy definition. Scope is nothing but where you gonna apply this policy, you can start with your subscription and then you can narrow it down by resource groups. If you don’t wanna apply to resource group you can leave it at the subscription level itself




Exclusions
Exclude any resource group or any other type of resources who doesn’t want to be part of this particular policy

Policy Definition
	• Thats where we go and add a new policy
	• You can also search in available policies

Here we use a policy called Allowed locations
This enables you to resctrict an operation within your organization who can specify when deploying your resources and you can use this to enforce your geography compliance resource as well
Sometimes the companies have some restrictions

Click parameters tab and choose the country of choice in allowed locations
We leave rest of the settings as it is for the walkthrough click on create

We create a storage account and test if policy works
Even though validation will be successful we shall not be able to create the policy

If you click on the error that you receive when the storage account cannot be successfully created in a location not specified in the policy, you see a pane on the right that shows that a plicy is apllied


Now we go to the policy and see if it is in compliance, when you click on the policy , it basically shows you if its compliant or not, compliance is nothing but it goes through the  whole resources to make sure that there is no other resources which Is outside of this boundary


We now go and delete the assignment of this policy/delete policy and create another storage account and check if it can be successful

Other scenarios where the Allowed Location policy can be useful
	• Things like cost tracking
		○ You can have different subscription for different regional locations and the policy can ensure that all resources are deployed in the intended region to help ccost tracking
	• Data residency and security compliance
		○ You can also have data residency requirements and create subscription per customer and specific workload and define that all resouces must be deployed in a particular database to ensure data and security compliance are met




Explore Role-based access control (RBAC)
	• RBAC provides a fine-grained access management for Azure resources, enabling you to grant users only the rights they need to perform their job
	• RBAC is provided at no additional cost to all Azure subscribers

RBAC Usage Scenarios
	• Allows one user to manage VMs in a subscription and another user to manage the virtual network
	• Allows database administrator group (DBA) manage  SQL databases in a subscription
	• Can allow a user to manage all resources in a resource group such as VMs, websites and subnets
	• Allows an application to access all resources in a resource group as well

Some of the best practices for RBAC are
	• You can segregate duties within your team and grant only the amount of access that is needed, instead of giving everybody unrestricted permission, only allow certain actions at a scope level
	• When planning your access control strategy grant users the lowest previlege levlel that they need to do their work

#42: Walkthrough:
Manage access with RBAC

Microsoft Azure Fundamentals [Exam AZ-900] Full Course



In this taks, we are going to assign some roles and we are gonna review some activity logs as well.

First we are gonna create a resource group to test this role assignment task
	• Go into resource group, select your subscription and choose a name for it and select a region and create
	• Go to the newly creatd RG
	• Once you are there, on the LHS, we can find Access Control(IAM), here we would have control to add assignments, deny assignments, administrators and roles ( all these are tabs within IAM)
		○ Lets explore Roles, click on Roles tab
		○ You can see there are lots of built in roles available within Azure by default, you can also crate a custom one. Most probably the one you are looking for should be built inn
		○ 
		
		Next to these roles there an information button that lets you know what sort of control you can assign when you assign somebody this particular role. Owner for example have full control
		Reader can only read and not change anytrhing etc
		
		If we go to the Role Assingments tab this is where you will be able to Add/Remove a user for particular role assignments. By default you can see who is the owner for subscripton. The owner will have 'owner' role assigned by default
		
		You can click on +Add to add role assignments, before assigning a role you need to know what role you are assigning to a user, in this we will go with a 'virtual machine contributor role' and leave the 'Assign Access to' - 'Azure AD user, group or service principle' that means all the eresources within your Azure and Azure AD. Under select field ypu type in the username or the email address of a user to assign a permission for that user for this resource group
		
		
		Now that you have successfully added a user on a particular role, you can ofcourse go back to the resource group and review that role assignments as well
		
		
	• You as a owner of the subscription or the RG will be always able to modify the role assignments
	• The whole idea of the role assignments is to give granular control to a particular user account
	• User account with Virtual Machine Contributor role will only be able to manage those resources that user will not be able to delete or assign a new user to that particular role

You as an owner can always go under the role assignments and delete or add a new role assignments as well

We shall go ahead and create another role assignments selecting 'Role' as 'Reader' and 'Assign Access to' - 'Azure AD user, group or service principle' and select a random user, here Summer Smith
This user will only have reader access to this particular resource group(highlighted in the pic below)


Summer as a user when visits the resource group section will only be able to see the resources in AZ-900-TEST-RG resource group where as Morty who has "Reader" access to the whole subscription will be able to see resources in other RGs in the subscription as well. 

If you go to a resource group and select 'Activity Log' under 'Overview' tab on the left pane, and click on 'Add Filter' and in first drop down select operation and in next drop down choose 'Create role assignment' you shall be able to see history of the selected operation type in that took place in the resource group


And you can go ahead and find out all other activity report within this activity log as well

Now we have learned how to assign roles and view the activity logs to find out who have done these changes

As always, after the walkthrough we should delete the unncessary resources





Module 04: Azure Governance Methodologies
#43: Define Resource Locks

	• Resource locks helps you prevent accidental deletion or modification of your Azure resources, you can manage these locks within the Azure portal

There are two types of locks
	1. Cannot delete
	2. Read only


Sometimes you may need to lock a subscription or a resource group or a resource to prevent other users in an organization from accidentally deleting or modifying critical resources

For that these two types of lock level can help you do that, cannot delete or read only

Cannot delete
	• Authorized admin can still delete and modify a resource but they cannot delete or update the resource

Apllying this lock is like restriciting all authorized users to the permissions granted by the reader role and when a resource lock is applied, you must first remove the lock in order to perform that acrtivity by putting an additional step in place, before allowing action to be taken on that resource, it helps protect that resource from any sort of other actions and helps protect your administrator from doing something they may not be intended to do

Resource locks apply regardless of other ____ permissions, even if you are owner of the resource, you must still remove the lock before you will actually be able to perform the blocked activity




#44: Walkthrough:
Manage Resource Locks

Create a resource group, add a lock to the resource group and test deletion, test deleting a resource in the resource group, and remove the resource lock
	1. Create a resource group
	2. Add a resource lock to prevent deletion of  a resource group
	3. Test deleting a member of the resource group
	4. Remove the resource lock

We start by creating a new resource groupk

In the resource group on the LHS, under settings, you can see the Locks tab
	• Click Add to create a new Lock
	• In Lock Type, choose from Delete or Read Only
		○ In this case we select Delete
This will prevent resources in this RG from being deleted or deletion of the RG itself



The only way to delete this RG, is by going into the RG, and Locks, modify the resource group or delete the Lock itself


	• Now we go ahead and create a new storage account in this RG and try to delete it but we would get the following error
	• 
So the only way to delete the RG or a resource in the RG is by deleting the Lock





Module 04: Azure Governance Methodologies
#45: Explore Azure Blueprints

Azure Blueprints
	• Azure blueprints enable cloud architects to define a repeatable set of Azure resources that implement and adhere to organization standards, patterns and requirements
	• Azure blueprints enables to development teams to rapidly build and deploy new environments
	• Is a declarative way to orchestrate the deployment of various resource templates and other artifacts such as role assignments, policy assignments, Azure resource manager templates and resource groups

The process of implementing an Azure Blueprint
	1. Create an Azure Blueprint
	2. Assign the Blueprint
	3. Track the blueprint assignments

With Azure Blueprint, the relationship between the Blueprint definition  and the Blueprint assignment is preserved
This connection support improved deployment tracking and auditing and Azure Blueprints are different from Azure resource manager templates
	• With Azure Resource Manager templates, you deploy resources, they have no active relationship with the deployed resources
	• By contrast with Azure Blueprint, each deployment is tied to an Azure Blueprint package this means that the relationship with the resources will be maintained even after deployment. 
	• Maintaining relationship in this way improves auditing and tracking capabilities



Define Subscription Governance
	• Azure subscriptions are discussed in many contexts, there are mainly three aspects to consider in relation to creating and managing subscriptions
	1. Billing 
		○ Reports can be generated by subscriptions, if you have multiple internal departments and need to do charge back, a possible scenario is to create subscription by department or project
	2. Access Control
		○ A subscription is a deployment boundary for an Azure resource and every subscription is associated with Azure AD tenant that provides administrators the ability to set up the Role Based Access Control or RBAC 
		○ When designing a subscription model, one should consider the deployment boundary factor, some customers have separate subscription for deployment and production, each one is isolated from each other from resource perspective are managed using RBAC
	3. Subscription Limits
		○ Subscriptions are also bound to some hard limitations, for example, the maximum number of express route circuit per subscription is 10
		○ Those limits should be considered during a design phase
		○ If there Is a need to go over those limits in particular scenarios then additional subscription may be needed,
		○  if you hit a hard limit there is no flexibility
	
Also available to assist with managing subscriptions are management groups which manage access policies and compliance across multiple Azure subscription



Module 05: Monitoring and reporting in Azure
#46 Explore Azure Tags

Why tagging is important?
What are the useful scenarios for tagging?

Tags
	• Provides metadata for your Azure resources
	• Logically organizes resources into a taxonomy
	• Each tag consists of a name and value pair
		○ For example you can apply the name, environment and the value production to all the resources in production 
		○ or tagged by company departments for example, the name of the departmnet and with the value of IT
	• After you apply tags, you can retrieve all these resources in your subscription with a  tag name and value
	• Tags enable you to retrieve related resources from different resource groups, this approach is helpful when you need to organize billing or management

Limitations of Tags
Some of the limitations of using tags are:
	• Not all resource types support tags
	• Each resource or resource group can have maximum of 50 tag values 
	• but storage account only supports 15 tags but the limit will be raised to 50 in the future release
	• Tag name is limited to 512 characters and tag value is limited to 256 characters
	• Tag applied to the resource group are not inherited by resources in the resource group





#47: Walkthrough:
Implement Resource Tagging

Create a policy assignment that requires tagging, create a storage account and test the tagging, view resources with a specific tag, and remove the tagging policy
	1. Create a policy assignment to require tagging
	• Go to Azure policy and find a policy called Require A policy called require tagging on resources, Modify policy and assign it to Azure subscription
			§ Click all services tab on left pane, search for policy, go to app
			§ Once we are inside Azure policy construct, we can see if there are any existing policies assigned to the subscription
			§ On the left pane in Policy, go to 'Assignments' tab ( we can see Definitions by clicking on tab with that name as well)
			§ Click on Assign Policy, here we can define a scope, scope is nothing but where you would like to assign this policy level to, is it on a subscription level or a resource group level. Here, we select the subscription, that is the scope of the policy is the whole subscription
			§ You get an option to exclude as well, if you are applying to a subscription level, you can exclude a resource group etc
			§ In policy definition field we search for "require a tag and its value on resources", not focusing on rest of the fields now
			§ We go to parameters, here we define the parameter for the tag name. for this particular policy we are gonna put a parameter as company
			§ We click on create, it will go through a validation process, after the validation, you can see that the policy is being created
			§ So now we have successfully created a policy with a  parameter called company and we have assigned to a subscription level
			§ This means that any new resource we create within this subscription need to have a tag which is called company, if it doesn’t have a tag assigned while you create a resouce within your Azure subscription, the whole process is going to fail
	2. Create a storage account to test required tagging
		○ Create storage account with default values and click on create, the validation process willl commplete without any error but when we try to create it, just before the deployment it should throw an error
		○ Now we go back to the storage account, create another storage account and add a tag in the Tags tab
			§ Name of the tag should be 'Company' and put in anything in the Value field
			§ When you click on Review+create, this is going to validate like last time and successfully create the storage account
			§ If you go to the storage account and click on Tags tab on the left pane within it,  we can see the Tag with name Company and the Value we entered in the last step
			
	3. View all resources with a specific tag
		○ We search for Tags in all services and go to Tags
		○ We can filter all the tags which is available within the Azure subscription
		○ This is another great place where we can allocate each resource on different tags
		○ This can be used for taxonomy purposes, this can be used for resource allocation and other sort og ranular control you want to have within your subscription
	4. Delete the policy assignment
	• We need to delete whatever we have created, especially while studying, so that it is not going to impact anything that you are going to learn next and anything within your production environment
	• We will now go to Policy > Assignments > Delete Assignment

Module 05: Monitoring and reporting in Azure
#48: Explore Azure Monitor

Azure Monitor
	• Maximized the availability and performance of your applications by delivering the comprehensive solutions for collecting, analyzing and acting on telemetry from your cloud and on-premises environment
	• It helps you understand how your applications are performing and proactively identifies issues affecting them and they resources they have dependent on
	• So what data does Azure want to collect?
		○ Azure monitor can collect data from variety of sources
		○ You can think of monitoring data for your apps in tiers ranging f

What does Azure Monitor collect?
	• Application monitoring data
		○ Data about the performance and functionality of the code you have written regardless of the platform
	• Guest OS monitoring
		○ Data about the OS that ypur app is running, this could be running in Azure, another cloud or on premises
	• Azure resource monitroing data
		○ This is the data about operation of an Azure resource
	• Azure subscription management data
		○ Data about subscription and management of an Azure subscriptiojn as well as data about heatlth and operation of Azure itself
	• Azure tenant monitoring data
		○ Data about operation of tenant level Azure services such as Azure Active Directory


Azure Service Health
	• Is a suite of experiences that provide personalized guidance  and support when issues with Azure services affect you
	• It can notify, help you understand the impact of the issues and keep you updated as the issue is resolved
	• Can also help you prepare for planned maintenance and changes that could affect the availability of your resources

Azure health is composed of the following three things
	1. Azure status
		○ Provides a global view of health data for Azure services
		○ Up to the minute information of service availability
		○ Everyone has access 
	2. Azure service health
		○ Provides a customizable dashboard that tracks the state of your Azure services in the regions where you use them
		○ In this dashboard you can track, active events such as ongoing service issues, upcoming plan maintenance or relevant health advisories
	3. Azure resource health
		○ Helps you diagnose and obtain support when an Azure issue affects your resources, it provides you details about current and past state of your resources
		○ Also provides technical support to help you mitigate problems 
		○ 
	together the Azure service health components provide you the comprehensive view of health status of  Azure services
	
Monitoring Apllications and services
.integrate Azure Monitor with other Azure services to improve your data monitoring capabilities and gain better insights into your operations

Azure Monitor features can be organized into four categories:
	• Analyze
		○ You analyze data for application insight, Azure monitor for containers, Azure Monitor for VMs
	• Respond
		○ You respond to these issues by looking into alerts and auto scale
	• Visualize
		○ Visualize the data using dashboards, views and power bi
	• Integrate
		○ You will often need to integrate Azure Monitor with other systems and build customized solutions that use  your monitoring data
		○ Oher Azure services can work with Azure Monitor to provide this integration

Examine Microsoft Azure Security, Privacy, Compliance,
and Trust
#49 Module 06:
Privacy, Compliance, and Data Protection Standards

Explore Azure Compliance Terms and Requirements
	• When selecting a cloud provider to host your solutions, you should understand how your provider can help you comply with regulations and standards, some questions to provide about the potential provider include
		a. How compliant is the cloud provider when it comes to handling sensitive data
		b. How complliant are the services offered by them
		c. How can I deploy my own cloud based solutions to scenarios that have accreditations and compliance requirements

Microsoft heavily invests in the development of robust  and innovative compliance process
Microsoft compliance framework for online services map their controls to multiple regulatory standards which enable Microsoft to design and build services using a common sense of control


With the following image you get a level of compliance offering from the following image



Identify Microsoft Privacy Statement
Provides openness and honesty about how Microsoft handles the user data
collected from its products and services.

	• It explains what personal data Microsoft processes
	• How Microsoft processes it
	• And for what purposes



Explore compliance manager
	• Assign,track and verify your compliance and assessment-related activities
	• Provides a score by evaluating your compliance status
	• Stores and manages your compliancy related actrifacts
Microsoft provides deatiled information to auditors and regulatores


Azure Government Services
	• Meets the security and compliance needs of US federal agencies, state and local governments, and their and their solution providers

Azure Government
	• Separate instance of Microsoft Azure Service
	• It addresses the security and compliance need of US federal agencies, state and local governments
	• Physically isolated from non-US governmetn deployments
	• Provides braodest complaince and level 5 department of defense or DOD apporval
	• You can choose from 6 only data center regions, including two regions granted a level 5 provisional authorization
	• Also offers the most compliant certification by any cloud provider

Azure China 21Vianet
	• Operated by 21Vianet
	• Is a physically seperated instance of cloud services, located in China
	• Prepared by 21Vianet
	
	

Azure services are based on the same Azure,Office 365, Office 365 and PowerBI technologies that make up the Microsoft global cloud service
Azure agreements and contracts in China where applicable are signed between customers and 21Vianet
As the first foreign cloud provider in china in compliance with chinese govt regulations

Examine Microsoft Azure Security, Privacy, Compliance,
and Trust
#50: Explore Trust Center
	• Is a website resource containing information and details about how Microsoft implements security, privacy, compliance and transparency in all Microsoft cloud products 

The Trust Center 
	• In-depth expert information
	• Curated lists of recommended resources, arranged by topic.
	• Includes information specific to each role, for example
	•  business managers, tenant admins, security teams, risk assessment and privacy officers and legal compliance teams


Service Trust Portal(STP)
	• Hosts the compliance manager service and is the Microsoft public site for publishing audit reports and other compliance related information related to Microsoft cloud services
	• In STP, users can download audit reports produces by external auditors and gain insights from Microsoft authorized report that provide details on how Microsoft build and operates its cloud services
	• STP also include information about how Microsoft online services can help your organization maintain and track compliance with standard laws and regulations such as ISO,SOC, GBPR etc.



#51: Walkthrough:

Explore the Service Trust Portal (STP)

Access the Trust Center, Service Trust Portal (ST P),
and Compliance Manager.

1. Access the Trust Center.
2. Access the Service Trust Portal.
3. Access the Compliance Manager.


Go to Microsoft.com/en-us/trust-center
Go to Microsoft Compliance Offering, notice how the offerings are grouped into global, US Government, Industry and Regional

Lets look at ISO 27001, it is a typical of the compliane information we provide, notice there is an overview of the  standard, in scope cloud services, audit reports and certificates, assessment, FAQ resources and whitepapers as well


We can access Service Trust Portal at servicetrust.microsoft.com
Here we have Audit reports for different types
You have an Audit report for ISO27001 here as ewll

Complaince Manager makes it easy to perform risk assessment for your Microsoft cloud services


Application Gateway
	• Also a type firewall that provides web application firewall capability

Network Security Group
	• Allows you to filter traffic to and from Azure resources in an Azure network
	• NSG can contain multiple inbound and outbound security rules that enable you to filter traffic to and from resources by source and destination IP address, ports and protocol


Azure Advanced threat protectio
	• Gives you behaviour intelligence on your existing resources on your Azure and on prem


Azure Security center
	• Gives you recommendations best practices for all of your resources from on prem and Azure

Azure Key Vault
	• Is a centralized cloud service for storing your application secrets
	• Keeps app secrets in a single central location
	• Provides secure access
	1. Store all your secrets and passwords

Azure Policy
	• Policies create and apply in a subscriptio level or a RG level

Azure Health Service
	• Gives you details about the health of all Azure services

Service Trust Portal
	• Public site for audit reports and other compliance 
	• STP users can download audit reports published by external auditors and gain insight from Microsoft author reports that provide reports on how Microsoft builds and operates its cloud services

Azure Policy can be used to enforce resource tagging, 


Azure Blueprint
	• Enables cloud architects to define a repeatable set of Azure resources that implement organizational requirements

Role Based Access Control (RBAC)
	• Grants users only the rights they need to perform their jobs

Azure ATP
	• A monitoring service that provides threat protection across all your services both in Azure, and on premises

Azure Information Protection
	• Is a cloud based solution that helps organizations classify and protect its documents and emails by applying labels. Labels can be applied automatically (by administrators who define rules and conditions), manually (by users), or with a combination of both (where users are guided by recommendations)

Good use of a resource lock
	• An express route circuit with connectivity back to your on-premises network

Azure Pricing, Service Level Agreements, and
Lifecycle
#53: Review Azure Subscriptions

	• Using Azure requires an Azure subscription which provides you with authenticated and authorized access to Azure accounts. Subscriptions can provide billing and access control boundaries
	• Allows you to provision resources
	• Is a logical unit of Azure services that links to an Azure account which is an identity in Azure AD or a directory that an Azure AD trusts
	• An Azure account can have one or multiple subscription and have different billing models and to which you apply different access management policies, 
	• you can use Azure subscription to define boundaries around your Azure products, services and resources


Taking it easy on Notes




There are three primary factors affecting costs:
Resource Type
Services
Location









Cost Management is an Azure product that provides
a set of tools for monitoring, allocating, and
optimizing your Azure costs.


Define Service Level Agreements (SLAs)
SLAS document the specific terms that define Azure performance standards.

• SLAS define Microsoft's commitment to an
Azure service or product.
• Individual SLAS are available for each Azure
product and service.
• SLAS also define what happens if a service or
product fails to meet the designated
availability commitments.






Preview versions have limitations , not suitable for productions


Availability Zones
Are data centers set up to be an isolation boundary from others in the region with their own power cooling and networking, if one zone in a region goes down other availavility zone in the region continue to work
![image](https://github.com/fayas1290/Learning-AZ900/assets/157561213/6bbb21d5-cf65-4d8f-b414-4f40cc442c5f)


