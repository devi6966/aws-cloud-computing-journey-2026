# Amazon Elastic Block Store (EBS)

## What is Amazon EBS?

Amazon Elastic Block Store (EBS) is a block storage service provided by AWS for Amazon EC2 instances. It stores operating systems, applications, and data with persistent storage.

## Features

* Block-level storage
* Persistent storage
* Can be attached to EC2 instances
* Supports snapshots for backup
* High availability within an Availability Zone

## Advantages

* High performance
* Reliable and durable
* Easy to resize
* Data remains available even after stopping an EC2 instance
* Supports backup and recovery

## Use Cases

* Operating system storage
* Databases
* Enterprise applications
* Boot volumes for EC2 instances

## Limitations

* Can be attached only within the same Availability Zone.
* Cannot be shared simultaneously by multiple EC2 instances (except Multi-Attach supported volumes).

## Real Life Example

A company hosts its website on an EC2 instance. The operating system, application files, and database are stored on an EBS volume. Even if the EC2 instance is stopped, the data remains stored in the EBS volume.

## Key Points

* EBS = Elastic Block Store
* Storage Type = Block Storage
* Works mainly with EC2
* Persistent Storage
* Supports Snapshots
