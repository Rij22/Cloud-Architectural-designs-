# Project_101
This repo contains an AWS architectural design of Project_101 i have worked on.

The diagram here shows a three tier Architecture of Chuncher’s Mobalysis platform. With require, a completely new solution that automates bug fixes and updates of the platform.
They needed a solution which reduces the RTO time when there is down time to improve reliability and highly available solution that can withstand traffic surges and finally they needed a metric that monitors their system which will allow them know exactly what is going on with resources of the application anytime there are changes.
    
    First to automate the entire process of building, testing and deploying we will be using AWS code pipeline for that task. We will assume that the source code is in the company’s GitHub repository. All we need is to push the code and code pipeline will automate the process. This will ensure rapid delivery and reliable features and updates.
   
   CLOUDFORMATION: - cloud formation will allow us model, provision and manage all of the AWS resources by using infrastructure as a code. It provisions our resources quickly, consistently and also manages them throughout their lifecycle. We can use a cloud template or we can use a template to create, update and delete stacks we don’t need. In the diagram, a Cloud Formation template was used to create all of the resources provisioned therein. The template will consist of the following resources;
1)Route 53
2)WAF
3)service
4)Application servers
5)Database servers
6)Event streams
7)Interactive tools
8)Streaming ingestion CDN
9)ELB
10)S3 Bucket
11)Web 
12)Metrics and Notification
13)Security groups


ROUTE 53: this provides DNS services to simplify our domain management.

WAF&SECURITY GROUPS: they move security to the instances to provide a stateful, host-level firewall for both the web servers and application servers.

CDN: Cloud distribution network for cloud front reaches viewers across the globe in millisecond with built-in-data compression, edge complete capabilities and field level encryption. It will start our streams quickly, play them with consistency and deliver high quality video to any device with media service. It will scale automatically to deliver our game patches and updates at scale with high transfer rates.

ELB: this will help to spread load across our availability zones at auto scaling groups for reduced redundancy and decoupling of the services we are using.

S3 BUCKET: this is provisioned for our static storage and backups, which enables simple HTTP-based object storage like images and videos in the game to be easily accessible. It also back’s up streaming data for analytics. 

WEB SERVERS AND APPLICATION SERVERS: they are the compute resources for the backend and frontend application of the Mobalysis. 

DATABASE SERVER: here we choose DynamodDB database due to the nature of the types of data provided by the game application. It is a fully managed NoSQL service designed to run high performance application at any scale. It will provide built- in security, continuous backups, automate multi-region replication, in-memory caching and data export tools for our software. It will build out our game platform with player data, session history and leader boards for millions of concurrent users.

EVENT STREAMS: kinesis data streams will store and ingest our streaming data in real-time. It has a low latency feature and automatically scales.

ITERACTIVE TOOLS: these tools will make it easy to analyse the data in S3 using standard SQL. It will provide the use of simple ETL jobs to prepare our data for analysis. Powered by machine learning, QuickSight allows everyone in the team to understand the data by asking questions in natural languages, exploring through interactive dashboards, and automatically looking for patterns and outliers.

METRIC AND NOTIFICATION: CloudWatch will monitor and observe our applications, respond to system-wide performance changes, and optimize the use of our resources. It will collect the application data in a form of logs metric and events. This will enable the company to see any changes and review before a customer complains. SNS is a messaging service for both application-to application and application-to-person communicating. SNS can fan out events as they happen in our game application account. It will also enable us to send notifications directly to users through sms text and email. 
The Architecture has been designed to be highly available, scalable, secure, cost effective, reliable and automative.

     


