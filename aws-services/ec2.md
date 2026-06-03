# EC2 (Elastic Compute Cloud)

## What is EC2?

Amazon Elastic Compute Cloud (EC2) provides resizable compute capacity in the cloud.

With EC2, you can launch virtual servers called instances and choose the CPU, memory, storage, and networking you need.

EC2 is often used for application hosting, batch processing, development environments, and more.

---

## Main Components

### Instances

An EC2 instance is a virtual server that runs applications in the AWS cloud.

Instances come in different families and sizes to match workloads like general purpose, compute optimized, memory optimized, and storage optimized.

Each instance type defines:

* CPU cores
* Memory
* Network performance
* Storage options

---

### Amazon Machine Images (AMIs)

An AMI is a template for launching instances.

It includes:

* Operating system
* Application server
* Applications and configuration

You can use AWS-managed AMIs, community AMIs, or create custom AMIs for consistent deployments.

---

### Elastic Block Store (EBS)

Amazon EBS provides persistent block storage for EC2 instances.

EBS volumes attach to instances and remain available even after the instance stops.

Types include:

* General Purpose SSD (gp3/gp2)
* Provisioned IOPS SSD (io2/io2 Block Express)
* Throughput Optimized HDD (st1)
* Cold HDD (sc1)

---

### Security Groups

Security groups act as virtual firewalls for EC2 instances.

They control inbound and outbound traffic at the instance level using rules.

Key points:

* Stateful traffic filtering
* Rules allow traffic by protocol, port, and source/destination
* Multiple instances can share the same security group

---

### Key Pairs

A key pair is used to securely connect to Linux EC2 instances.

The public key is stored in AWS, and the private key is kept by the user.

Use the private key with SSH to access instances.

---


## Security Best Practices

### Use the Principle of Least Privilege

Grant only the permissions required to manage or operate EC2 resources.

Example:

If a role only needs to start and stop instances, do not grant permissions to terminate or create security groups.

---

### Use IAM Roles for EC2

Assign IAM roles to EC2 instances instead of embedding access keys.

This provides temporary credentials and reduces exposure of sensitive keys.

---

### Protect Instance Access

Use security groups and network ACLs to restrict traffic.

Enable SSH access only from trusted IP addresses, and use key pairs or Session Manager where possible.

---

### Use Monitoring and Logging

Enable Amazon CloudWatch for metrics and Amazon CloudTrail for API activity.

Monitor instance health, CPU usage, disk I/O, and network traffic.

---

## Common Use Cases

* Hosting web applications
* Running batch jobs and compute workloads
* Development and testing environments
* Data processing and analytics
* Migrating on-premises servers to the cloud

---

## Related Services

* Amazon VPC
* Amazon S3
* AWS IAM
* Amazon RDS
* AWS Auto Scaling

EC2 is often used together with VPC for networking and IAM for access control.

---

## Tips

* Choose the right instance type for your workload.
* Use EBS volumes for persistent storage.
* Use security groups to protect instances.
* Prefer IAM roles instead of access keys.
* Use CloudWatch to monitor performance.
* Stop or terminate unused instances to control costs.

---

## Quick Summary

| Component       | Purpose                                                       |
| --------------- | ------------------------------------------------------------- |
| Instance        | Virtual server in AWS                                          |
| AMI             | Template for launching EC2 instances                           |
| EBS             | Persistent block storage for instances                        |
| Security Group  | Virtual firewall for instance traffic                         |
| Key Pair        | SSH authentication for Linux instances                         |


### Key Takeaways

* EC2 provides resizable compute capacity in the cloud.
* Use AMIs to standardize instance deployments.
* EBS provides persistent storage for instances.
* Security groups control instance traffic.
* IAM roles are best for EC2 instance permissions.
* Monitoring and logging improve reliability and security.
* Select instance types based on workload needs.
