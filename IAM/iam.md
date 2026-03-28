

---

# Part 1 – IAM Important Questions for Exam (CLF-C02)

### 1. What is IAM?

**Answer:**
IAM (Identity and Access Management) is a global AWS service used to securely control access to AWS resources by defining **users, roles, groups, and permissions** using policies.

---

### 2. What are the main components of IAM?

**Answer:**

* Users → individual identities
* Groups → collection of users
* Roles → temporary access identity
* Policies → permission rules in JSON format

---

### 3. What is the Principle of Least Privilege?

**Answer:**
Provide only the minimum permissions required to perform a task.
Improves security and reduces risk of misuse.

Example: Give read-only access instead of full access.

---

### 4. Difference between IAM User and IAM Role

| IAM User                | IAM Role                    |
| ----------------------- | --------------------------- |
| permanent identity      | temporary identity          |
| has password/access key | no permanent credentials    |
| used by person          | used by service/application |
| long-term access        | short-term access           |

---

### 5. What is a Policy in IAM?

Policy is a JSON document that defines:

* Effect → Allow or Deny
* Action → what actions allowed
* Resource → on which resource

Example:
Allow EC2 access or S3 read access.

---

### 6. What is MFA? Why important?

MFA = Multi Factor Authentication.

Login requires:

* password
* OTP from mobile

Provides extra security for AWS accounts.

---

### 7. What is Root account?

Root account is created when AWS account is created.
Has full permissions.

Best practice:

* Do not use root for daily work
* Enable MFA

---

### 8. What are Access Keys?

Used for programmatic access:

* CLI
* SDK
* API

Contains:

* Access key ID
* Secret access key

---

### 9. What is difference between Managed Policy and Inline Policy?

Managed policy:

* reusable
* created once
* attached to multiple users

Inline policy:

* directly attached to one user/group/role
* not reusable

---

### 10. Is IAM regional or global?

IAM is GLOBAL service.

---

# Part 2 – IAM Interview Questions for SDE role (if you mention CLF-C02)

Interviewers usually check whether you **actually understand real usage**.

### Basic Level Questions

### 1. Why do we need IAM?

Expected answer:
To control who can access AWS resources and what actions they can perform securely.

---

### 2. Suppose you have 10 developers who need S3 access. How will you manage permissions?

Expected answer:
Create group → attach S3 policy → add users to group.

Efficient and scalable.

---

### 3. When will you use IAM Role instead of IAM User?

Answer:
When temporary access required.

Examples:

* EC2 accessing S3
* Lambda accessing DynamoDB
* Cross-account access

---

### 4. How EC2 instance can access S3 securely?

Answer:
Create IAM Role with S3 permissions → attach role to EC2 instance.

No need to store access keys.

---

### 5. What happens if policy has both Allow and Deny?

Answer:
Deny always overrides Allow.

(Security concept)

---

### 6. How to give read-only access to S3 bucket?

Answer:
Attach policy with action:
s3:GetObject

---

### 7. How IAM improves security?

Answer:

* least privilege
* MFA
* role-based access
* no sharing credentials

---

# Part 3 – Realistic Interview Scenario Questions

### Scenario 1

Developer accidentally deleted database.

What could be done using IAM?

Answer:
Restrict delete permissions using policy.

---

### Scenario 2

Company wants interns to only view EC2 instances.

Solution:
Create group → attach ReadOnly policy.

---

### Scenario 3

Application running on EC2 needs access to DynamoDB.

Solution:
Attach IAM role to EC2.

---

# Part 4 – How interviewer may ask about CLF-C02

If you say:
"I am AWS Certified Cloud Practitioner"

They may ask:

* Difference between IAM role and user
* What is EC2?
* What is S3?
* What is VPC?
* What is region and availability zone?
* How security managed in AWS?
* Shared responsibility model
* How AWS pricing works
* What is scalability?

They normally DO NOT ask very deep DevOps questions.

---

# Part 5 – Short Revision (1 minute)

IAM controls access to AWS.

Components:

* User → individual login
* Group → collection of users
* Role → temporary access
* Policy → permission JSON

Security:

* least privilege
* MFA
* avoid root usage
* roles for services

IAM is global service.

---

If you want, I can also give:
• EC2 notes (very important)
• S3 notes (most asked in interview)
• Complete CLF-C02 roadmap for SDE interview
• 50 most asked AWS interview questions
