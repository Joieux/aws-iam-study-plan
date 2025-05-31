# Practitioner Level

This section covers the foundational AWS IAM skills required at the Practitioner level. You'll learn how to write and apply IAM policies, understand permission boundaries, and follow best practices for secure access management.

---

## Key Concepts

### IAM Policies

- **Definition:** JSON documents that define permissions for actions on AWS resources.
- **Types:**
  - **Identity-based policies:** Attach to users, groups, or roles.
  - **Resource-based policies:** Attach directly to AWS resources (e.g., S3 buckets).

#### Example Policy

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
Policies can be attached to IAM users, groups, or roles through the AWS Management Console, CLI, or Infrastructure as Code tools.

# Best Practices

Use least privilege: Grant only the permissions required for tasks.
Regularly review and update policies: Remove unnecessary permissions and review assignments.
Prefer managed policies: Use AWS managed policies for easier updates and maintenance.
Enable MFA: Require Multi-Factor Authentication for all users.
Audit IAM resources: Periodically check policy usage and identity access patterns.

# Permission Boundaries

Definition: A managed policy that sets the maximum permissions an identity-based policy can grant to an IAM entity (user or role).
Use Case Example: Restrict what actions a role or user can perform, even if they have broader permissions attached elsewhere.

# Resources

AWS IAM Documentation
AWS Free Tier (for practice)
IAM Policy Simulator
AWS IAM Best Practices
