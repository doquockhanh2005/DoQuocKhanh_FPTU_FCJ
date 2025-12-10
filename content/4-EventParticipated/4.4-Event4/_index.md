---
title: "Event AWS Cloud Mastery Series #3"
date: 2025-11-29


weight: 1
chapter: false
pre: " <b> 4.4. </b> "
---
# Summary Report: “Identity & Access Management”
## Event Objectives
* Understand IAM concepts, credential management, and AWS Organization structure.
* Master the threat detection system with GuardDuty and the Detection-as-Code mindset.
* Design a Layered Security network architecture and implement an optimized Network Firewall.
* Gain deep understanding of data encryption mechanisms with AWS KMS (Key Management Service): The difference between AWS Managed Keys and Customer Managed Keys (CMK).
* Apply automated traffic filtering strategies (Automated Domain Lists) to block emerging threats.
## Speakers
* **FCJ members**
## Key Highlights
### Identity & Access Management (IAM)
* Principles: Eliminate long-term Access Keys; use short-term credentials via IAM Identity Center.
* Controls: Combine SCPs (blocking permissions at the organization level) and Permission Boundaries (limiting permissions at the user level).
* Automation: Automatically rotate DB passwords with Secrets Manager.
### Detection & Response
* GuardDuty: Real-time monitoring (Runtime Monitoring) to detect anomalous behavior deep within the OS (processes, file access).
* Detection-as-Code: Manage detection rules as code (CloudFormation/Terraform) to ensure consistency and compliance.
### Network Security
* Layered Security: Combine WAF (Layer 7) -> Network Firewall (Layer 3-7) -> NACL (Subnet) -> Security Group (Instance).
* Network Firewall:
  * Use Active Threat Defense to automatically update blocking rules against the latest threats from AWS Threat Intelligence.
  * Automated Domain Lists feature: Automatically analyze HTTP/HTTPS traffic to create blocking or allowing rules based on domain names (FQDN) without manual IP management.
### Data Protection
* KMS Mechanism:
  * KMS manages the Master Key (never leaves KMS).
  * The Master Key is used to encrypt the Data Key.
  * The Data Key (plaintext) is what actually encrypts user data.
* Key Classification:
  * AWS Managed Key: Free, managed by AWS; users cannot manually rotate or change policies.
  * Customer Managed Key (CMK): Paid; users have full control (rotation, permissions, deletion); mandatory for high compliance requirements.
  * EBS Encryption: The process of encrypting EBS volumes involves creating a Data Key, encrypting the volume with that Data Key, and storing the encrypted Data Key with the volume.
## Key Takeaways
### Data Protection Strategy
* Use CMK for sensitive data: Although AWS Managed Keys are convenient, CMKs allow tighter control over who can use the key for decryption (via Key Policy).
* Key Rotation: Enable automatic key rotation every year (for CMK) to ensure safety if an old key is compromised.
### Technical Architecture
* Optimize Network Costs: Use the Multiple VPC Endpoints model for Network Firewall to reduce operational costs and simplify network architecture.
* Security Group Reference: Instead of whitelisting hardcoded IPs in Security Groups, reference the SG IDs of other tiers (e.g., SG-App only allows traffic from SG-Web) for greater flexibility.
## Application to Projects
#### Improve Identity Management (IAM)
* Audit & Clean-up: Review all IAM Users in the project; delete old/unused Access Keys. Mandate MFA activation (preferably FIDO2/YubiKey) for all accounts.
* Implement Secrets Manager: Replace environment variables containing DB passwords in code (e.g., Spring Boot/Node.js) with code that calls the API to retrieve secrets from AWS Secrets Manager.
#### Enhance Network Security
* Egress Filtering: Deploy AWS Network Firewall or DNS Firewall to control traffic from servers to the Internet, blocking connections to strange domains or C2 servers.
* Review Security Groups: Convert rules currently using static IPs to use Security Group Referencing to better support Auto Scaling.
#### Monitoring & Automated Response
* Activate GuardDuty: Enable GuardDuty in the Production environment to immediately detect anomalous behaviors (like crypto mining, port scanning).
* Automated Remediation: Write a simple Lambda function connected to EventBridge: When GuardDuty reports a "High" severity issue, automatically revoke session tokens or block the Security Group of that instance.
## Event Experience
Participating in "AWS Mastery #3" helped me systematize all security layers on AWS. As a developer who usually focuses on code rather than infrastructure, this event truly changed my mindset regarding security responsibilities:
#### Changing the mindset on "Clean Code"
* Previously, I thought not hardcoding passwords was enough. But seeing the IAM Access Analyzer demo, I realized that writing Infrastructure-as-Code (Terraform/CloudFormation) also needs to be "linted" (checked for errors) for security logic. A single accidental Principal: * line in the code can throw the doors open for hackers, and this tool acts like a "Unit Test" for policies.
#### Mélofee Malware Analysis
* Seeing the wget http://173.209... command connecting directly to an IP instead of a domain was a "wake-up call." I used to think just blocking DNS was safe, but real malware is much smarter. This proves why Network Firewall (blocking IP egress) is so critical for backend servers.
#### The "Cost" Lesson
* A small but expensive detail the speaker shared: The Free Tier account immediately expires upon joining an AWS Organization. This is extremely useful information for Devs who use personal accounts for tinkering, helping to avoid "out of the blue" bills.

