---
title: "Deploying Apps into Linux Via Jenkin Plugins"
datePublished: Mon Apr 24 2023 12:34:01 GMT+0000 (Coordinated Universal Time)
cuid: clgutl3c3000409li0snb3ywi
slug: deploying-apps-into-linux-via-jenkin-plugins
tags: ec2, linux, aws, maven, jenkins

---

Hey Guys,

**<mark>ALERT:- After practicing this It can cost you Around 30 to 40 USD(Around 2500 to 3000). You can terminate the AWS instance after this or you can close Your Account.</mark>**

Let's get started, Guys!

## **Pre-Requisites**

* One should make an EC2 instance Ready with default AMI.
    
* Install MobaXterm and connect Your EC2 instance using SSH. Please read my blog, How to do this here--&gt;[https://nidhidevops.hashnode.dev/how-to-establish-ssh-connection-to-your-remote-machines-via-ssh-keys](https://nidhidevops.hashnode.dev/how-to-establish-ssh-connection-to-your-remote-machines-via-ssh-keys)
    

## Installing JAVA on a Linux machine

Okay, So the first step here will be Installing Java on a Linux machine(EC2 Instance) which we have Created on AWS.

The steps are as follows:-

* Go to [https://www.java.com/en/download/help/linux\_x64\_install.html](https://www.java.com/en/download/help/linux_x64_install.html)\--&gt;Click Java for Fedora(It's a flavor for Linux and this comes close to AWS as well)
    
* Now copy this below command used under fedora
    

`$ su -c "yum install java-1.8.0-openjdk-devel"`

if you are logged in as root and also the location is "~", now use `yum install java-1.8.0-openjdk-devel` Because we want JRE and JDK.

* It will ask "Is This Okay", Enter 'y"
    
* Use the command to see the Java version --&gt; `java -version`
    
* To remove any program use the command --&gt; `yum remove java` (Optional)
    

## Setting Java Home Path

As we know where the location of java is, Jenkins or any other software won't know where Java is, So hence we are adding it to system variables with Its path.

* Use the command `ls -a` to see all files in directories.
    
* You will see **.bash profile**
    
* Use command `cat .bash profile` to see content
    

Extra Commands to look into

\--&gt; `pwd` :- For seeing present directory

\--&gt; `cd ..` :- to move one directory back

\--&gt; `ls`:- to see the files in directory

\--&gt; `cd root` :- to get back to root folder

Okay, Back to our commands😁

* Use command `cd usr/lib` as java is installed there
    
* `ls -a`
    
* `cd jvm`
    
* `ls -a`
    
* Copy the content showing java path (Which maybe has keyword openjdk )
    
* again enter cd and that path
    
* now do `ls-a` to see jre is displayed
    
* now use command `pwd`
    
* Copy whole path
    
* Now again move to **.bash profile**
    

Use the below commands to reach back to your original positions

* enter `exit`
    
* enter `sudo su -`
    

Again Going back to edit the **.bash profile(<mark>VERY IMPORTANT</mark>)**

* enter `vi .bash profile`
    
* select `i` button so that it will be now in insert mode
    
* Under User specific environment and startup programs, Enter
    
    **JAVA\_HOME=(Paste the path, we copied earlier)**
    
    **PATH= :$JAVA\_HOME(Take care you have written without removing anything at the last) see image**
    
* to save the file, use command :
    
    click `esc` -&gt; enter `:wq`
    
    To exit without saving a file
    
    click `esc` -&gt; enter `:q!`
    
* To see if the path is set, the user is on the location **.bash profile**. Enter `cat .bash` profile. And users see the entered content.
    

## Installing MAVEN on a Linux machine

we will use **<mark>wget</mark>** to install maven --&gt; Wget solely lets you download files from an HTTP/HTTPS or FTP server. You give it a link and it automatically downloads the file where the link points. It helps to download Binaries.

* Hit the url [https://maven.apache.org/download.cgi](https://maven.apache.org/download.cgi) (you will see a tar.gz link, which is used by linux)
    
* Enter `wget` [`https://dlcdn.apache.org/maven/maven-3/3.9.0/binaries/apache-maven-3.9.0-bin.tar.gz`](https://dlcdn.apache.org/maven/maven-3/3.9.0/binaries/apache-maven-3.9.0-bin.tar.gz)
    
* now go to the url [https://maven.apache.org/install.html](https://maven.apache.org/install.html)
    
* You will see a command to unzip it in linux
    
* Use command `tar xzvf apache-maven-3.9.0-bin.tar.gz`
    
* <mark>Make Sure everything you are doing is as root user.</mark>
    
* It's recommended by Maven to install maven at opt package.
    
    User is on "/" home location, write the command.
    
    \--&gt; `ls -a`
    
* to copy a folder from one location to another type `cp -r apache-maven-3.6.3 /opt` (cp -r is copy file recursively)
    
* type `pwd` and copy the path-&gt;type `exit` -&gt;`sudo su -`
    
* type `vi .bash profile`
    
* Write the following in bash profile
    
    * **MAVEN\_HOME= (Paste the selected path above)**
        
    * **M2= /opt/apache-maven-3.6.3/bin**
        
    * **PATH= :$MAVEN\_HOME:$M2(Take care you have written without removing anything at the last) see image**
        
    * to save the file, use command :
        
        click `esc` -&gt; enter `:wq`
        

## Install Jenkins on Linux and start the Jenkin server

Write the below code as root user after exiting wherever you were.👇

```plaintext
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo yum upgrade
# Add required dependencies for the jenkins package
sudo yum install java-11-openjdk
sudo yum install jenkins
sudo systemctl daemon-reload
```

* After this to start jenkins write `sudo systemctl start jenkins`
    
    You can refer the page ([https://www.jenkins.io/doc/book/installing/linux/#red-hat-centos](https://www.jenkins.io/doc/book/installing/linux/#red-hat-centos))
    
* Go to the AWS instance
    
* Copy the public IP
    
* And add `:8080` to it and You server will get started 😍
    
* go to the Location written for password authentication, and Copy password.
    
* Paste the Password on the URL
    
* Click Installed suggested Plugins
    
* Provide Username and other details-&gt;Save and continue
    
* Click Save and finish
    
* Click Start using jenkins
    

## Create a new Jenkins Job for deploying apps

On the Home page itself

* Click Create new Job
    
* Enter an Item name
    
* Select Free style Project
    
* Click Okay
    

Now you are on the **deployment/configure** page

Under Source code Management

* Select GIT
    
* Under repository URL, copy paste your Project/App URL from github.com
    

Configuring Jenkins so that it will know directly Your git URL and JAVA And MAVEN Variables

* Click Manage Jenkins
    
* Click Global Tool configuration
    
* Add JDK Path (Goto mobaxterm terminal, type clear)
    
* Enter `echo $JAVA_HOME`
    
* Also Enter the name
    

Now for GIT

* Go to terminal and type `Which Git`
    
* If Git is not there, Install Git
    
* Enter `Yum Install Git` as root user
    

Now for Maven

* Under Build Environment
    
* Add Build step **Invoke top-level Maven targets**
    
* Write `test install` under goals which will build your `.war` file
    
* Now Save the Project and Run