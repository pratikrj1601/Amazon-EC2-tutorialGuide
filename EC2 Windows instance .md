### Here I have mentioned step by step process of how we can create a windows instance using Amazon EC2 service.

- Stage 1: select AMI (Note: select free tier eligible) </br>
- Stage 2: select instance type (t2.micro) </br>
- Stage 3: select number of instances </br>
- Stage 4: add storage </br>
- Stage 5: tags (leave it as default) </br>
- Stage 6: Security groups </br>
- Stage 7:  Review details and launch and download the key pair. </br>
- Create a new key pair and give suitable name to it. <hr>

### But first we will discuss what is Regions and availability zones because it is required before creating instances in EC2

- In below mentioned figure you can see that there is 25 geographical regions and 81 availability zones are currently present. 
- Regions are created to avoid traffic and latency and also customer from different part of world can choose a region closest to them in order to host their cloud infrastructure.
- Availability Zones are distinct locations within an AWS Region that are created to avoid failover scenarios. fro example, if one zone is facing dwontime then oher zones can serve the request to the users and in that way we are getting almost 100% availability.
- They provide inexpensive, low-latency network connectivity to other Availability Zones in the same AWS Region. Each region is completely independent. 
- All AZs in an AWS Region are interconnected with high-bandwidth, low-latency networking, over fully redundant, dedicated metro fiber providing high-throughput, low-latency networking between AZs. All traffic between AZs is encrypted. 
- AZs are connected to each other with fast, private fiber-optic networking, enabling you to easily architect applications that automatically fail-over between AZs without interruption.<br><br>
![image](https://user-images.githubusercontent.com/83777309/130329084-c567ea7e-9a63-47d4-b750-0ce2fd15b915.png)

### Creating Windows Instance on AWS console

This is your EC2 dashboard. as you can see curently we are in Mumbai region and we have no instances. we will create here windos instance.<hr>
![image](https://user-images.githubusercontent.com/83777309/130415165-3fe9e3f6-8b3c-48f1-bc55-a7e1a9f42b9b.png)

- Stage 1: Click on launch instances from the dashboard and select AMI (Note: select free tier eligible) as we are planning to create windows instance we will select below mentioned instance. </br>

![image](https://user-images.githubusercontent.com/83777309/130414809-5ea0d9e8-795c-46b1-b606-9604e4ce5c78.png)<hr>

- Stage 2: select instance type (t2.micro). it will come with 1 CPU and 1GB RAM.

![image](https://user-images.githubusercontent.com/83777309/130415688-562bc2f4-8c88-4824-b1a9-eb71b4b5a8c8.png)<hr>

- Stage 3: select number of instances. you can create 10 instances at once but here we will select nly 1.

![image](https://user-images.githubusercontent.com/83777309/130415908-bebd01fb-3c96-44ec-9d44-0179ecbeb266.png)<hr>

- Stage 4: add storage. Here you will get 30 GB of Hard disk space by default. if you want to add another volume, you can but it is chargebale.

![image](https://user-images.githubusercontent.com/83777309/130415999-ed670532-5c3d-4a03-a524-bd592d4211b2.png)<hr>

- Stage 5: tags (leave it as default) A tag is a label that you or AWS assigns to an AWS resource. Each tag consists of a key and a value. For each resource, each tag key must be unique, and each tag key can have only one value. You can use tags to organize your resources, and cost allocation tags to track your AWS costs on a detailed level.

![image](https://user-images.githubusercontent.com/83777309/130416076-d647c8e5-1c7c-459b-a218-ce79c4b59928.png)<hr>

- Stage 6: give suitable name to Security group because it will help you to manage the incoming traffic control and port settings.
- as you can see AWS will open RDP port for windows instance because it is required to connect. port is point of communication using which you can connect to yur remote instance from your device.

![image](https://user-images.githubusercontent.com/83777309/130416162-1639cfca-8880-43e0-b0a2-7d3657d95c5a.png)<hr>

- Stage 7: Review details and launch and download the key pair. Here you can check all the configurations like AMI, instance type, HDD (Hard disk), Port etc. 

![image](https://user-images.githubusercontent.com/83777309/130416263-ffa60197-09f1-4aca-886c-689366d87571.png)<hr>

- Stage 8: Select Create a new keypair and give suitable name to it and download it. you can also use existing keypair option but it is good practice to create separate keypair for different instances. if you have only one keypair for all instances and if it gets deleted then you won't be able to connect any of the existing instances.

![image](https://user-images.githubusercontent.com/83777309/130416360-08a40c4f-c2df-4c19-9dcf-6be4914a206c.png)<hr>

- Now click on view instances and you wil be redirected to EC2 dashboard.

![image](https://user-images.githubusercontent.com/83777309/130416560-702bef81-58a5-4453-9216-7afe500c6bc4.png)<hr>

- This is E2 dashboard where you can see list of all instances. click on edit name and give suitable anme to your instance.

![image](https://user-images.githubusercontent.com/83777309/130416623-fc1750bd-f01b-40a6-a053-139180e82630.png)<hr>

- you can select the instance and you will find all details like Public IP, Private IP, what ports are opened, instance DNS name, instance state, instance type etc.

![image](https://user-images.githubusercontent.com/83777309/130416723-40878f66-f7b0-4f3f-b533-c0fb8aa1391f.png)<hr>

-Now select your instance, click on connect and go to RDP client where you can find the details on how we can connect.

![image](https://user-images.githubusercontent.com/83777309/130416877-2c36578e-e234-4553-ae0d-1cb2877754d0.png)<hr>

- You have to open Remote Desktop Application and you required DNS name, Username and Password inorder to connect. you will get DNS name and Username directly from AWS console. you have to click on get Password and it will ask to upload the pem file you already created at the time of instance creation.
- upload the .pem file, click on Decrypt password and now you are ready to connect.

![image](https://user-images.githubusercontent.com/83777309/130417218-50e0d687-a454-4496-8642-e5294dbe10ba.png)<hr>

- Now copy the DNS name to remote desktop application and click on connect.

![image](https://user-images.githubusercontent.com/83777309/130416921-38dbf6e7-11e1-42a2-aafa-bfe2d5b6233e.png)<hr>

- Now add username and passowrd and click on yes and wait for few minutes to start the instance.

![image](https://user-images.githubusercontent.com/83777309/130417304-f1321134-cc48-47e1-9ec9-b210bd643d13.png)<hr>

- As you can see we have successfully connected to Windows instance. Now you can perform your required task using this instance.
- 
![image](https://user-images.githubusercontent.com/83777309/130417685-2c334a20-75e6-41e5-825f-999fbfad6806.png)<hr>

### NOTE: Do not forget to stop the instance once you have done with your work. for stopping the instance go to EC2 dashboard --> select the instance --> Actions --> stop instance.

## I hope above steps will help you on how to create an Windows instance on AWS and how to connect to it. THANK YOU !!!!


















