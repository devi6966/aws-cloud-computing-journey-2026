# Auto Scaling Group (ASG)

## What is Auto Scaling Group?

Auto Scaling Group (ASG) is an AWS service that automatically launches or terminates EC2 instances based on application demand to maintain performance, availability, and cost efficiency.

## Why do we need ASG?

* Automatically increases or decreases EC2 instances
* Maintains High Availability
* Reduces infrastructure cost
* Replaces unhealthy EC2 instances automatically

## Key Components

* Minimum Capacity
* Desired Capacity
* Maximum Capacity
* Launch Template
* Scaling Policy

## Features

* Automatic Scaling
* Health Checks
* Fault Tolerance
* Cost Optimization
* Integration with ELB

## Scaling Types

### Scale Out
Adds more EC2 instances when traffic increases.

### Scale In
Removes EC2 instances when traffic decreases.

## Advantages

* High Availability
* Better Performance
* Automatic Recovery
* Cost Saving
* Fully Managed by AWS

## Real Life Example

During Amazon's Great Indian Festival, traffic increases significantly. Auto Scaling Group automatically launches additional EC2 instances to handle the load. When the sale ends, it terminates the extra instances, reducing costs.

## Key Points

* Automatically manages EC2 instances
* Uses Launch Template
* Supports Scale Out and Scale In
* Maintains Optimal Capacity
* Works together with Elastic Load Balancer (ELB)

## Related Services

* Amazon EC2
* Elastic Load Balancer (ELB)
* Launch Template
* Amazon CloudWatch
