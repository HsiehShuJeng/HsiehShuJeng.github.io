# AWS Reinvent 2020
* [Computing](#computing) 
* [Containers](#containers)
* [AWS is changing the game for what customers can build](#aws-is-changing-the-game-for-what-customers-can-build)  
* [Storage](#storage)  
* [Database](#database) 
* [When all you have is a hammer, everything looks like a nail](#when-all-you-have-is-a-hammer-everything-looks-like-a-nail)  
* [Analytics](#analytics)  
* [ML/DL](#ml-dl)  
* [Customer Engagement](#customer-engagement)  
* [IoT](#iot)  
* [Hybrid](#hybrid)  
* [Ending](#ending)


## <a id="computing"></a>Computing

### <a id="EC2"></a>EC2

- brief

	- Fastest networking with P4d instances (400 Gbps)
	- Largest high memory instances for SAP (24TB)
	- Largest local storage instances with D3en (336TB)
	- Most powerful ML training instances with P4d
	- Most powerful ML inference instances with Inf1
	- Best price/performance for graphics-intensive workloads with G4ad
	- Only cloud provider with on-demand macos instances
	- Only cloud provider that supports Intel, AMD, and Arm processors

- Graviton 2

	- Instances powered by AWS Gravition2 Arm processors
	- 40% better price/performance for all workloads

		- R6g - General purpose
		- M6g - Memory optimized
		- C6g - Compute optimized
		- C6g with enhanced networking
		- T4g - Burstable

- Habana Gaudi-based Amazon EC2 instance

	- Available first half of 2021
	- Support for TensorFlow new Habana Gaudi processors from Intel
	- Up to 40% better price/performance over current GPU-based EC2 ML training instances
	- Support for TensorFlow and PyTorch

- AWS Trainium

	- Available in 2021
	- Our ML training chip custom designed by AWS to deliver the most cost-effective training in the cloud
	- Most teraflops of any ML instance in the cloud
	- Uses same Neuron SOK as Inferentia
	- Available as EC2 instances or in Amazon SageMaker

### Hundreds of thousands of customers use AWS Lambda

- brief

	- Build and run applications without managing servers
	- 1 millisecond billing lowers costs up to 70% (vs. 100 ms billing)
	- More native integrations and event sources by 7x (140)
	- Nearly half of new apps at Amazon* were deployed to AWS Lambda in 2020

- Lambda Container Support

	- Package code and dependencies as a Docker or Open Container Initiative containers
	- Use a consistent set of tools for compatible container image and Lambda-based applications
	- Deploy Lambda functions built on top of third-party base container images

## <a id="containers"></a>Containers

### the best place to run and manage containers

- Amazon EKS
- Amazon ECS
- Amazon Fargate

### the management challenge of moving containers to the cloud

- Amazon ECS Anywhere

	- COMING IN 2021
	- Same AWS-style ECS APIs, cluster management, workload scheduling, and monitoring
	- Works on any infrastructure
	- Seamless ECS experience across AWS and your on-premises infrastructure

- Amazon EKS Anywhere

	- COMING IN 2021
	- Same EKS experience to set up, upgrade, and operate on-premises Kubernetes clusters
	- Works on any infrastructure
	- Seamless EKS experience
	- Amazon EKS Distro across AWS and your on-premises infrastructure
	- Amazon EKS Distro open sourced

### The challenge of moving to smaller units of compute

- AWS Proton

	- The first fully managed deployment service for container and serverless applications
	- Building microservices with AWS Proton

		1. Define stack
		2. Publish stack
		3. Select stack
		4. Enter parameters
		5. Deploy microservice
		6. Update and maintain microservices

## <a id="aws-is-changing-the-game-for-what-customers-can-build"></a>AWS is changing the game for what customers can build

### instances

### containers

### serverless

### company case
SmugMug

- https://www.smugmug.com/

## <a id="storage"></a>storage

### Reinventing data stores

- More data is created every hour today than
in an entire year 20 years ago
- More data will be created in the next
3 years than in the prior 30 years combined

### block storage is foundational and on of the most pervasive forms of storage

- Amazon Elastic Block Store

	- gp3 volumes for EBS

		- Provision IOPS and throughput separately with next-generation SSD volumes (at a 20% lower price per GB)

	- io2 for even higher IOPS and throughput

- io2 Block Express

	- 4x the IOPS (up to 256,000), throughput (4,000MB/s). and storage capacity (64TB) of io2
	- Scale, provision, and pay for just the capacity you need
	- SAN performance without the headaches
	- More SAN features coming in 2021: Multi-Attach, I/O Fencing, Fast Snapshot Restore, and Elastic Volumes

## <a id="database"></a>database

### On-premises databases require a lot of undifferentiated heavy lifting

- prologue

	- Hardware and software installation
	- Configure, patch, and back up
	- Capacity planning and cluster scaling
	- Manage security and compliance

- Amazon Aurora

	- brief

		- MySQL and PostgreSQL compatible
		- Several times faster than standard MySQL and PostgreSQL
		- Highly available and durable
		- 1/10th the cost of commercial-grade databases

	- showcase of customers using Amazon Aurora

- Amazon Aurora Serverless

	- Automatically starts up, shuts down, and scales capacity up or down
	- No database instances to manage
	- Scales database capacity to meet demand within for Amazon Aurora 5 to 50 seconds

- Amazon Aurora Serverless V2

	- AVAILABLE IN PREVIEW TODAY
	- Scale to hundreds of thousands of transactions in a fraction of a second
	- some detail

		- Scale to hundreds of thousands of transactions fraction of a second
		- Scale capacity up and down in fine-grained increments for just the right amount the application requires
		- Save up to 90% vs. provisioning capacity for peak load
		- Multi-AZ support, Global Database, Read Replicas, Backtrack, and Parallel Query

### More than 350,000 databases migrated to AWS

- prologue

	- AWS Schema Conversion Tool (SCT) to migrate database schema
	- AWS Database Migration Service (DMS) to migrate data with minimal downtime

- Babelfish for Aurora PostgreSQL

	- AVAILABLE IN PREVIEW TODAY
	- Run SQL Server applications on Aurora PostgreSQL with little to no code changes
	- some detail

		- Stop paying for SQL Server licenses you don't need
		- New translation capability to easily run SQL Server applications on Aurora PostgreSQL
		- Understands SQL Server's proprietary dialect (T-SQL), and communications protocol (TDS)
		- Migrate the data with DMS, then update your application configuration to point to Aurora instead of SQL Server

- Babelfish for PostgreSQL

	- COMING IN 2021
	- OPEN SOURCE PROJECT
	- Uses the Apache 2.0 license
	- Makes the source code available to add new features
	- Available on GitHub in 2021

## <a id="when-all-you-have-is-a-hammer-everything-looks-like-a-nail"></a>When all you have is a hammer, everything looks like a nail

### The right tool for the right job

- RELATIONAL

	- Amazon RDS

		- AURORA

			- MySQL
			- PostgreSQL

		- COMMERCIAL

			- Oracle
			- Microsoft SQL Server

		- Commuity

			- PostgreSQL
			- MariDB

- KEY VALUE

	- Amazon DynamoDB

- IN-MEMORY STORE

	- Amazon ElasticCache

		- Memcached
		- Redis

- GRAPH

	- Amazon Neptune

- DOCUMENT

	- Amazon DocumentDB

		- with MongoDB compatibility

- TIME-SERIES

	- Amazon Timestream

- LEDGER

	- Amazon QLDB

- WIDE COLUMN

	- Keyspaces for Apache Cassandra

### purpose-built analytic stores optimized for particular use cases

- INTERACTICE QUERY

	- Amazon Athena

- BIG DATA PROCESSING

	- Amazon EMR

- OPERATIONAL ANALYTICS

	- Amazon Elastic Search

- REAL-TIME ANALYTICS

	- Amazon Kinesis

- DATA WAREHOUSING

	- Amazon Redshift

## <a id="analytics"></a>Analytics

### Data Movement

- Amazon Aurora
- Amazon DynamoDB
- Amazon SageMaker
- Amazon Redshift
- Amazon Elasticsearch Service
- Amazon EMR

### AWS Glue Elastic VIews

- AVAILABLE IN PREVIEW TODAY
- Easily build materialized views that automatically combine and replicate data across multiple data stores
- Easily combine and replicate data from different data stores with AWS Glue Elastic Views

	- source data stores

		- Aurora
		- RDS
		- DynamoDB

	- AWS GLUE ELASTIC VIEWS

		- Copies data from each source data store to a target data store
		- materialized views

			- automatically keeps the data in the target data store updated

	- target data stores

		- Redshift
		- Elasticsearch Service
		- S3
		- DynamoDB
		- Aurora
		- RDS

### company support
BOOM

- https://boomsupersonic.com/

- partners

	- Japan Airlines

- all-in with AWS

## <a id="ml-dl"></a>ML/DL

### company support
Intuit

- https://www.intuit.com/company/

### Framework used for new machine learning scientific publications

- 9 out of 10 machine learning practitioners use more than one framework
- 60% of machine learning practitioners use more than two frameworks

### # Ask 1
Need the right tools for expert ML practitioners

- ML Frameworks & Infrastructure

	- Tensorflow
	- mxnet
	- PyTorch
	- Gluon
	- Keras
	- scikit-learn
	- DeepGraphLibrary
	- resources

		- Deep Learning & AMIs & containers
		- GPU and CPUs
		- Elastic Inference
		- Inferentia
		- FGPA

### # Ask 2
Tools for everyday developers and data scientists

- Ground Truth data labeling
- ML Marketplace
- SageMaker Studio IDE

	- Built-in algorithms
	- SageMaker Notebooks
	- SageMaker Experiments
	- Model Training
	- SageMaker Debugger
	- Model hosting
	- SageMaker Model Monitor
	- SageMaker Data Wrangler
	- SageMaker Feature Store
	- SageMaker Pipelines

- Sage Neo
- Rapid pace of innovation with Amazon SageMaker

	- showcase of customers using Amazon SageMaker

		- 50+ capabilities added since last year

	- SageMaker Studio

		- SageMaker Notebooks
		- SageMaker Debugger

			- Debug and profile model training

		- SageMaker Experiments

			- Organize, track and compare ML trainings

		- SageMaker Model Monitor

			- Automatically detect concept drift

		- SageMaker Autopilot

			- AutoML with full control and visibility

- Data preparation of machine learning is hard

	- prologue

		- Write queries and code to download raw data from data stores
		- Figure out and prototype the conversions, transformations, and feature combinations
		- Transform the data, spin up infrastructure to run code, monitor, manage for each change, validate, and save the results
		- Make sure it all works - data point by data point and fix any errors, outliers, or missing data points

	- Amazon SageMaker Data Wrangler

		- GENERALLY AVAILABLE TODAY
		- The fastest way to prepare data for ML
		- Aggregate and prepare ML features with SageMaker Data Wrangler

			- Imports and inspects data to identify the data types
			- Recommends transformations based on the data in the dataset
			- Applies transformations to features - can see a preview in real time
			- Checks to ensure the data is valid and balanced

- Storing, saving, and reusing ML features is hard

	- prologue

		- Need to be able to maintain variations and combinations of features for many different models
		- Need to share features across multiple places
		- Need to be made available for inference in real time
		- Need to ensure consistency of features for both training and inference

	- Amazon SageMaker Feature Store

		- brief

			- GENERALLY AVAILABLE TODAY
			- A new repository that makes it easy to store, update, and share ML features

	- Amazon SageMaker Pipelines

		- brief

			- GENERALLY AVAILABLE TODAY
			- The first purpose-built, easy-to-use CI/CD service for ML

		- Amazon SageMaker Pipelines - Data workflows for ML

			- Define each step of your end-to-end ML workflow
			- Pre-configure customizable workflow templates
			- Logs each step in SageMaker Experiments
			- Workflows can be shared and reused

### # Ask 3
ML for those who don't want to build 

- AI Services

	- VISION

		- Amazon Rekognition

	- SPEECH

		- Amazon Polly
		- Amazon Transcribe + Medical

	- TEXT

		- Amazon Translate
		- Amazon Comprehend + Medical
		- Amazon Textract

	- SEARCH CHATBOTS

		- Amazon Kendra
		- Amazon Lex

	- PERSONALIZATION

		- Amazon Personalize

	- FORCASTING

		- Amazon Forecast

	- FRAUD

		- Amazon Fraud Detector

	- DEVELOPMENT

		- Amazon CodeGuru

- Amazon CodeGuru

	- CodeGuru Reviewer provides automated code reviews for Java
	- And now for Python
	- CodeGuru Profiler identifies the most expensive lines of code
	- CodeGuru Security Detector provides real-time alerts when developing code that may not be secure

- Amazon DevOps Guru

	- brief

		- AVAILABLE IN PREVIEW TODAY
		- A new service that uses ML to identify operational issue ng before they impact customer

	- Automatically detect operational issues and recommend actions with Amazon DevOps Guru

		- Under-provisioned compute capacity
		- Database I/O overutilization
		- Memory leaks
		- Missing or misconfigured alarms
		- Early warning of approaching resource limits
		- Code and config changes that may cause outages

### # Ask 4
Not having to figure out how to put pieces together

- reinventing business intelligence
- Amazon QuickSight

	- Scale to tens of thousands of users without any infrastructure management or capacity planning
	- Easy to embed dashboards in applications
	- Pay-per-session pricing
	- Automatically generates summaries of dashboards in plain language

- Amazon QuickSight Q

	- brief

		- AVAILABLE IN PREVIEW
		- Ask Q any question in natural language and get answers in seconds

	- some detail

		- Enter business questions in search bar
		- Uses NLP to understand domain-specific business language
		- Automatically generates data models that understand meanings and relationships of data
		- Not limited to asking a specific set of questions

### showcase of customers using AWS  for ML

- company support
Fox

	- https://www.foxcorporation.com/

## <a id="customer-engagement"></a>Customer Engagement

### The challenges of traditional contact centers

### Amazon Connect

- brief

	- Built from the ground up with the cloud and Al/ML in mind
	- Set up and configure a contact center in minutes
	- Easy to use and configure for non-technical users
	- Scale from tens to tens of thousands of agents
	- Save up to 80% over traditional contact center solutions
	- No infrastructure to deploy or manage

- showcase of customers using Amazon Connect
- Agents need the right info at the right time

	- prologue

		- How can we get the right data about products or services provided to agents when a customer is inquiring?
		- How can we get data on a customer's related activity and experiences?

	- Amazon Connect Wisdom

		- brief

			- AVAILABLE IN PREVIEW TODAY
			- A new capability that uses machine learning to deliver agents the product and service information they need to solve issues in real time

		- Connect Wisdom reduces the time agents spend finding answers for customers

	- Amazon Connect Customer Profiles

		- brief

			- GENERALLY AVAILABLE TODAY
			- Gives agents a unified profile of each cu mer to provide more personalized service durir call

		- Connect Customer Profiles enables agents to deliver faster, more personalized customer service

- We want to identify and react to customer issues in real time

	- prologue

		- Can you make it easier to understand and react to customer contacts that are going sideways. and do so in real time?

	- Contact Lens for Amazon Connect

		- Activate Contact Lens with a single click in Connect
		- Automatically transcribe and analyze customer calls
		- Get full text transcription with speaker detection
		- Analyze sentiment, long periods of silence, and times when an agent and customer are talking over each other
		- Search all transcriptions for keywords, phrases, and analysis criteria

	- Real-Time Contact Lens for Amazon Conect

		- brief

			- GENERALLEY AVAILABLE TODAY
			- Identifies issues in real time to impact customer interactions during the call itself

		- Real-Time Contact Lens uses machine learning to detect customer experience issues during live calls

- Help us optimize customer service agent's time

	- prologue

		- How can we help agents manage their time outside of calls?
		- How can we optimize agents' time on the phone?

	- Amazon Connect Tasks

		- brief

			- GENERALLY AVAILABLE TODAY
			- Automates, trado, and manages tasks for contact center agents

		- Connet Tasks makes follow-up tasks easier for agents and enables managers to automate some tasks entirely

	- Amazon Connect Voice ID

		- brief

			- AVAILABLE IN PREVIEW TODAY
			- Real-time caller authentication using ML-powered voice analysis

		- Connect Voice ID provides real-time caller authentication without disrupting natural conversation

## <a id="iot"></a>IoT

### what industries are being reinvented? 

- reinventing automotive

	- RIVIAN

	- BMW GROUP

	- ly

	- LyA

	- BlackBerry

	- VOLKSWAGEN

- reinventing healthcare
- reinventing media and entertainment
- reinventing manufacturing

### company support
Carrier

- https://www.corporate.carrier.com/

	- cooling tracks
	- track shippment

### data is the connective tissue for industrial processes

### improving industrial processes

- #1 machine data

	- use machine data to predict when 
	- Amazon Monitron

		- brief

			- GENERALLY AVAILABLE TODAY
			- End-to-end solution for equipment monitoring

		- End-to-end equipment monitoring system to enable predictive maintenance

	- Amazon Lookout for Equipment

		- brief

			- AVAILABLE IN PREVIEW TODAY
			- Anomaly detection service for industrial machinery

		- some detail

			- Sends sensor data to AWS to build a ML model
			- Pulls data from machine operations systems, such as OSISoft
			- Learns normal patterns and creates a model
			- Uses real-time data to identify early warning signs that could lead to machine failures

- #2 computer vision

	- Amazon Panorama Appliance

		- brief

			- AVAILABLE IN PREVIEW DAY
			- A new hardware appliance that allows organizations to add computer vision to existing on-premises cameras

		- some detail

			- Plug in appliance, connects to network, and starts to identify video streams from existing cameras
			- Pre-built computer vision models in manufacturing, retail, construction, and other industries
			- Can also build models in SageMaker and deploy to Panorama
			- Integrates with AWS loT services, including SiteWise, to send data for broader analysis

	- Amazon Panorama SDK

		- AVAILABLE IN PREVIEW TODAY
		- some detail

			- Provides camera manufacturers with an SDK and APIs to create cameras to run CV models at the edge
			- Chips designed for CV and deep learning from Nvidia and Ambarella
			- Panorama-compatible cameras work out of the box with AWS ML services
			- Build and train models in SageMaker and deploy to cameras with a single click

## <a id="hybrid"></a>hybrid

### company support
Riot Games

- https://www.riotgames.com/en

- "With Outposts, AWS gave us a unique solution to ensure a level playing field for our players and streamlined our deployments using the same tools and APIs on-premises and in the cloud."
ZACH BLITZ, HEAD OF INFRASTRUCE

### What is hybrid?

- early confusion
- so, really, what is hybrid?

### when trying to move workloads from on-premises to cloud

- how do I get AWS on-premises as I'm transitioning and for workloads that must remain on-presmises
- AWS Outposts

	- AWS servers with AWS compute, storage, database, and analytics services
	- Fully managed and supported by AWS
	- Same hardware that AWS runs in its data centers
	- Same APIs, same control plane, same tools, and same functionality

- AWS Outposts in two new sizes

	- brief

		- COMING IN 2021
		- Smaller Outposts to run AWS infrastructure in locations with less space

### Amazon Local Zones

- Extension of an AWS Region
- Deliver single-digit millisecond latency to local end users
- Launched in Los Angeles in 2019
- Now available in Boston, Houston, and Miami (Preview)
- 12 more Local Zones coming in 2021: Atlanta, Chicago, Dallas, Denver, Kansas City, Las Vegas, Minneapolis, New York, Philadelphia, Phoenix, Portland, and Seattle

### AWS Snow Family

- Portable, rugged, secure devices designed for local data collection and processing in remote locations with little or no connection

### on-premises at 5G Edge

- AWS Wavelength

	- Build applications that serve mobile end users with ultra-low latency
	- Same AWS APIs, tools, and functionality
	- Deploy 5G applications globally
	- Currently available with Verizon in eight US cities
	- KDDI in Tokyo and SK Telecom in Daejeon
	- Vodafone in London

### so, what's hybrid

- ON-PRESMISES AT AVAILABILITY
- 5G NETWORKS
- MAJOR METROS
- RUGGED EDGE

## <a id="ending"></a>ending

### I wish I could Google my ending...someone give me reassurance, answers, anything will do.  

![](new_background.jpg)

