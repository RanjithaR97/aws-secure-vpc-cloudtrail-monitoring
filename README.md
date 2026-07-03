# aws-secure-vpc-cloudtrail-monitoring
Secure AWS network infrastructure using Amazon VPC, EC2, CloudTrail, and Amazon SNS with monitoring, audit logging, and network isolation.

# Secure VPC Infrastructure with Amazon VPC, EC2, CloudTrail & Amazon SNS

## Project Overview

This project demonstrates how to build a secure AWS network infrastructure using Amazon VPC. A custom Virtual Private Cloud (VPC) was created with public and private subnets, an Amazon EC2 instance was deployed within the VPC, routing components were configured, AWS CloudTrail was enabled to track account activity and API calls, and Amazon SNS was configured to send notifications for security-related events. The project focuses on implementing secure networking, monitoring, and audit logging in AWS.

---

## Objective

Design and deploy a secure AWS network environment with proper network isolation, monitoring, and activity tracking using Amazon VPC, Amazon EC2, AWS CloudTrail, and Amazon SNS.

---

## AWS Services Used

* Amazon VPC
* Amazon EC2
* AWS CloudTrail
* Amazon SNS
* Internet Gateway
* Route Tables
* Security Groups

---

## Key Features

* Custom Amazon VPC configuration
* Public and Private Subnets
* Secure EC2 deployment inside the VPC
* Internet Gateway configuration
* Route Table configuration
* Security Group implementation
* AWS CloudTrail audit logging
* Amazon SNS notifications
* Secure and isolated network architecture

---

## Prerequisites

* AWS Account
* IAM User with appropriate permissions
* Amazon EC2 Key Pair
* Basic understanding of AWS Networking
* Basic Linux knowledge

---

## Architecture

```text
                           Internet
                               │
                               ▼
                       Internet Gateway
                               │
        ┌────────────────────────────────────┐
        │          Amazon VPC                │
        │                                    │
        │   ┌──────────────┐                 │
        │   │ Public Subnet│                 │
        │   │              │                 │
        │   │ EC2 Instance │                 │
        │   └──────────────┘                 │
        │                                    │
        │   ┌──────────────┐                 │
        │   │Private Subnet│                 │
        │   │ Future Resources│              │
        │   └──────────────┘                 │
        └────────────────────────────────────┘
                 │
                 ▼
          Security Groups
                 │
                 ▼
          AWS CloudTrail
                 │
                 ▼
            Amazon SNS
```

---

## Implementation Steps

### Step 1: Create a Custom Amazon VPC

* Created a custom Amazon VPC.
* Configured an IPv4 CIDR block.
* Enabled DNS Resolution and DNS Hostnames.

---

### Step 2: Create Public and Private Subnets

* Created a Public Subnet.
* Created a Private Subnet.
* Placed both subnets in the desired Availability Zone.
* Assigned appropriate CIDR blocks.

---

### Step 3: Launch an Amazon EC2 Instance

* Launched an Amazon EC2 instance inside the Public Subnet.
* Selected the Amazon Linux AMI.
* Configured the required Security Group.
* Connected to the instance using SSH.

---

### Step 4: Configure Internet Gateway

* Created an Internet Gateway.
* Attached the Internet Gateway to the custom VPC.
* Enabled internet access for resources in the Public Subnet.

---

### Step 5: Configure Route Tables

* Created Public and Private Route Tables.
* Associated the Public Route Table with the Public Subnet.
* Associated the Private Route Table with the Private Subnet.
* Added the default route (0.0.0.0/0) to the Internet Gateway for the Public Route Table.

---

### Step 6: Configure Security Groups

* Allowed SSH (Port 22) access.
* Allowed HTTP (Port 80) access.
* Restricted unnecessary inbound traffic.
* Configured outbound rules as required.

---

### Step 7: Enable AWS CloudTrail

* Created a CloudTrail Trail.
* Enabled logging for Management Events.
* Configured log storage.
* Verified Event History.
* Monitored AWS API activity.

---

### Step 8: Configure Amazon SNS

* Created an SNS Topic.
* Added an Email Subscription.
* Confirmed the subscription.
* Configured notifications for security-related events.

---

## Testing

The following validations were performed:

* Verified successful VPC creation.
* Verified Public and Private Subnets.
* Confirmed Internet Gateway attachment.
* Verified Route Table associations.
* Successfully launched the EC2 instance.
* Confirmed internet connectivity.
* Verified Security Group rules.
* Verified CloudTrail event logging.
* Confirmed SNS email notification delivery.

---

## Project Outcome

Successfully designed and deployed a secure AWS networking environment using Amazon VPC. Implemented secure network isolation through Public and Private Subnets, configured routing using Route Tables and an Internet Gateway, enabled AWS CloudTrail for auditing account activity, and configured Amazon SNS for security notifications. The project demonstrates core AWS networking, security, and monitoring concepts.

---

## Folder Structure

```text
aws-secure-vpc-infrastructure/
│
├── README.md
├── architecture/
│   └── architecture-diagram.png
│
├── screenshots/
│   ├── 01-VPCCreation.png
│   ├── 02-EC2LaunchInVPC.png
│   ├── 03-ConfigureRouteTables.png
│   ├── 04-EnableCloudTrail.png
│   ├── 05-SNSSetUp.png
│   ├── 06-CloudtrailOutput.png
│


---

## Screenshots

output screenshots all uploaded in screenshot folder

---

## Skills Demonstrated

* Amazon VPC
* Amazon EC2
* AWS CloudTrail
* Amazon SNS
* Internet Gateway
* Route Tables
* Security Groups
* AWS Networking
* Network Security
* Monitoring and Audit Logging

---

## Learning Outcomes

* Designed a secure Virtual Private Cloud (VPC).
* Configured Public and Private Subnets.
* Implemented Internet Gateway and Route Tables.
* Deployed an EC2 instance within a custom VPC.
* Configured Security Groups for controlled network access.
* Enabled AWS CloudTrail for monitoring API activity.
* Configured Amazon SNS for automated security notifications.
* Gained hands-on experience with AWS networking and security best practices.

---



