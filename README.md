**AWS-Project-1**

**Description**:
This project contains a cloudformation template to deploy a VPC with 3 public, 3 private and 3 DB subnets spread across three Availability Zones. It deploys an internet gateway, with a default route on the public subnets. It deploys NAT gateways and default routes for them in the private subnets. The application is based on ECS Fargate cluster with Auto Scaling and DB is Aurora Postgres. Also, an S3 bucket is provisioned. 


![arch1](https://user-images.githubusercontent.com/103620921/169332190-1b77ab21-5bfa-4933-a6fb-f9fa6a94b28b.JPG)



**Disaster Recovery Plan (High Level)**
A resilient workload helps to prepare for disaster events, which is one of the biggest challenges one can face. 
Such events include natural disasters like earthquakes or floods, technical failures such as power or network loss, and human actions such as inadvertent or unauthorized modifications.

AWS disaster recovery plan should include the following steps:

1.	**Backup your data:** Regularly backup your data to Amazon S3 using AWS Backup. This will ensure that you have a copy of your data in case of a disaster. For example, you could set up a daily backup of your critical data to an S3 bucket in a different region.
2.	**Create a recovery plan:** Create a recovery plan that outlines the steps you will take in case of a disaster. For example, your recovery plan might include the following steps:

•	Determine the cause of the disaster: Identify what caused the disaster, such as a hardware failure, a natural disaster, or a cyber attack.

•	Activate your recovery plan: Once you have identified the cause of the disaster, activate your recovery plan. This might involve launching a new instance of your application in a different region, restoring your data from a backup, or both.

•	Test your recovery: Once your application is up and running in the new region, test your recovery to ensure that everything is working as expected.

3.	**Test your recovery plan:** Regularly test your recovery plan to ensure that it will work when you need it. For example, you could schedule a quarterly test where you simulate a disaster scenario and activate your recovery plan.
4.	**Use multiple availability zones:** Use multiple availability zones to ensure that your data and applications are available in case of a disaster. For example, you could use AWS Elastic Load Balancer to distribute traffic across multiple availability zones in the same region.
5.	**Use AWS disaster recovery services:** Use AWS Disaster Recovery to automate the recovery of your applications in case of a disaster. For example, you could use AWS Disaster Recovery to create a replica of your application in a different region.
6.	**Implement monitoring and alerting:** Implement monitoring and alerting to detect and respond to issues before they become major problems. For example, you could use AWS CloudWatch to monitor your application and receive alerts if there are any issues.
7.	**Have a communication plan**: Have a communication plan in place to ensure that you can quickly and effectively communicate with your customers, employees, and other stakeholders in case of a disaster. For example, you could create a contact list of key personnel and stakeholders, and use AWS SNS to send notifications in case of a disaster.
By following these steps, we can create an effective disaster recovery plan that will help us to quickly recover from a disaster and minimize downtime for our customers.


**Documentation**: https://aws.amazon.com/blogs/architecture/disaster-recovery-dr-architecture-on-aws-part-i-strategies-for-recovery-in-the-cloud/ 


