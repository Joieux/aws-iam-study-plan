# Architect Level (AWS IAM)

## Overview

Achieving architect-level expertise in AWS Identity and Access Management (IAM) means mastering how to design, implement, and manage IAM at scale across complex, multi-account AWS environments. You'll be expected to make security decisions that impact entire organizations, implement best practices, and support business needs while maintaining strong security controls.

---

## Core Architect-Level IAM Domains

### 1. IAM Design at Scale

- **Multi-Account Strategy:** Understand AWS Organizations, account structures, and security boundaries.
- **Principle of Least Privilege:** Apply least privilege across users, roles, and services at scale.
- **Delegated Administration:** Use cross-account roles and resource-based policies for scalable management.

### 2. Service Control Policies (SCPs)

- **What Are SCPs:** Policies in AWS Organizations that set permission boundaries for all accounts.
- **Best Practices:**
  - Start with a Deny List SCP and add exceptions.
  - Use `FullAWSAccess` as a baseline, then restrict.
  - Test SCPs in a sandbox before deploying widely.
- **Example Use Cases:** Prevent deletion of critical resources, enforce encryption, restrict regions.

### 3. Attribute-Based Access Control (ABAC)

- **Definition:** Grant permissions based on user attributes (tags) rather than static roles.
- **Benefits:** Scales better than RBAC in large environments.
- **Implementation Steps:**
  - Tag resources and identities consistently.
  - Write policies using `${aws:PrincipalTag/...}` and `${aws:ResourceTag/...}` variables.
- **Example:** Allow developers tagged `Department=Dev` to access only `Department=Dev` resources.

### 4. Cross-Account Access

- **Cross-Account Roles:** Grant access between AWS accounts via `sts:AssumeRole`.
- **Resource-Based Policies:** Apply policies directly to resources (S3, Lambda, KMS, etc.).
- **Best Practices:**
  - Use external IDs for third-party access.
  - Log all cross-account activity with CloudTrail.

### 5. Identity Federation

- **SAML 2.0 and OIDC:** Integrate external identity providers (AD, Okta, Google Workspace).
- **Temporary Credentials:** Use federation for least-privilege, short-term access.
- **Best Practices:** Enforce strong authentication (MFA), audit access patterns.

### 6. Advanced IAM Features for Architects

- **Permissions Boundaries:** Delegate role creation safely.
- **Session Policies:** Apply additional restrictions during session creation.
- **Policy Evaluation Logic:** Master policy merging, explicit deny, and evaluation order.
- **IAM Access Analyzer:** Detect unintended access paths.

---

## AWS Certified Solutions Architect Exam Alignment

- **Domains Covered:**
  - Design secure access to AWS resources
  - Design cost-optimized and resilient architectures
  - Implement monitoring and logging for IAM
- **Key Skills:**
  - Write and evaluate complex IAM policies
  - Architect for least privilege and compliance
  - Troubleshoot permission issues at scale

---

## Study Tips

- Practice writing and analyzing IAM policies in JSON.
- Use AWS Organizations and SCPs in a sandbox account.
- Simulate real-world scenarios (cross-account, federated access).
- Explore IAM Access Analyzer findings and resolve unintended access.
- Review AWS documentation and whitepapers on IAM, Organizations, and Security Best Practices.

---

## Resources

- [AWS IAM Documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/)
- [AWS Organizations Documentation](https://docs.aws.amazon.com/organizations/latest/userguide/orgs_introduction.html)
- [AWS Security Best Practices](https://d1.awsstatic.com/whitepapers/Security/AWS_Security_Best_Practices.pdf)
- [AWS IAM Policy Simulator](https://policysim.aws.amazon.com)
- [AWS Certified Solutions Architect – Exam Guide](https://aws.amazon.com/certification/certified-solutions-architect-associate/)

---

## Example Questions & Scenarios

1. Write an SCP that prevents the use of unapproved AWS regions.
2. Design an ABAC policy for project-based resource access.
3. Troubleshoot why a federated user cannot assume a role in another account.
4. Analyze Access Analyzer findings for unintended public S3 access.

---
