---
title: "Databases"
datePublished: Tue Mar 28 2023 16:40:44 GMT+0000 (Coordinated Universal Time)
cuid: clfshidkk000f0ajk9s2mh64z
slug: databases
tags: aws, dynamodb, databases, redshift, aws-rds

---

If you are from a non-technical background, And still want to know what is databases, Please don't worry guys, I will make you understand what are databases with **Images** and will see what all database services are provided by AWS.

Let's begin...

What are **DATABASES**?

*A database is an organized collection of structured information, or data, typically stored electronically in a computer system.*

Here we learned about EBS, want to read detailed blog--&gt; visit [https://nidhidevops.hashnode.dev/elastic-block-storage-amazon-machine-image](https://nidhidevops.hashnode.dev/elastic-block-storage-amazon-machine-image)

Also learned about S3 👇👇

[https://nidhidevops.hashnode.dev/amazon-simple-storage-service-amazon-s3](https://nidhidevops.hashnode.dev/amazon-simple-storage-service-amazon-s3)

Above mentioned articles are for Storage only, So why there is a need for Databases???

The answer is Because S3, EBS and EC2 instance stores can have limits. Apart from this one wants structured data or define relations. You can use Databases😍😍 Easy right?

## Relational databases

As the name suggests, The work is also in the same way 👌

A relational database is ***a type of database that stores and provides access to data points that are related to one another***.

More simply, The different tables are connected with a common point.

See the image 👉👉👇👇

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678814750543/e485c061-b7d9-4813-bb5d-e5e9fdcbda4f.png align="center")

Now let's move to the next one

### **NoSQL Databases**

NoSQL--&gt; no SQL--&gt; no relation

NoSQL has flexible Schemas and they are purpose-built for modern applications

For NoSQL, you can use JSON Schemas

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678901314854/04675701-f76a-444d-8dfc-ccd1180627e5.png align="center")

Guys, Get ready to learn Amazon RDS. 👇🙌

## Amazon Relational Database

* It's a managed DB service and uses SQL as a query language
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678901875513/51b6016f-5ccd-47bc-9d05-e3bd9d019c67.png align="center")
    

Above image displays how Amazon RDS works 👆👆

* In the above image, 7 RDS engines are  [Amazon Aurora with MySQL compatibility](https://aws.amazon.com/rds/aurora/?pg=ln&sec=hiw), [Amazon Aurora with PostgreSQL compatibility](https://aws.amazon.com/rds/aurora/?pg=ln&sec=hiw), [MySQL](https://aws.amazon.com/rds/mysql/?pg=ln&sec=hiw), [MariaDB](https://aws.amazon.com/rds/mariadb/?pg=ln&sec=hiw), [PostgreSQL](https://aws.amazon.com/rds/postgresql/?pg=ln&sec=hiw), [Oracle](https://aws.amazon.com/rds/oracle/?pg=ln&sec=hiw), and [SQL Server](https://aws.amazon.com/rds/sqlserver/?pg=ln&sec=hiw). Other steps are self-understood.
    
* This means that the code, applications, and tools you already use today with your existing databases should work seamlessly with Amazon RDS.
    
* With RDS, you don't need to worry about the underlying infrastructure, such as hardware provisioning, software patching, or database backups. Instead, AWS takes care of all of that for you, so you can focus on building your applications.
    

Hope you understood Amazon RDS

Let's move to the next one

## AMAZON Aurora

* [Amazon Aurora](https://aws.amazon.com/rds/aurora/) is a modern [relational database](https://aws.amazon.com/relational-database/) service.
    
* Unlike AWS RDS it is only MySQL and PostgreSQL-compatible.
    
* It provides built-in security, continuous backups, and serverless computing.
    
* And up to 15 read replicas, automated multi-Region replication, and integrations with other AWS services.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678903821980/ddf890ae-87b4-4089-b00f-4a6c999b08b9.png align="center")

Above image makes AA(Amazon Aurora 😁) easy to understand.

Guys Theory is not at all enough in AWS you have to go through the practical sessions as well.(Knowlege is good but implemention of that knowledge is way more important)

So Now we will look through RDS practically

Let's get started guys, Excited😍

## RDS HANDS-ON

* Type RDS in the search of the console
    
* Click Databases
    
* Click Create database
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678985657723/98b0dac2-37c8-423c-a88a-98b3997c8ebd.png align="center")

* Choose Standard create (Because You set all of the configuration options)
    
* Choose MySQL
    
* Choose MYSQL Community
    
* Choose Engine version according to you, I will choose the default one
    
* Choose Template as Free Tier
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678985886862/b42e1662-cb5f-4432-9b3d-9cc1bf5ad595.png align="center")

* Keep DB instance identifier as the default one
    
* Write master username as admin
    
* Also, write the master password as per the guidelines.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678986518993/c89693d3-f02c-4ac7-aa55-76ecf72f37cb.png align="center")
    
    Keep the storage type section as default.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678988319009/b3c33922-7ef7-431a-bd11-9f0fb3d5ba47.png align="center")
    
