1. How to access the RDS from ec2 instances - IAM DB Authentication
2. AWS Budgets - set custom budgets 
3. Cost Explorer - visualize and manage your cost
4. If you are not able to connect to instance -> pem converted and user name is correct or not 
5. Frequent schema changes - dynamo db
6. Metrics that is not available in Cloudwatch metrics - memory
7. Lambda sensitive information keep in KMS
8. Kinesis firehose -> s3, redshift, elastic search and splunk
9. move the application from on prem to aws and use the same IP Address -> create Route Origin Authoriation(ROA) and then advertise your whitelisted ip
10. Improve the writethroughput of database -> RAID 0 with 2 EBS volumes, increase instance size
11. Idenitty federation - ad directory service AD connector and RBAC -> IAM Role
12. How to monitor your database - enable enhanceed monitoring in rds
13. s3 singlesign on -> setup federation proxy or identity provider , configure IAM role and policy 
14. 5 messages recieved 20 times -> message delete is not happening 
15. Redshift define the number of query queues how queries are routed for processing -> Use workload management(WLM) in the parameter group configuration.
16. Redshift - montiroing all copy and unload -> enhance vpc routing
17. ECS secure credentials -> in system management store 
18. Default montiriong - console and enhanced monitoring - CLI
19. montirong disck utilization and moemry -> install cloud watch agenet which gathers disk utlizaiton and memory and view custom etrics
20. how you will ensure high avialablity and fault tolerance without elb - scripts, assign ip address 
21. Signed url -> RTMP distribution, restrict access to invidial files,
22. signed cookies -> no rtmp, access to multiple files, no change in current url.
23. Root volume can be used when instance is running while taking snapshot
24. which instance will be out -> Asg having oldest configuration
25. Aurora write capacity to high priority one and read capacity to low priority one -> create custom endpoints
26. improve dynamo db performance -> partition key with low cardinality attributes have few dinstinct values
27. shield - ddos 
28. less usage -> cold HDD
29. Traffic shiftings  for lambda
    canary - traffic shifting in two increments
    liner - traffic shifting in equal increments
    all at once -traffic shifting from original one to new one all at once. 
30. S3 IA is low latency and high throughput
31. Bastion cost can be small instance
32. default ecnryption - stroage gateway and glacier
33. PPS -> cloudfront and ELB
34. If the dynamo db doesnt have enough capacity to storethe data -> increase write capacity assigned to the shard table. 
secure your application by allowing multiple domains to serve SSL traffic over the same ip address - generate ssl certificate
with aws certificate manager and create a cloud front web distribution.then associate the certificate with your web distribution
and enable the support for SNI
35. decouple architecture - sqs and sws
36. hot attach -running, warm attach - stopped , cold attach - launched
37. EBS volume automated bacup -> ADM to create all ebs snapshots
38. EBS replicated in single AZ only.
39. IP switch from primary db to seconadry db - cname get change automatically
40. Cognito ID is returned for auth verification
41. Shared responisbility model
42. DR plan
    1.  Backup and restore -> slow one frequent snapshots and restore 
    2.  pilot light -> core system running faster than abobve, active/passive failover
    3.  warm standby -> faster than above, scaled down version of fully functional environment , active/passive failover
    4.  multi site -> fastes active and active , cost high and no downtime. 
43. Default subnet of VPC is public subnet.So instances in default subnet has both public and private ip. 
    Instances in non default subnet has private ip only and not public. 
44. Mobile app development real time - App sync and dynamo Db
45. VPN -IPSEc and TLS tunnels  using private sessions between vpc and on prem
46. SWF decision task -> tells the dcider the state of workflow of execution 
47. Max 5GB in single upload > 100MB till 5 TB in multi part upload 
48. S3 objects will execte in parallel operations. so will retriving you will get outdated data. 
49. S3 Glacier with retrieval capacity 150MB/s of retrieval throughput -> expedited retrival, purchase provision retreival capacity
50. s3 performance --3500/s for add  and 5000request/second for retrieve have good performance. 
    beyond that use sequential patterns
51. in single s3 the data is replicated in multiple facilities in single AZ.
52. Lambda erros in cloud watch - invocations and dead letter errors. 
53. AR game dynamodb -> DAx with auto scalling enabled and API gateway for caching 
54. A new AMI need to use for auto scaling -> create a new launch configuraiton
55. hardware or software provisioning, setup, configuration, scaling and backups. -> dynamo db
56. hardware or software provisioning, setup, configuration, and backups. -> RDS
57. EC2 lifecycle
    1.  pending - no cost
    2.  running - no cost
    3.  stopping - no cost for regular and cost is there for hiberation 
    4.  stopped - no cost
    5.  shutting-down - no cost
    6.  terminated - cost 
58. vault policy lock for legal and compliance requirements - retain archive for 1 year 
    and no delete is applicable here. 
59. change the instance type from one to another in auto scaling group. - create a new launch configuration
    with the new instance type and update the ASG. 
    Note - you cant modify the launch configuration after you create it. 
60. if your asg instance is not launching new instance when your high memory usage exceeds - install cloud watch monitoring
    scripts in the instance. send custom metrics to cloudwatch which will trigger auto scaling group to scale up. 
    detailed monitoring is not applicable here since it is not related to "memory"
70. costing - running ec2 and ebs attached to ec2. 
71. automate the recurring tasks - coordinate multiple aws services into serverless workflows - step functions 
72. redshift spectrum -> run sql queries againsts exa bytes of unstructured data in amazon s3. no loading or transformation is reqruired. 
73. Name any resources - ARN 
74. ELB has subnet for each AZ in region/VPC . 6 instances for elb, public,private and multiple fault tolerance. 
75. Dynamo DB - increase the thoughput and decrease based on traffic patterns -> using auto scaling.
76. remember to provide the best option for the fault tolerance 6 instances each 2 in 3 AZ. 
77. when no duplicated -> ksiness and duplicate no sqs message
78. order processing - sws 
79. RDS regular metrics - CPU utilization 
80. RDS enhanced metrics -> RDS child process, RDS process, OS process
81. Where SSL/TLS certicate store -> AWS certificate manager, IAM certificate store
82. bucket name -> bucketname.s3-region.amazonaws.com 
83. Tracing and analzye user requests  - xray
84. spot instance are terminated if the instance gets interuppted by ec2 for capacity requirements
    But stop and hibernate options are available for persistent spot requets and spot fleets with maintain option enabled. 
85. public s3 files -> upload make sure and configure s3 bucket policy for public read 
86. ldap on on premise service need to integrate with AWS VPC using IAM. but it is not comptabile with SAML. 
    - Develop an on premise custom identity broker application and use STS credentials
87. Data store
    1.  temp storage - instance store 
    2.  multi instance stoage - EFS
    3.  high durable storage - S3, EFS
    4.  static data - S3, EFS
    5.  low latency data - EBS
88. Connection Draining -> if backend instasnce fails the LB should not send any requets to unhealthy instances but should allow existing request to complte. 
89. Sticky session - session mainteance in LB
90. Cross Zone load balacing -> distribute request evenly across the registered instances in all enabled AZ. 