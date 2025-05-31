# Practitioner Level

This section covers the foundational AWS IAM (Identity and Access Management) skills required at the Practitioner level. You’ll learn how to write and apply IAM policies, understand permission boundaries, and follow best practices for secure AWS resource management.

---

## Table of Contents

1. [Key Concepts](#key-concepts)
2. [IAM Policies](#iam-policies)
    - [Types of Policies](#types-of-policies)
    - [Example Policy](#example-policy)
    - [Applying Policies](#applying-policies)
3. [Best Practices](#best-practices)
4. [Permission Boundaries](#permission-boundaries)
5. [Common Mistakes to Avoid](#common-mistakes-to-avoid)
6. [Practice Exercises](#practice-exercises)
7. [Glossary](#glossary)
8. [Resources](#resources)

---

## Key Concepts

- **IAM User:** An entity that represents a person or service that interacts with AWS.
- **IAM Group:** A collection of users managed as a unit.
- **IAM Role:** An AWS identity with specific permissions.
- **IAM Policy:** A document that defines permissions.

---

## IAM Policies

IAM policies are at the heart of AWS security. They define what actions are allowed or denied for which AWS resources.

### Types of Policies

| Policy Type             | Attached To                 | Example Use Case                                   |
|-------------------------|----------------------------|----------------------------------------------------|
| Identity-based Policy   | Users, Groups, Roles       | Grant S3 access to a developer group               |
| Resource-based Policy   | Resources (e.g. S3 bucket) | Allow another account to access an S3 bucket       |
| Permissions Boundary    | Users, Roles               | Limit maximum permissions a role can have          |
| AWS Organizations SCPs  | Accounts, OUs              | Restrict services that child accounts can use      |
| Session Policies        | Temporary Credentials      | Further restrict permissions during a session      |

### Example Policy

A simple policy to allow listing an S3 bucket:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:ListBucket",
      "Resource": "arn:aws:s3:::example_bucket"
    }
  ]
}
# Applying Policies

Policies can be attached to IAM users, groups, or roles through various methods:
- **AWS Management Console:** Use the web interface to attach policies directly to identities.
- **AWS CLI:** Example command:
  ```bash
  aws iam attach-user-policy --user-name <username> --policy-arn <policy-arn>
Infrastructure as Code Tools: For example, use AWS CloudFormation or Terraform to define and attach policies programmatically.
Real-World Scenario:
Suppose your organization wants only the DevOps group to manage EC2 instances. You would create an identity-based policy granting ec2:* actions and attach it to the DevOps group.

# Best Practices

Use least privilege: Grant only the permissions required for tasks.
Regularly review and update policies: Remove unnecessary permissions and review assignments.
Prefer managed policies: Use AWS managed policies for easier updates and maintenance.
Enable MFA: Require Multi-Factor Authentication for all users.
Audit IAM resources: Periodically check policy usage and identity access patterns.
Document policy intent: Add descriptions to custom policies and keep change logs.

# Permission Boundaries

A permission boundary is a managed policy that defines the maximum permissions an identity-based policy can grant to an IAM entity (user or role).

# Use Case Example:

A developer is granted a role that allows creating EC2 instances. A permission boundary is set to prevent launching instances of certain types or in certain regions, even if the main policy would otherwise allow it.

# Visual Diagram:

Mermaid
graph TD
    Policy[Identity Policy] -->|Permissions| User
    Boundary[Permission Boundary] -->|Restricts| User
    User((User or Role))
    User -->|Effective Permissions = Policy ∩ Boundary| AWS

# Common Mistakes to Avoid

Granting broad permissions such as *:* (all actions, all resources).
Not removing or disabling unused IAM users/roles.
Failing to enable MFA for privileged accounts.
Over-relying on inline policies instead of managed policies.
Not auditing policy changes and usage.

# Practice Exercises
1. Write a policy: Allow a user to read objects in a specific S3 bucket only.
2. Apply a permission boundary: Restrict a role so it cannot delete resources, even if other policies would allow it.
3. Audit: Use the IAM Access Analyzer to find resources shared with external accounts.
4. Scenario: A user needs full access to CloudWatch but only read access to S3. Draft the policies required.

#Glossary

Action: An operation that can be performed on an AWS resource (e.g., s3:PutObject).
Effect: Whether the policy allows or denies access (Allow or Deny).
Resource: The AWS object the action applies to (e.g., a bucket ARN).
Principal: The user, role, or service making the request.
Statement: An individual permission block in a policy.
ARN: Amazon Resource Name, uniquely identifies AWS resources.

# Resources
AWS IAM Documentation
AWS Free Tier (for practice)
IAM Policy Simulator
AWS IAM Best Practices
AWS Identity and Access Management Workshop