* In the connectivity, section Choose public access as YES
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678988372730/33f0a98c-40c8-4cdb-b7aa-2c5b3ffeaa4c.png align="center")

* Create a new security group as demo-database-rds
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678988558618/12c65159-e504-4a22-8c1e-6c70818b0246.png align="center")
    
    Choose the database Authentication option as Password Authentication
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678988792475/c3832540-7702-40c1-afa7-125fa6f218d9.png align="center")

* And left everything as it is
    
* Click Create Database
    

Note:- It will take around 2-3 minutes to create a database.

* click on the database you created, You will see all the things one needs to see.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678989418764/6bf29073-8640-45d7-b04d-71d720270dde.png align="center")

* one can take <mark>snapshot of databases</mark> as well(In easy language snapshots are backups)
    
* Click Actions--&gt;click take snapshots
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678989678916/c50b8ffe-a1a4-4a32-944d-6eb4dddb0ab0.png align="center")
    
    Click Take snapshot after writing the snapshot name
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678989635180/254017e0-e166-4f84-a134-f9b7d0a5b23c.png align="center")
    
    Go to the newly created snapshot, and see if the status is available.
    
* Under Actions, if you click restore the snapshot, it will help you to create a new database, a bigger database, or a copy of the database(Isn't this amazing😁)
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678990169889/9b797d1f-fdc1-41bc-a324-e01766c02eb7.png align="center")

Let's move to the next Amazing thing, Read this carefully👇👇

## Amazon ElastiCache

Yes, Guys Let's see what's amazing in this🤔

What is Cache?

A cache is a hardware or software component that stores data so that future requests for that data can be served faster; the data stored in a cache might be the result of an earlier computation or a copy of data stored elsewhere.

Now Read the below about the ElasticCache, everything will get clear

* Amazon ElastiCache is a fully managed, Redis- and Memcached-compatible service.
    
* That means it's a caching service built to deliver real-time performance for real-time applications.
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679160719128/ef8993f4-d39e-4783-a703-6d5a976bb4c1.png align="center")
    
    It reduces the load from databases for intensive workloads.
    

Guys Let's meet with the database which is very heavy when we say its name. It is 👇

(Just Kidding)

## DynamoDB

* DynamoDB is a fast and flexible <mark>nonrelational database(NoSQL) service</mark> for any scale.
    
* Its flexible data model and reliable performance make DynamoDB a great fit for mobile, web, gaming, advertising technology, Internet of Things, and other applications.
    
* <mark>Single-digit millisecond latency</mark>
    
* DynamoDB offers built-in security, continuous backups, automated multi-Region replication, in-memory caching, and data import and export tools.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680019158892/3b8f17cc-7bcf-46ee-86a2-06f31819cdf3.png align="center")

Let's read the Use cases which will make us Understand this better

**Applications with large amounts of data and strict latency requirements**. As your amount of data scales, JOINs and advanced SQL operations can slow down your queries. With DynamoDB, your queries have predictable latency up to any size, including over 100 TBs!

**Serverless applications using AWS Lambda**. [AWS Lambda](https://aws.amazon.com/lambda/) provides auto-scaling, stateless, ephemeral compute in response to event triggers. DynamoDB is accessible via an HTTP API and performs authentication & authorization via IAM roles, making it a perfect fit for building Serverless applications.

**Data sets with simple, known access patterns**. If you're generating recommendations and serving them to users, DynamoDB's simple key-value access patterns make it a fast, reliable choice.

Above we have learned about in-memory cache, right?

In the same way, we have a dedicated in-memory Cache for DyamoDB that is

### DynamoDB Accelerator - DAX

Amazon DynamoDB Accelerator (DAX) is a fully managed, highly available, in-memory cache for Amazon DynamoDB that delivers up to a 10 times performance improvement—from milliseconds to microseconds—even at millions of requests per second.

DAX does all the heavy lifting required to add in-memory acceleration to your DynamoDB tables, without requiring developers to manage cache invalidation

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679332116901/4c75b5fa-51f6-4972-a40c-6f3966635033.png align="center")

**<mark>DAX is only used for DynamoDB</mark>**

Now Let's move to **Redshift** 👇👇👇

## AWS REDSHIFT

* An Amazon Redshift data warehouse is an enterprise-class relational database query and management system.
    
* Amazon Redshift achieves efficient storage and optimum query performance through a combination of massively parallel processing, columnar data storage, and very efficient, targeted data compression encoding schemes.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680019113951/0a9fa10c-7352-4b1f-a5e3-1f7063086cd0.png align="center")

### Traditional databases VS REDSHIFT

Data Warehousing is the process of storing and analyzing data from multiple sources to provide meaningful business insights. It involves transforming the data from multiple sources into a common format for both storage and analysis. This process is generally known as **ETL** or **Extract, Load,** and **Transform**. Data Warehouses like Amazon Redshift leverage this process to cater to their customers.

