
# Welcome to Amazon EC2 tutorialGuide
Here I have given complete explanation about Amazon EC2 service in very easy and understandabale language. 
you will find theory and practical implementention about how we can create remote instance using amazon EC2.


## What is Amazon EC2 and why we should use it?

<ul>
  <li>EC2 stands for Elastic compute cloud
  <li>An AWS EC2 instance is also called as computer, machine, box, PC and server.
  <li>Amazon Elastic compute cloud provides scalable computing capacity in the amazon web services (AWS) cloud. 
  <li>If you use Amazon EC2, you do not require to calculate the cost for hardware and also it will give three major benefits and they are as follows:
  
  <li> <b>Availability:</b> it means your remote machine or instance will run 24 * 7.
  <li> <b>Scalability:</b> you can increase or decrease hardware configurations of EC2 instance at any point of time.
  <li> <b>Pay as you go Pricing:</b> AWS will charge according to the resources you have used.
</ul><br>

<p style="text-align: justify;">Using EC2 service you can create your virtual instance with Operating system likes Windows, Ubuntu, and various flavours of these operating system. also you can choose from various hardware configurations like how much RAM and HDD(hard disk) you want, how much CPUs you want. you can also add rules for allowing or blocking any type of network traffic to your instance. you can make your instance as a webserver.</p> 

## About EC2 Free tier
AWS Free Tier includes 750 hours of Linux and Windows t2.micro instances, ( t3.micro for the regions in which t2.micro is unavailable) each month for one year. 

## Features of EC2
<ul>
  <li>you will get preconfigured templates for your instances, known as Amazon Machine Image(AMI) which contains the configurations of OS and application server.
  <li>you will get multiple instance types like t2.micro, t2.small, t2.medium, t2.large and many more different configurations are available using which you can create instance with desired capacity.
  <li>you can add multiple volumes if you want more storage.
  <li>you can create customized AMI from your instance and create multiple instances using that customized AMI.
  <li>you can create snapshots of your volumes which is useful when you want to copy entire volume across multiple regions.
  <li>you can attach/detach volumes if you need.
  <li>you can manage incoming traffic towards you instance using security groups.
</ul><br>

## What is Security Groups?

<ul>
  <li>A security group acts as a virtual firewall for your EC2 instances to control incoming and outgoing traffic.
  <li>Inbound rules control the incoming traffic to your instance, and outbound rules control the outgoing traffic from your instance. When you launch an instance, you can specify one or more security groups.
  <li>If you don't specify a security group, Amazon EC2 uses the default security group. You can add rules to each security group that allow traffic to or from its associated instances. 
   <li>You can modify the rules for a security group at any time. New and modified rules are automatically applied to all instances that are associated with the security group.      <li>When Amazon EC2 decides whether to allow traffic to reach an instance, it evaluates all of the rules from all of the security groups that are associated with the instance.
</ul>

## what is key Pair?
A key pair, consisting of a public key and a private key, is a set of security credentials that you use to prove your identity when connecting to an Amazon EC2 instance. Amazon EC2 stores the public key on your instance, and you store the private key. For Linux instances, the private key allows you to securely SSH into your instance. Anyone who possesses your private key can connect to your instances, so it's important that you store your private key in a secure place.
  
  
## What is .pem and .ppk file?

.pem stands for Privacy Enhanced Mail which is most common format of certificates and cryptographic keys. the content is encoded in the BASE64 ASCII format which contains public and private keys.
.ppk stands for Putty Private key which is required when you want to connect to your instance using putty.

The .pem and .ppk files are similar because they are both private key file formats.
 
The differences between .pem and .ppk are the following,
 
System platform compatibility,<br>
Linux users —> .pem file format<br>
Mac users —> .pem file format<br>
Windows PowerShell users —> .pem file format<br>
Windows PuTTY/Cygwin users —> .ppk file format

