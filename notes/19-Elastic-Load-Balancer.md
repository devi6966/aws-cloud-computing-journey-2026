# Elastic Load Balancer (ELB)

## What is Elastic Load Balancer?

Elastic Load Balancer (ELB) is a fully managed AWS service that automatically distributes incoming application traffic across multiple EC2 instances to improve availability, scalability, and fault tolerance.

## Why do we need ELB?

* Automatically distributes incoming traffic
* Prevents server overload
* Increases High Availability
* Performs health checks on EC2 instances
* Works with Auto Scaling Group (ASG)

## Types of ELB

* Application Load Balancer (ALB)
* Network Load Balancer (NLB)
* Gateway Load Balancer (GWLB)

## Features

* Automatic traffic distribution
* Health checks
* SSL/TLS termination
* High Availability across multiple Availability Zones
* Fault tolerance
* Integration with Auto Scaling

## Advantages

* Fully managed by AWS
* Improves application availability
* Reduces downtime
* Automatically routes traffic to healthy instances
* Scales with application demand

## Real Life Example

An online shopping website uses an Elastic Load Balancer to distribute customer requests across multiple EC2 instances. If one instance fails, ELB automatically sends traffic only to healthy instances, ensuring uninterrupted service.

## Key Points

* AWS managed Load Balancer service
* Automatically distributes traffic
* Supports High Availability
* Performs health checks
* Works with Auto Scaling Group
* Available in three types: ALB, NLB, and GWLB

## Related Services

* Amazon EC2
* Auto Scaling Group (ASG)
* Amazon CloudWatch
