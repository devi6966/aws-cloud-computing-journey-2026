# AWS Security Groups

## What is a Security Group?

A Security Group is a virtual firewall that controls inbound and outbound traffic for an EC2 instance.

## Features

* Works at the instance level.
* Allows only permitted traffic.
* Supports inbound and outbound rules.
* Stateful firewall.

## Inbound Rules

Inbound rules control the incoming traffic to an EC2 instance.

Example:
* Allow SSH (Port 22)
* Allow HTTP (Port 80)
* Allow HTTPS (Port 443)

## Outbound Rules

Outbound rules control the traffic leaving an EC2 instance.

By default, all outbound traffic is allowed.

## Benefits

* Protects EC2 instances
* Controls network access
* Improves security
* Easy to configure

## Real Life Example

A company hosts a website on an EC2 instance. The Security Group allows HTTP (80) and HTTPS (443) traffic for users while allowing SSH (22) access only for the administrator.
