---
title: "Amazon Ec2"
datePublished: Fri Nov 25 2022 14:54:48 GMT+0000 (Coordinated Universal Time)
cuid: clawmkd8z000k08mo4pl7adme
slug: amazon-ec2
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1668180570953/aLoJjKuFV.png
tags: aws, elb, aws-ec2, autoscaling, securitygroups

---

Hi, All of you,
Once Again welcome to my blog :-)

hmm, I hope everyone somewhere has listened to this term and if not, Don't worry we will cover this from the beginning :-)

First of all, let's complete the Full form of EC2, Its **Elastic Compute Cloud.**

### **Amazon Elastic Compute Cloud **

Let's see what's Amazon Technical definition is
Amazon Elastic Compute Cloud (Amazon EC2) is a web service that provides resizable compute capacity in the cloud. 

Let  me tell you in one statement

**AMAZON EC2 are VIRTUAL SERVERS IN CLOUD**

Easy, Right?

Let's see the difference between servers and virtual servers..

What are servers?
 A server is a software or hardware device that accepts and responds to requests made over a network.

What are virtual Servers?
A virtual server re-creates the functionality of a dedicated physical server.

Let me show you How EC2 Dashboard looks like ↓ 



![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1668182532506/9R_G7MtKY.png align="left")


What can I do with Amazon EC2?


- Amazon EC2’s simple web service interface allows you to obtain and configure capacity with minimal friction. It provides you with complete control of your computing resources and lets you run on Amazon’s proven computing environment. 

- Amazon EC2 reduces the time required to obtain and boot new server instances to minutes, allowing you to quickly scale capacity, both up and down, as your computing requirements change. Amazon EC2 changes the economics of computing by allowing you to pay only for capacity that you actually use.

On the EC2 dashboard we can see on the left side Security Groups, Elastic Load Balancer & Autoscaling Groups.

Let's learn about these and see how they are connected


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1669384006367/GPiNsiVSI.png align="left")

**NOTE**:-We will read only briefly about SG, ELB, and ASG. I will write dedicated blogs on these.

**Security Groups** -->
A security group acts as a virtual firewall for your EC2 instances to control incoming and outgoing traffic. Inbound rules control the incoming traffic to your instance, and outbound rules control the outgoing traffic from your instance.

**Elastic Load Balancer** -->
Elastic Load Balancing automatically distributes your incoming traffic across multiple targets, such as EC2 instances, containers, and IP addresses, in one or more Availability Zones. It monitors the health of its registered targets, and routes traffic only to the healthy targets. Elastic Load Balancing scales your load balancer capacity automatically in response to changes in incoming traffic.

**Autoscaling Groups**(Horizontal Scaling) -->
An Auto Scaling group contains a **collection of EC2 instances** that are treated as a logical grouping for the purposes of automatic scaling and management. Both maintaining the number of instances in an Auto Scaling group and automatic scaling are the core functionality of the Amazon EC2 Auto Scaling service.

The size of an Auto Scaling group depends on the number of instances that you set as the desired capacity. You can adjust its size to meet demand, either manually or by using automatic scaling.


**Overview** -->
*Isn't it beautiful how servers have firewall which is called Security groups and also how our Elastic Load Balancing automatically distributes your incoming traffic across EC2 instances and how beautifully our EC2 instances size increases to meet the demand using Auto scaling group.*



Now you got how they are connected :)

Hope You got a brief idea of what EC2 is and how it works :)

Follow for more such content.

All the suggestions are welcomed.











