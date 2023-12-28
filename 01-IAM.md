# IAM (Identity and Access Management)

## Introduction to IAM

AWS Identity and Access Management (IAM) is a foundational service in Amazon Web Services (AWS) that holds a critical role in overseeing access to your AWS assets. Functioning as a security mechanism for your AWS account, IAM empowers you to regulate and specify permissions through various entities such as users, groups, and roles. IAM is essential for secure access management, adhering to the principle of least privilege. Key elements encompass users, groups, and roles, each fulfilling a distinct function in access control. Policies, scripted in JSON, dictate permissions and can be assigned to entities. IAM incorporates features like Multi-Factor Authentication (MFA) and audit trails, providing additional layers of security and traceability for AWS resources.

### Key Concepts

1. **Users:**
   - IAM users represent individuals or entities requiring access to AWS resources.
   - Each user has a unique name and security credentials (password or access keys) for authentication.

2. **Groups:**
   - IAM groups are collections of users with similar access requirements.
   - Permissions are assigned to groups, streamlining access control and easing management.

3. **Roles:**
   - IAM roles provide temporary access to AWS resources.
   - Typically used by applications or services on behalf of users or other services.
   - Associated policies define permissions and actions allowed for the role.

4. **Policies:**
   - IAM policies are JSON documents specifying permissions.
   - Actions on AWS resources and applicable resources are defined.
   - Policies can be attached to users, groups, or roles to control access.
   - AWS provides both managed policies (maintained by AWS) and customer-managed policies.

### IAM Functionality

- **Permissions and Policies:**
  - IAM enables the definition of permissions through policies written in JSON format.
  - Policies dictate allowed or denied actions on specific AWS resources.

- **Principle of Least Privilege:**
  - IAM adheres to the principle of least privilege.
  - Users and entities are granted only necessary permissions, minimizing security risks.

- **Multi-Factor Authentication (MFA):**
  - IAM supports multi-factor authentication for enhanced security.

- **Audit Trail:**
  - IAM provides an audit trail to track user activity and changes to permissions.
  - Facilitates accountability and compliance tracking.