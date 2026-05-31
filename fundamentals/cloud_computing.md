# Cloud Computing

## What is Cloud Computing?

Cloud computing is the on-demand delivery of computing resources over the internet. Instead of buying and maintaining physical infrastructure, users can access resources when needed and pay only for what they use.

### Service Models

#### IaaS (Infrastructure as a Service)

Provides virtualized computing resources such as servers, storage, and networking.

Examples:

* Amazon EC2
* Amazon S3

#### PaaS (Platform as a Service)

Provides a platform for developing, running, and managing applications without worrying about the underlying infrastructure.

Examples:

* AWS Elastic Beanstalk
* AWS Lambda

#### SaaS (Software as a Service)

Provides ready-to-use software over the internet.

Examples:

* Gmail
* Microsoft 365
* Salesforce

---

## Characteristics of Cloud Computing

* On-demand self-service
* Broad network access
* Resource pooling
* Rapid elasticity
* Pay-as-you-go pricing

---

## Benefits

* Reduced costs and less waste
* Faster deployment and innovation
* Global scale and flexibility
* Strong security and disaster recovery
* High availability and reliability

---

## AWS Regions

AWS has Regions all around the world.

A Region is a geographic area that contains multiple Availability Zones.

Factors when choosing a Region:

* Compliance requirements
* Lower latency (closer to users)
* Service availability
* Pricing differences between Regions

---

## Availability Zones (AZs)

Each AWS Region contains multiple Availability Zones, minimum of three.

An Availability Zone consists of one or more data centers with redundant power, networking, and connectivity.

Availability Zones are connected through high-speed, low-latency networks.

Benefits:

* High availability
* Fault tolerance
* Disaster recovery

---

## Edge Locations

Edge Locations are sites located closer to end users.

They are used by services such as Amazon CloudFront to cache content and deliver it faster.

Benefits:

* Lower latency
* Faster content delivery
* Better user experience

Example:
If a user in São Paulo accesses a website hosted in the United States, CloudFront can serve cached content from a nearby Edge Location instead of retrieving it from the original server every time.

---
