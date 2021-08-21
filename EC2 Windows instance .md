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

