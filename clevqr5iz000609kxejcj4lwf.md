---
title: "Elastic Block Storage & Amazon Machine Image"
datePublished: Sun Mar 05 2023 18:43:07 GMT+0000 (Coordinated Universal Time)
cuid: clevqr5iz000609kxejcj4lwf
slug: elastic-block-storage-amazon-machine-image
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678041268467/c17e8379-8ed0-4d09-a2a4-ac25d9a94750.png
tags: ec2, aws, ebs, ebs-snapshots

---

After EC2, Let's learn about EBS.

\--&gt; Think of it as a Network drive, you attach to your instance while they run.

\--&gt; It allows you to persist data, even after your termination.

\--&gt; They are bound to specific availability zones

PS:- Think of it as a network USB stick, which can be taken out of the computer to another

### So **What is EBS resolving**?

Please let me allow to answer this

The data stored on a local instance store will persist only as long as that instance is alive. <mark>However, data that is stored on an Amazon EBS volume will persist independently of the life of the instance.</mark> Therefore, we recommend that you use the local instance store for temporary data and, for data requiring a higher level of durability, AWS recommend using Amazon EBS volumes.

Now,

You can see EBS under EC2

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676915832042/a0219894-9905-4087-8add-1b9ae5ac06bd.png align="center")

1. Click volumes (See Attached Image)
    
2. Click Volume ID highlighted (See Attached Image)
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676915920993/613bd47f-0312-4e34-9ec9-6c9cac25a04e.png align="center")

1. Scroll down to see Attached Instances (See Attached Image)
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676915968218/0becc392-7596-4850-9ae4-dad5fb36306d.png align="center")

One more question which is very important here is--&gt;

### **What are EBS snapshots?**

EBS snapshots are nothing but backup of EBS volumes.

Please look through the image attached 👇

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678039312919/34bf24e5-66c0-4296-97fb-b476158a98de.png align="center")

You can clearly see in the image that you can create a snapshot for your EBS volumes and then from that snapshot one can restore multiple fully provisioned EBS volumes OR Copy the snapshot across regions else share it with other AWS accounts.

After restoring EBS Volumes, Finally one can **Launch there Instances.**

Easy???

Let's study a bit about AMI's

## **AMI(Amazon Machine Image)**

In Technical terms An Amazon Machine Image (AMI) is a supported and maintained image provided by AWS that provides the information required to launch an instance.

In very easy language **it's the customization of an EC2 instance.**

Here,

<mark>--&gt; You add your own configuration, software, own Operating System, Monitoring</mark>

<mark>--&gt; Its boot/configuration time is faster because all your software is pre-packaged</mark>

Take a look at the attached Image

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678040494069/95aae27e-702a-4cca-b6a7-cebe47417dd6.png align="center")

Go to EC2 -&gt; Instaces-&gt; Launch new Instance-&gt; Scroll Down

And yes, That is **AMI**

You can Launch Instaces from Public AMI(AWS Provided), Your own AMI & An AWS marketplace AMI(AMI someone else made).

Finally we learned About EBS and AMI

Guys cloud is super-fun 😍

This doesn't end here, I will come again with my next blog!

Stay Tuned!!😊

All suggestions are welcomed!!

A small hint Next Blog I will be covering **Databases 🛢️**