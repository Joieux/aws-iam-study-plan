# AWS IAM Study Plan

## Overview

This repository provides a comprehensive, role-based study roadmap to master AWS Identity and Access Management (IAM). The content is organized into four progressive sections—Analyst, Practitioner, Engineer, and Architect—each building on the previous, equipping you with knowledge and practical skills for real-world AWS IAM challenges and certifications.

---

## Table of Contents

- [Section Overviews](#section-overviews)
    - [01. Analyst](#01-analyst)
    - [02. Practitioner](#02-practitioner)
    - [03. Engineer](#03-engineer)
    - [04. Architect](#04-architect)
- [Repository Structure](#repository-structure)
- [Usage Instructions](#usage-instructions)
- [Study Tips](#study-tips)
- [Resources](#resources)
- [Example Questions & Scenarios](#example-questions--scenarios)
- [Contributing](#contributing)

---

## Section Overviews

### 01. Analyst

Builds foundational knowledge of AWS IAM. Focuses on basic concepts, terminology, navigation, and security principles.
- Understand IAM users, groups, roles, and policies
- Learn authentication and authorization basics
- Practice reviewing and interpreting IAM resources

### 02. Practitioner

Introduces hands-on IAM management and everyday best practices for secure AWS environments.
- Create/manage IAM entities (users, groups, roles, policies)
- Implement least privilege, password policies, MFA
- Troubleshoot common IAM issues

### 03. Engineer

Explores advanced IAM features, automation, and scenario-based problem solving.
- Automate IAM with AWS CLI, SDKs, and CloudFormation
- Implement ABAC, service-linked roles, cross-account access
- Analyze permissions, simulate policies, and use resource-based policies

### 04. Architect

Covers design, audit, and governance of IAM at scale for complex organizations.
- Architect multi-account IAM with AWS Organizations & SCPs
- Integrate external IdPs (SAML, OIDC), enforce security/compliance at scale
- Advanced topics: permissions boundaries, session policies, IAM Access Analyzer

---

## Repository Structure
aws-iam-study-plan/ ├── 01-analyst/ │ └── analyst-level.md ├── 02-practitioner/ │ └── practitioner-level.md ├── 03-engineer/ │ └── engineer-level.md ├── 04-architect/ │ └── architect-level.md ├── README.md └── (other supporting files/resources)


---

## Usage Instructions

1. Start with the section that matches your current experience.
2. Work through each section’s materials and exercises.
3. Use the official AWS documentation linked below for deeper study.
4. Try the example questions to check your understanding.

---

## Study Tips

- Practice writing and troubleshooting IAM policies (JSON).
- Use a sandbox AWS account to experiment safely.
- Simulate real-world scenarios, such as cross-account roles or identity federation.
- Regularly review AWS documentation and security whitepapers.

---

## Resources

- [AWS IAM Documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/)
- [AWS Organizations Documentation](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_introduction.html)
- [AWS Security Best Practices](https://d1.awsstatic.com/whitepapers/Security/AWS_Security_Best_Practices.pdf)
- [AWS IAM Policy Simulator](https://policysim.aws.amazon.com)
- [AWS Certified Solutions Architect – Exam Guide](https://aws.amazon.com/certification/certified-solutions-architect-associate/)

---

## Example Questions & Scenarios

1. Write a policy to limit S3 access to specific buckets.
2. Create a role for cross-account Lambda execution.
3. Troubleshoot an IAM user denied access to EC2.
4. Analyze why a federated user can't assume a role.
5. Design an SCP to restrict resource creation to specific regions.

---

## Contributing

Contributions are welcome!
- Open issues for suggestions or corrections.
- Submit pull requests with new scenarios, improved explanations, or additional resources.
- Please follow AWS security and documentation best practices in all examples.

---
