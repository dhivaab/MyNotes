1) Inside the instance to avoid dataloss what need to be done before termination? add life cycle hooks to auto scaling group that will put the instance in wait state. 
default wait state is 1hour. you can do all critical activities here. 
2) If an application is scaling up and down multiple times in the same hour. what you will do? modify the cool down timer.modify the alarm period that triggers your auto scaling down policy
3) Aurora - Size is high 64Tb and replica less than 100ms
4) sqs message -> each message take 55 seconds to complete somestimes being pulled twice. increase visiblity time out to 60 seconds. 
5) s3- hexa hash
1. EC2 instance - state change need to monitored - cloud watch logs is enough for monitoring

2. Out of threee AZ instances have to 2 ELB nodes? how many private ip address will be used by ELB nodes at the intiial lauch? -

2 nodes in 2 AZ will consume two private ip address.

3. RDS - Aws will do a storage volume snapshot of database instance during the backup window once a day transaction logs for every 5 minutes will store in S3.

4. KMS is region specific

5. random selection - multi value routing policy

6. lambda high memory low cost

7. dont assign vpc to lambda. fi we assign then it will asisng ENI and this process will take some time which can increaes latnecy of lambda results

8. NAT - http interente and bastion ssh and rdp

9. aws security - network level - NACL instance level - security groups

10. AWS PrivateLink provides private connectivity between VPCs, AWS services, and on-premises applications, securely on the Amazon network

11. stack based model for its resources in AWS. different stacks for development and production. - Ops works to define different layers for your application.






https://www.aws.training/ 



DR Scenarios in AWS
 
Backup & Restore (Data backed up and restored)
Pilot Light (Only Minimal critical functionalities)
Warm Standby (Fully Functional Scaled down version)
Multi-Site (Active-Active)
 
Multi-Site is the one with least RTO and RPO. In this scenario you are always running a duplicate copy of your production resources in another AWS region and do a DNS failover during a disaster. I hope this was useful for you.
RDs and EBS outside and connection string in s3


1) For an application - required I/O and minimum memory requriements for an application ,
2) during hiberation - ony elatic ip cost is there and no instance cost
	during thsi private ip is retained and public ip is released and allocate new one during restart from hiberante state. 
3) vpc peering - no overlapping ips, no on premise connectino for transitive peering 
4) if we disable rdp backup - you are compromising point in time backups
5) Block chain - Resource, Memeber,Network 
6) s3 bucket should trigger code pipeline that will intiate EBS - disable periodic check and create event rule.
7) EFS - use EFS mount helper.
8) use TLS to generate new certificate and upload in certificate manager.

1. EC2 instance - state change need to monitored - cloud watch logs is enough for monitoring 
2. Out of threee AZ instances have to 2 ELB nodes? how many private ip address will be used by ELB nodes at the intiial lauch? - 
2 nodes in 2 AZ will consume two private ip address. 
3. RDS - Aws will do a storage volume snapshot of database instance during the backup window once a day transaction logs for every 5 minutes will store in S3. 
4. KMS is region specific 
5. random selection - multi value routing policy
6. lambda high memory low cost
7. dont assign vpc to lambda. fi we assign then it will asisng ENI and this process will take some time which can increaes latnecy of lambda results
8. NAT - http interente and bastion ssh and rdp
9. aws security - network level - NACL instance level - security groups
10. AWS PrivateLink provides private connectivity between VPCs, AWS services, and on-premises applications, securely on the Amazon network