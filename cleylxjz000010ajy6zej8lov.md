---
title: "Amazon Simple Storage Service (Amazon S3)"
datePublished: Tue Mar 07 2023 18:51:26 GMT+0000 (Coordinated Universal Time)
cuid: cleylxjz000010ajy6zej8lov
slug: amazon-simple-storage-service-amazon-s3
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678214416496/15036dc7-8b49-410f-9397-48d1eb4b04ac.png
tags: aws, amazon-s3, s3, iam, aws-s3

---

Hey Guys,

As the name suggests, S3 is related to storage and yes Guys it is related to storage.

Let's Learn more about S3(We will call Simple Storage Service as S3).

Are Guys Excited??

We will learn from very Basic...

In layman's terms, Amazon S3 is object storage built to <mark>store and retrieve</mark> any amount of data from anywhere.

Now Let's see how it looks like in AWS

Let's deep dive 🏊

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678105332250/949117fb-172a-446b-942f-2dd7e59da431.png align="center")

wait wait....

What is This bucket?

we were talking about S3 🤔

Now Read Carefully,

<mark>S3 Allows people to store Objects in a Bucket.</mark>

Keep In Mind guys **<mark>Buckets are Not directories</mark>**, Please see the Attached Image

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678127110785/c55ea721-a6b1-417e-874a-93df46aa57dc.png align="center")

### **What S3 Is used for?**

Using this service, you can easily build applications that make use of cloud native storage. Since Amazon S3 is highly scalable and you only pay for what you use, you can start small and grow your application as you wish, with no compromise on performance or reliability.

Also S3 is used for Backup & storage, Disaster Recovery, Archive, Hybrid Cloud Storage, Application Hosting, Media hosting, Data lakes & big data analytics, Software delivery and static website.

Now let's move to do some **practical** things to know it better.

Go to Amazon s3-&gt;click buckets from the left side menu-&gt;click create bucket

And yes there you go

* Write Bucket name(Its hould be unique)
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678210534898/1a2e8031-6c9c-42ab-95c8-f8949d1a2c99.png align="center")
    
* Select AWS region
    
* Let object ownership be ACL's disabled
    
* Block All Public Access
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678210586604/304d2783-4f9f-4ef7-b7fe-6edc433d8958.png align="center")

* Let Bucket versioning be Enabled(Discussed below)
    
* Let Default encryption be as it is
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678210650454/23a85315-f5ab-4268-8bab-e2e45d3fd632.png align="center")
    

Now before moving further let me tell you the importance of **Bucket versioning**

S3 bucket versioning is a feature that allows you to store multiple versions of an object in an S3 bucket. Each version of an object is assigned a unique identifier and a version number. When you upload a new version of an object to the S3 bucket, the new version replaces the previous version, but the previous version is still stored and can be retrieved if needed.

### **Versioning**

It is a simple yet powerful feature that can provide valuable protection and recovery options for your data stored in an S3 bucket.

With versioning enabled, you can:

1. Protect against accidental overwrites or deletions
    
2. Recover from both unintended user actions and application failures
    
3. Maintain a complete history of object changes
    

For Seeing the versions you can toggle **Show versions** like seen in the attached Image(update the index.html object and upload it with same name)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678213485655/1ec34c6c-9f45-4fdb-bbaf-c442de79682f.png align="center")

Isn't it great to see versions of objects😍

Let's move to one more crucial part of S3 and that is

## Bucket Policy

Yes, Like IAM, we have a policy for Buckets as well, let me show you how you can access that

After Creating a Bucket

1. Select the bucket that you want to add the policy to.
    
2. Click on the "Permissions" tab and then click on "Bucket Policy".
    
3. In the "Bucket policy editor" window, enter the policy in JSON format. The policy will define the permissions for the bucket, including who can access the bucket and what actions they can perform on the objects in the bucket.
    
4. Once you have entered the policy, click on "Save" to apply the policy to the bucket.
    

Bucket Policy is also in JSON format and here is the Example

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1678211808422/ac216208-872b-4306-b6dd-dfae075c133f.png align="center")

Let's move to

### **S3 Encryption**

**No encryption**:- If the User uploads a file to the bucket and no encryption is done on the server side or client side.

**Server-Side Encryption:-** User uploads a file to the bucket and Server encrypts the file after receiving it

**Client-Side Encryption:-** User Encrypts the file Before uploading it to the Bucket.

After Encryption, Let's move to

### **S3 Storage Classes**

* Amazon S3 Standard - General Purpose --&gt; Used for frequently accessed data
    
* Amazon S3 Standard-Infrequent Access (IA) --&gt;Used for data that is less frequently accessed, but requires rapid access when needed
    
* Amazon S3 One Zone-Infrequent Access--&gt; Used for Storing secondary backup copies of on-premise data, or data you can recreate
    
* Amazon S3 Glacier Instant Retrieval--&gt; Great for data accessed once a quarter
    
* Amazon S3 Glacier Flexible Retrieval--&gt;for data archiving and long-term backup. Amazon S3 Glacier provides flexible retrieval options that are Standard & bulk
    
* Amazon S3 Glacier Deep Archive--&gt;for long-term storage
    
* Amazon S3 Intelligent Tiering--&gt; Moves objects automatically between Access Tiers based on usage
    

Above are Different storage classes with Different Costs. I have kept it very brief. If anyone has doubts about these sections, please let me know in the comment section I will make it detailed and precise.

A very Important Statement About S3 is here guys👇

### **<mark>Data transfer IN to the AWS S3 service is free. Data transfer OUT of the AWS S3 servers to the Internet is charged.</mark>**

Next, We will learn About **AWS Snow Family** ☃️❄️⛄

Stay Tuned for more content like this!

All suggestions are welcomed!!

For Learning more about Policies you can visit my IAM blog

[https://nidhidevops.hashnode.dev/aws-identity-access-management](https://nidhidevops.hashnode.dev/aws-identity-access-management)