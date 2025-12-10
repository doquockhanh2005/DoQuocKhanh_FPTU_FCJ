---
title: "Event AWS Cloud Mastery Series #2"
date: 2025-11-17


weight: 1
chapter: false
pre: " <b> 4.3. </b> "
---

## Summary Report: “DevOps on AWS”
## Event Objectives
* Analyze the shift from manual operations (ClickOps) to Infrastructure as Code (IaC) to eliminate human error and inconsistency.
* Master the operational mechanisms of AWS CloudFormation in defining and managing the lifecycle of cloud resources.
* Master AWS CDK (Cloud Development Kit) to build infrastructure using high-level programming languages through Construct levels.
* Gain deep understanding of Docker technology, the application packaging process, and image management with Amazon ECR.
* Compare and select the appropriate Container orchestration solution among Amazon ECS, Amazon EKS, and AWS App Runner.
## Speakers
* **FCJ members**
## Key Highlights
### Infrastructure Mindset & Configuration Management
* Limitations of ClickOps: Operations via the Management Console pose high risks of human error, slow speed, and collaboration difficulties.
* CloudFormation Stack: Manages a collection of resources as a single unit, allowing for the synchronized creation, update, or deletion of the entire infrastructure.
* Drift Detection: A crucial mechanism to identify when actual resource configurations have been manually changed and no longer match the original definition template.
### Infrastructure Programming with AWS CDK
* Multi-language: Supports infrastructure definition using TypeScript, JavaScript, Python, Java, C#/.NET, and Go.
* Constructs System:
  * L1 Constructs: 1:1 mapping with CloudFormation resources (Cfn), requiring detailed configuration.
  * L2 Constructs: Provide optimized defaults and helper methods.
  * L3 Constructs (Patterns): Complete architectural patterns, combining multiple resources to solve a specific problem.
* Workflow: From initialization (cdk init), template synthesis (cdk synth), to deployment (cdk deploy) and destruction (cdk destroy).
### Container Ecosystem & Orchestration
* Docker Fundamentals: Distinguish between Containers (lightweight, shared kernel) and Virtual Machines (heavy, includes Guest OS) and the Build - Push - Pull - Run process.
* Amazon ECR: Secure container image repository, supporting vulnerability scanning and lifecycle policies.
* Orchestration Models:
  * Amazon ECS: AWS-native solution, simple, deeply integrated, supports running on EC2 or Fargate (Serverless).
  * Amazon EKS: Managed Kubernetes service, providing flexibility and open-source standardization but requiring more complex operations.
  * AWS App Runner: PaaS solution enabling rapid web application deployment directly from source code or images without infrastructure management.
## Key Takeaways
### IaC Strategy
* Code over Clicks: Completely shift to the "No More ClickOps" model to ensure consistency and scalability.
* Version Control: Use templates (YAML/JSON) or CDK source code as the single blueprint for infrastructure.
* Change Management: Frequently use cdk diff and Drift Detection to control differences between source code and reality before deployment.
### Technical Architecture
* Immutability: Docker Images and Containers ensure consistent application execution across all environments ("It works on my machine" -> "Ship your machine").
* Compute Selection: Use AWS Fargate to remove server management burdens (Serverless), or EC2 when deep control and cost optimization for long-running tasks are needed.
* Abstraction Levels: Leverage L2/L3 Constructs in CDK to reduce code volume and inherit built-in best practices.
## Application to Projects
* Deploy App Runner: Use for web applications or APIs requiring rapid deployment (prototypes) without wanting to manage servers.
* Optimize ECS: Apply the ECS model combined with Application Load Balancer (ALB) for standard microservices architectures as seen in the "Cats vs Dogs" demo.
* Switch to CDK: Start writing infrastructure in TypeScript/Python instead of raw CloudFormation to accelerate development and code reusability.
## Event Experience
Participating in the “AWS Mastery #2” session provided deep insights into modernizing operations through infrastructure coding and containers. Practical experiences included:
### Learning from Experts
* Understand the core differences between Terraform (multi-platform, uses HCL) and AWS CDK/CloudFormation (optimized for AWS, uses programming languages) to select the appropriate tool.
* Grasp the Construct Tree structure of a CDK application, from App to Stack and Resources.
## Lessons Learned
* Tool Selection: ECS or App Runner are the best choices for teams wanting lower ops overhead, while EKS is for complex requirements and high portability.
* Automation is Mandatory: Integrating CI/CD with CodePipeline and CodeBuild is key to maintaining stability when deploying distributed container architectures.
* Standardization: Using Dockerfile and ECR helps standardize the runtime environment, completely eliminating errors caused by environmental differences.


