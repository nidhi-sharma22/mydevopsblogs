---
title: "AWS Identity Access Management"
datePublished: Thu Nov 03 2022 18:11:00 GMT+0000 (Coordinated Universal Time)
cuid: cla1dvxhf000008jq6is8dme2
slug: aws-identity-access-management
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1667411977026/UjW33veCW.png
tags: cloud, linux, aws, iam, aws-iam

---

**T**he first question in our mind comes is

What is IAM? Why are we starting with this service only in AWS?

**What is AWS IAM(Identity Access Management)?**

Try to understand the full form first, It says Identity Access Management which clearly means to Manage Identity Access.

Now Let's move to Technical Definition which AWS recommends \*\*IAM provides fine-grained access control across all of AWS. With IAM, you can control access to services and resources under specific conditions.\*\* Use IAM policies to manage permissions for your workforce and systems to ensure the least privilege. IAM is offered at no additional charge. Now you know what is IAM :-)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676824965613/46c78c8e-2bde-46c5-9233-0ad342422879.png align="center")

\*\*Note :- Anyone who has just created an account on AWS, he will be always logged in as Root\*\* But Why first this service? Because AWS strongly recommends that you use the root user only for two things:- - Create the first administrator user in AWS Identity and Access Management (IAM) - Perform those tasks that can be performed by only the root user. That means the root user has full access, AWS highly recommends not using the root user but rather creating users and groups under the IAM service and logging into the account with that user created under IAM. Now you got my point about why I am taking this as my first service :-) Below Attached Image displays the Users.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676825006704/a87331b9-ba36-4ea7-8aeb-7fdf242f8afd.png align="center")

There will be one more question revolving around your mind, But what are IAM policies? (See definition) \*\*IAM policies \*\* IAM policies define permissions for an action regardless of the method that you use to perform the operation. For example, if a policy allows the GetUser action, then a user with that policy can get user information from the AWS Management Console, the AWS CLI, or the AWS API. Now Again Read the definition IAM provides fine-grained access control across all of AWS. With IAM, you can control access to services and resources under specific conditions. \*\*Use IAM policies to manage permissions for your workforce and systems to ensure the least privilege. IAM is offered at no additional charge.\*\* PS:- I will make you by Heart this definition. :-D :-D Just kidding :-) Please view the below image for better understanding of IAM policy.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676825039444/215cf35b-6459-4807-b5d2-7b39c9aedbc0.png align="center")

Oh IAM policy is in \*\*JSON \*\* format. Yes, IAM policies will be always in JSON format. Now Let's understand the things written in JSON Effect: The effect can be Allow or Deny. By default, IAM users don't have permission to use resources and API actions, so all requests are denied. An explicit allow overrides the default. An explicit deny overrides any allows. Action: The action is the specific API action for which you are granting or denying permission. Resource: The resource that's affected by the action. For example:-Some Amazon EC2 API actions allow you to include specific resources in your policy that can be created or modified by the action. You specify a resource using an Amazon Resource Name (ARN) or using the wildcard (\*) to indicate that the statement applies to all resources. Condition: Conditions are optional. They can be used to control when your policy is in effect. \*\*Note:- Also, You can Create your own policy.\*\* I recommend making your own User under IAM and attaching a policy(give permissions) to that user. Hope till this everything is cleared! \*\*What are Groups?\*\* Easy Definition:- An IAM user group is a collection of IAM users. For example, you could have a user group called Admins and give that user group typical administrator permissions.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676825065482/3327d33f-af0a-4b60-9b26-c913d7c8fc49.png align="center")

Again One More Questions People Have there in their Mind That is,\*\* Can the same user be in two groups?\*\* \*\*\*Yes, users can belong to multiple user groups.\*\*\* Each user has an individual set of security credentials. This is the Basics of IAM, If you have any queries please comment below.

Cloud is Just awesome!

Also, You can review this article for IAM ROLES https://spacelift.io/blog/aws-iam-roles

Follow for more such Content.

All suggestions are welcomed!