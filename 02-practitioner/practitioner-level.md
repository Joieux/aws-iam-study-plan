# Practitioner Level

This section covers the foundational IAM skills required at the AWS Practitioner level. You’ll learn how to write and apply IAM policies, and understand permission boundaries.

---

## Key Concepts

### IAM Policies

- **Definition:** Documents that define permissions for actions on AWS resources.
- **Types:** 
  - Identity-based policies (attach to users, groups, or roles)
  - Resource-based policies (attach directly to resources)
- **Example Policy:**
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
  Applying Policies
How to Attach: Policies can be attached to IAM users, groups, or roles.
# Best Practices:
Use least privilege: Grant only the permissions required for tasks.
Regularly review and update policies.
Prefer managed policies for easier maintenance.
# Permission Boundaries
Definition: A managed policy that sets the maximum permissions an identity-based policy can grant to an IAM entity (user or role).
# Use Case Example:
Restrict what actions a role or user can perform, even if they have broader permissions attached elsewhere.
# Best Practices
Always follow the principle of least privilege.
Regularly audit and update IAM policies.
Use AWS managed policies where possible for easier updates and maintenance.
Enable MFA (Multi-Factor Authentication) for additional security.
# Resources
AWS IAM Documentation
AWS Free Tier (for practice)
IAM Policy Simulator
AWS IAM Best Practices
