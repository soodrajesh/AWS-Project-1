**AWS-Project-1**

**Description**:  This project contains cloudformation templates to deploy a VPC with 3 public, 3 private and 3 DB subnets spread across three Availability Zones. It deploys an internet gateway, with a default route on the public subnets. It deploys NAT gateways and default routes for them in the private subnets.
The applicaton is based on ECS Fargate cluster and DB is Aurora Postgres. All the transaction logs are stored in S3 bucket. 

**Step 1:** Deploy VPC-3AZ.yaml

**Step 2:** Deploy ECS.yaml

**Step 3:** Deploy RDS.yaml

**Step 4:** Deploy S3.yaml

![arch1](https://user-images.githubusercontent.com/103620921/169332190-1b77ab21-5bfa-4933-a6fb-f9fa6a94b28b.JPG)



**Disaster Recovery Plan (High Level)**
A resilient workload helps to prepare for disaster events, which is one of the biggest challenges one can face. 
Such events include natural disasters like earthquakes or floods, technical failures such as power or network loss, and human actions such as inadvertent or unauthorized modifications.

**Multi-Region strategy:**

AWS provides multiple resources to enable a multi-Region approach for our workload. This provides business assurance against events of sufficient scope that can impact multiple data centers across separate and distinct locations. In this example, I am using a multi-Region approach to demonstrate DR strategies. But, we can also use these for Multi-AZ strategies or hybrid (on-premises workload/cloud recovery) strategies.

**Documentation**: https://aws.amazon.com/blogs/architecture/disaster-recovery-dr-architecture-on-aws-part-i-strategies-for-recovery-in-the-cloud/ 

![DR](https://user-images.githubusercontent.com/103620921/169332126-6a71b07f-2734-47e7-9037-e0428c9c2adb.JPG)