Next is AMAZON EMR😊😊

## AMAZON EMR

EMR is Elastic MapReduce

\--&gt; Amazon EMR is the industry-leading cloud big data solution for petabyte-scale data processing, interactive analytics, and machine learning using open-source frameworks such as Apache Spark, Apache Hive, and Presto.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1679333377625/abc9895d-7676-4da1-9b50-541d94b29cc0.png align="center")

## **AMAZON ATHENA**

* It's a serverless service to analyze data that is stored in Amazon S3 using Python or standard SQL.
    
* You don’t even need to load your data into Athena; it works directly with data stored in Amazon S3.
    

Below is the picture which clearly explains Amazon Athena, Have a look 👇👇🙌

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680014546180/25eee315-8290-45c4-9ce5-75fb8b005ff5.png align="center")

### How to get started with Athena?

To start with Athena, log in to the AWS Management Console for Athena and create your schema by writing Data Definition Language (DDL) statements on the console or using a create table wizard. You can then start querying data using a built-in query editor. Athena queries data directly from S3, so there’s no loading required.

## Amazon QuickSight

Guys with this you can create interactive dashboards, But How?? 👇👇

* Amazon QuickSight is a fully managed cloud-scale business intelligence service that is powered by machine learning and allows you to create data visualizations and dashboards for the people you work with, wherever they are.
    
* AWS QuickSight allows you to connect your data from many different data sources.
    
* It also provides user-management tools to scale from just a few users to tens of thousands of users — all of this with no infrastructure to deploy and manage yourself. 
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680017141960/6e867ade-d9c5-4a21-bec1-fbff7f363c9e.png align="center")

##   
DocumentDB

Amazon DocumentDB (with MongoDB compatibility) --&gt; we can remember DocumentDB by this😁

* It's a fast, scalable, highly available, and fully managed enterprise document database service that supports native JSON workloads.
    
* As a document database, Amazon DocumentDB makes it easy to store, query, and index JSON data.
    
* The storage and computing are decoupled, allowing each to scale independently.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680019015219/30df7813-9a66-4ea3-8b1c-916d6f490c48.png align="center")

## AMAZON NEPTUNE

* Amazon Neptune is a fully managed database service built for the cloud that makes it easier to build and run graph applications.
    
* Neptune provides built-in security, continuous backups, serverless computing, and integrations with other AWS services.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680019342721/711fa20a-4f6f-4489-8e3e-0bfd48d74914.png align="center")

##   
Amazon QLDB

**Amazon Quantum Ledger Database (QLDB)**

* Amazon Quantum Ledger Database (QLDB) is a fully managed ledger database that provides a transparent, immutable, and cryptographically verifiable transaction log.
    
* Use cases are:- **Storing financial transactions, Reconciling supply chain systems, Maintaining claims history & centralizing digital records**
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680019551709/cb9d8571-9d1a-4f8e-a570-ebcca419c24a.png align="center")

## Amazon Managed Blockchain

* Amazon Managed Blockchain is a fully managed service that allows you to join public networks or set up and manage scalable private networks using popular open-source frameworks.
    
* **Blockchain makes it possible to build applications where multiple parties can execute transactions without the need for a trusted, central authority.** 
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680020492515/764b39b4-77aa-4e38-a591-92ac41f15fd8.png align="center")

##   
AWS Glue

* AWS Glue is a serverless data integration service that makes it easier to discover, prepare, move, and integrate data from multiple sources for analytics, machine learning (ML), and application development.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680020635496/b8c04274-1661-4095-a87c-2d09e96e930b.png align="center")

Last But Not Least, Let's move to our final topic DMS👇😊

##   
DMS – Database Migration Service

* AWS Database Migration Service (AWS DMS) is a managed migration and replication service that helps move your database and analytics workloads to AWS quickly, securely, and with minimal downtime and zero data loss.
    
* AWS DMS supports migration between the 20-plus database and analytics engines.
    

**HETEROGENEOUS MIGRATIONS**

Ex:- Microsoft SQL Service to Aurora

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680020891194/ae857bbe-aefb-4d5f-8077-63090c920853.png align="center")

**HOMOGENEOUS MIGRATIONS**

Ex:- Oracle to Oracle

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680020969724/225a8b2b-fc63-4094-95b2-d7308228f34a.png align="center")

Guys I literally enjoyed writing this Blog, I put my best to make you all understand DATABASES using images😍.

Hope you all will like it. I wrote the Longest blog ever. ⛄⛄

To the Best of my knowledge, I have covered all the databases. But still, if you find anything you don't understand, Please let me know in the comment section👇👇

If You want to read my blogs on AWS and want to understand the basics of the cloud please visit 👇👇

[https://nidhidevops.hashnode.dev/](https://nidhidevops.hashnode.dev/)

All suggestions are Welcomed!!