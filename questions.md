Auto Scaling
1. you can perform custom actions during launch/terminate an instance using Lifecycle hooks to Auto scaling groups
   eg: is copying data when instance stops of sql server db. 
2. EBS - No datawarehouse or nightly process. 
3. Cloud formation drift detectino techniques - explicity set the property values which can be same as default value. 
4. s3 performance - randomize key for object performance. 
5. SQS - to avoid duplicate message - increase visiblity timeout for message to get it processed for 30-60 seconds 
6. red shift cluster - do the configuration for cross region snapshots
7. security for redshift data - hsm and kms
8. redshift cluster -> cluster subnet group
9. cft - speciic th target accounts and region for instances 
10. media player and media files -> web and rmtp 
11. dynomo db workload 
	priced based on provisioned throutput regardless of whether you use it or not
	cost effective for read workloads
5. redshift availablity and durarblity  - continous and incremtnal backups, keeps three copies of data 
6. page click streams -> kinesis
7. alb -> ec2 instances -modify the security of ec2 to accept traffic from alb security group
8. unecrypted to encrypted volume for root -> crate and ount a new ecnrupte ebs volume and move the data and delete the old volume
9. users cant change their wn policy but groups can do it -> deselect the option, iam policies to users
10. health check period time depends on -> code of ami, time taken to bootstrap to run
11. mem cache no preseisnt 
12. cost explorer - you can view charts of your costs and free
    budget -set custom budget and alert you when cost exceeds the budget 	
    billing dashboard - exceeds threshold and alert you

13. alb routing -> alb and bind multiple SSl certicate using SNI extension
14. cft securily configured templates
15. white list -> nat gateway 
16. s3 queyr -. athena and iam policies for bucket access fine grained
17. x forwarded for http and proxy protocal and tcop
18. basic monitoring is enabled y defaulf ic created by console
	detailed monitoring is enaled if asg is created from cli
19. Communication between regions is across the public Internet
20. AZs are connected with low-latency private links (not public internet) - AWS private link
21. PCI compliance -> enable cloud front access logs, capture requests that are sent to cloud front api.
22. user pool user access in aws services be on aws policies
23. If one AZ is down 50% 
24. less usage and less cost -> cold hdr
25. redshfit performance monitoring -> cloud watch and trustees advisor
26. cloud front is global service and usage for each locatin
27. cloud hsm backup - ebk is used to encrypt data and pbk is used to encrypt ebk before saving data to same region bucket as that of hsm cluster. 
28. if there is a peak demand in dynamo db - go for auto scaling
29. when compare to s3 logs and s3 logs go for s3 which is cheaper. 
30. enable job mark on aws glue
31. ebs is automatically replicated within its availablity zone to protect any failure. 
32. source az code commit and deploy as elastic bean stalk
33. aws vpc peering for different region. 
34. block chain - resource and member
35. key complete control and lifecycle -> KMS
36. windows server not login - key is converted and user name is correct
37. custom permission set with session duration as 6 hours
38. for billing beneifts instanceid should be in same az
39. audit purpose - cross account role


1. access the db from ec2 instance - using credentials with the authentication token. 
2. kinesis firehouse -> redshift, s3 ,elastic search and splunk 
3. migratation of application from on prem to cloud no need to change the ip address
4.  - create Route Origin aurhotization(ROA)
5.  increase write capacity of db -> raid 0 and increase ec2 instance type.
6.  ad -> simple ad connector and rbac -role based access
7.  DB monitoring -> enhanced monitoring in rds
8.  individual ip used 111.2.3.3/32
9.  s3 single signon -> setup federation proxy or an idenitty provider
10. redshift define query qeues and routing -> use worload management in parameter group
11. posis complaint - efs
12. ecs -> database credentials - keep in system management store.
13. without elb how can you achieve high availablity and fault tolerence -> script to verify the instnance, assign elastic ip address to the instance. 
14. signed urls - rtmp distribution, restrict invidival files, download your application, users doesnt support cookies
15. signed cookies - no rtmp distribution, access to multiple restrict files, all hls files, dont want to change your current url
16. instance store snapshot - still use the volume
17. which instance stop first in asg -> asg with oldest launch configuration.
18. auroroa read and write for lower prirority cqueries - create custom endpiont 
19. dynamo db performance increase -> reduce the number of partition keys
20. shield - ddos attack