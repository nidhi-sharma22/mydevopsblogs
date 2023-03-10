---
title: "How to establish SSH connection to your remote machines via ssh keys."
datePublished: Fri Mar 03 2023 13:02:26 GMT+0000 (Coordinated Universal Time)
cuid: clesjpbus000c09l26b98fhra
slug: how-to-establish-ssh-connection-to-your-remote-machines-via-ssh-keys
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1677848192211/e70afe63-0832-4627-8706-b436d85acbb3.png
tags: linux, devops, ssh, aws-ec2, ssh-keys

---

Hey guys!

Welcome back to my blog.

Today we will learn a simple thing where in you will connect two machines via SSH.

Let's Begin!

Pre-requisite:-

Download MobaXterm

MobaXterm?

\-&gt;It is **a toolbox for remote computing**.

After Instaling it ,

* Click Session-&gt;click ssh-&gt;enter the remote host details(I will enter the public address of my Ec2-server I created on AWS)-&gt;check the Checkbox(near specify user name)
    
* Enter the username **necessarily** as ec2-user.
    
* Click Advance SSH settings
    
* Upload the key pair, You generated it while creating an instance on AWS.
    

Below Attached is the Image showing all the details I explained above.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677494624147/196dfc9f-f64a-41e7-af0b-535fc2e6ec4b.png align="center")

* Click OK
    

See Your server is started

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677494739822/247007dd-b91a-457f-a8f6-1e13cf3e58db.png align="center")

Yay!

Finally, Connect AWS Linux servers using SSH Client.

1st step is done guys, Congratulations!

Next, we will make one more instance on AWS.

\-&gt; After creating instance, make sure you connect that too with ssh using Mobaxterm.

Now those servers will look something like this,

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677500578057/2202cbd0-cf23-4443-8dd7-8a8027576a61.png align="center")

Now all the gameplay will be of Commands...

Let's start(use these commands in 1st server)

* type ssh ec2-user@ipaddress(use the ip adddress of the linux machine you want to connect with this)
    
* click yes
    
    (after this Some errors will be generated, correct?)
    
* type ssh-keygen
    
    It will automatically create two keys public and private. Let's learn more about them.
    
    **Private keys**:-private key is located on the client machine and is secured and kept secret.
    
    **Public keys:-** public key can be given to anyone or placed on any server you wish to access.
    
    <mark>When you attempt to connect using a key-pair, the server will use the public key to create a message for the client computer that can only be read with the private key.</mark>
    
    (Now you got some idea what to do!)
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677845897525/278eaf0a-6365-4a31-80e6-cf7f3762f55d.png align="center")
    

Now the important thing here is

**Go to the next server where you want the connection.(Use commands in 2nd server)**

* Now write the command `sudo su -` to become a root user.
    
* write the command vi /etc/ssh/sshd\_config
    
* Update Password Authentication to Yes
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677846204920/9bf5d0fd-97d9-4727-9be4-a0ba77348723.png align="center")
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677846430435/a3dad140-2c07-462b-a046-6dfd0db90748.png align="center")
    
    now as a root user, change the password of the user
    
* enter the command `passwd ec2-user`
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677846641259/77b92cab-5921-4bed-8736-dc2efe3f3935.png align="center")
    
* Your password will be updated successfully
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677846710495/47db39bb-55d0-4144-9a13-19b00d67edba.png align="center")
    

After this write

* `service sshd reload`
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677847476945/8c977130-84b4-4c14-9d01-e3f6630630a4.png align="center")

Now come back to your 1st server

* type `ssh-copy-id user@<target-server>`     
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677846837926/fd3f4c84-8167-40cc-b954-9e687e78be9a.png align="center")
    
    Enter your Password(Recently Updated)
    
* To check if your keys are copied
    
* go to `.ssh` folder (cd .ssh)
    
* type `ls -a`
    
* then write command `cat id_rsa.pub`
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677847243704/0efb2a2b-2964-4e9a-a501-217f9f473ce4.png align="center")
    
    Go to the 2nd server and hit the following commands(Please see the screenshots)
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677847333004/5196decf-fbd3-4f7b-b571-2bf6ef0d6fef.png align="center")
    

Finally, The final command

* ssh ec2-user@&lt;targetipaddress&gt;
    

* **<mark>Boom </mark>** it will definitely work!!!
    
* see You will have full access to your 2nd instance
    
    Let me show you some screenshots to understand it more efficiently.
    
* So in the first server I made a text file(Please see screenshots thoroughly)
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677847765624/43d35482-658e-4b5c-921a-9de9aa3a3ff1.png align="center")
    
    Now let me show you the same file in the second server
    
* ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677847814438/3563e604-efaf-416c-8f03-8ef6f2190f01.png align="center")
    

Guys, You have done this, Yay!!

See this was very easy right :)

If you have any confusion, or find any sort of suggestions, Do let me know :)

All suggestions are welcomed!

More DevOps content is Ahead!!

Apart from this to know How to build a Docker image for any Application!

You can read this blog [https://riddhisharma.hashnode.dev/devops-project](https://riddhisharma.hashnode.dev/devops-project)