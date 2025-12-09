---
title: "Week 2 Worklog"
date: 2024-09-21


weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---
{{% notice warning %}} 
⚠️ **Note:** The following information is for reference purposes only. Please **do not copy verbatim** for your own report, including this warning.
{{% /notice %}}


### Week 2 Objectives:

* Understanding of AWS network architecture: VPC, Subnets, Route Tables.
* Understand network security mechanisms: Security Groups vs. NACLs.
* Practice building a Custom VPC instead of using the default one

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Learn about AWS Virtual Private Cloud, Regions and Availability Zones (AZ) <br> - Understand CIDR Blocks and IP addressing/subnetting| 15/09/2025 | 15/09/2025|
| 3   | - Learn about Subnets (Public/Private), Route Tables, Internet Gateway (IGW) <br> - Learn about NAT Gateway (enabling internet access for Private subnets) | 16/09/2025 | 16/09/2025      | <https://cloudjourney.awsstudygroup.com/> |
| 4   | **Practice:** Create a Custom VPC, create 2 Subnets (1 Public, 1 Private), attach an Internet Gateway | 17/09/2025 | 17/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| 5   | - Distinguish between Security Groups (Stateful) and Network ACLs (Stateless) <br> - Configure basic Inbound/Outbound rules (SSH, HTTP) | 18/09/2025 | 18/09/2025 | <https://cloudjourney.awsstudygroup.com/> |
| 6   | - **Practice:** Finalize the 2-tier VPC model. Test network connectivity between subnets and to the internet. | 19/09/2025 | 19/09/2025 | <https://cloudjourney.awsstudygroup.com/> |


### Week 2 Achievements:

* Clearly understood packet traffic flow within a VPC environment.

* Successfully built a secure VPC architecture including: a Public Subnet (for Web Server) and a Private Subnet (for future Database).
  
* Learned how to configure Security Groups to open only necessary ports (Principle of Least Privilege).
