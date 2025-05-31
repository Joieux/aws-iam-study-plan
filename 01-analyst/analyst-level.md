# Analyst Level

Learn IAM basics, auditing tools, and credential management.

---

## Learning Objectives

- Understand AWS IAM core concepts and terminology
- Learn to create and manage IAM users, groups, roles, and policies
- Explore IAM auditing and monitoring tools
- Master credential management best practices

---

## 1. IAM Basics

- What is IAM? Overview and importance in AWS security
- Users, Groups, Roles, and Policies: Definitions and differences
- Policy structure: JSON basics, managed vs. inline policies
- Least privilege principle

**Resources:**
- [AWS IAM Documentation](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)
- [IAM Policy Reference](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_policies.html)

---

## 2. Auditing Tools

- AWS CloudTrail: What it is, how to enable, and how to interpret logs
- IAM Access Analyzer: Basics and use cases
- AWS Config for IAM resources

**Hands-On:**
- Enable CloudTrail in a test AWS account
- Use IAM Access Analyzer to identify overly permissive policies

**Resources:**
- [Monitoring IAM with AWS CloudTrail](https://docs.aws.amazon.com/IAM/latest/UserGuide/logging-using-cloudtrail.html)
- [Access Analyzer Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/what-is-access-analyzer.html)

---

## 3. Credential Management

- Managing long-term vs. short-term credentials
- Best practices for password policies and multi-factor authentication (MFA)
- Using roles and temporary security credentials (STS)
- Detecting and rotating compromised credentials

**Hands-On:**
- Enable MFA for an IAM user
- Create an IAM role and assume it with the AWS CLI

**Resources:**
- [Credential Management Best Practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)
- [AWS STS Overview](https://docs.aws.amazon.com/STS/latest/APIReference/Welcome.html)

---

## 4. Checklist

- [ ] Read core IAM documentation
- [ ] Create IAM users, groups, and roles in a test account
- [ ] Write and attach custom policies
- [ ] Enable and review CloudTrail logs
- [ ] Use IAM Access Analyzer
- [ ] Set up MFA for IAM users
- [ ] Rotate credentials and test temporary access

---

## 5. Further Reading and Practice

- [AWS Identity and Access Management Learning Plan](https://explore.skillbuilder.aws/learning-plan/aws-iam)
- [IAM Tutorials and Labs](https://aws.amazon.com/getting-started/hands-on/iam/)
