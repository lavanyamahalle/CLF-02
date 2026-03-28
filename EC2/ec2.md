

# AWS EC2 (Elastic Compute Cloud) – Notes

## 1. What is EC2?

**EC2 (Elastic Compute Cloud)** provides **virtual servers** in the cloud.

It allows you to:

* run applications
* host websites
* deploy backend services
* run databases
* perform computing tasks

👉 EC2 = computer on cloud

Example:
Instead of buying physical server → use EC2.

---

## 2. Key Features of EC2

### A. On-demand computing

Launch server whenever needed.

### B. Scalable

Increase or decrease resources.

### C. Pay as you use

Only pay for running time.

### D. Secure

Integrated with IAM and security groups.

---

## 3. EC2 Instance

EC2 instance = virtual machine.

Includes:

* CPU
* RAM
* Storage
* Operating system

Example OS:

* Linux
* Windows
* Ubuntu

---

## 4. AMI (Amazon Machine Image)

AMI is a **template** used to create EC2 instance.

Contains:

* operating system
* application software
* configuration

Example:
Ubuntu AMI
Windows AMI

---

## 5. Instance Types

Different instance types based on performance.

Examples:

### General Purpose

Balanced CPU and RAM.
Example:
t2.micro

---

### Compute Optimized

High CPU power.

Example:
c5

---

### Memory Optimized

High RAM.

Example:
r5

---

### Storage Optimized

High disk performance.

Example:
i3

---

## 6. Security Group

Security group acts like **firewall**.

Controls:

* incoming traffic
* outgoing traffic

Example rules:
Allow:

* HTTP → port 80
* HTTPS → port 443
* SSH → port 22

---

## 7. Key Pair

Used for secure login to EC2 instance.

Contains:

* public key
* private key

Private key used while connecting.

Example:
.pem file

---

## 8. Connect to EC2

### Linux

Use SSH:

```bash id="t1qvau"
ssh -i key.pem ec2-user@public-ip
```

---

### Windows

Use RDP.

---

## 9. Pricing Types (Important for exam)

### On-Demand

Pay per use.
Flexible.

---

### Reserved Instances

Commit for 1 or 3 years.
Cheaper.

---

### Spot Instances

Very cheap.
Can be stopped anytime by AWS.

---

### Dedicated Hosts

Physical server reserved.

---

## 10. EC2 Storage

### EBS (Elastic Block Store)

Storage attached to EC2.

Persistent storage.

Data not lost when instance stops.

---

### Instance Store

Temporary storage.

Data lost when instance stops.

---

## 11. Regions and Availability Zones

Region:
geographical area.

Example:
Mumbai region.

Availability Zone:
data centers inside region.

Example:
ap-south-1a
ap-south-1b

High availability.

---

## Important Exam Questions (EC2)

### 1. What is EC2?

Virtual server in AWS cloud.

---

### 2. What is AMI?

Template used to launch EC2 instance.

---

### 3. What is security group?

Firewall controlling traffic.

---

### 4. Difference between EBS and Instance store?

EBS:
persistent storage

Instance store:
temporary storage

---

### 5. Which port used for SSH?

22

---

### 6. Which port used for HTTP?

80

---

### 7. Which pricing model cheapest?

Spot instance.

---

### 8. Can we stop EC2 instance?

Yes.

---

## Interview Questions (SDE level)

### 1. Why use EC2 instead of local server?

Scalable and cost effective.

---

### 2. How to securely connect EC2?

Using key pair and security group.

---

### 3. How EC2 connects to S3?

Using IAM role.

---

### 4. What happens when EC2 stopped?

Compute stops.
EBS data remains.

---

### 5. Difference between stop and terminate?

Stop:
can restart later

Terminate:
deleted permanently

---

### 6. How to make application highly available?

Deploy EC2 in multiple availability zones.

---

## Real-life Scenario Questions

### Scenario 1

Website traffic increased suddenly.

Solution:
Scale EC2 instance.

---

### Scenario 2

Developer cannot connect to EC2.

Check:
security group port 22 open or not.

---

### Scenario 3

Need cheap compute for testing.

Use:
spot instance.

---

# Quick Revision (1 minute)

EC2 provides virtual servers.

Important terms:

* AMI → template
* security group → firewall
* key pair → login
* EBS → storage
* spot instance → cheapest
* IAM role → permissions

Ports:
22 SSH
80 HTTP
443 HTTPS

---

If you want, I can also give:
• S3 notes (most asked in interview)
• VPC notes
• Shared responsibility model
• AWS full revision cheat sheet
• 50 AWS interview questions for SDE
