## IAM (Identity and Access Management)

IAM (Identity and Access Management) is a foundational service in Amazon Web Services (AWS) that plays a critical role in overseeing access to your AWS assets. Functioning as a security mechanism for your AWS account, IAM empowers you to regulate and specify permissions through various entities such as users, groups, and roles. IAM is essential for secure access management, adhering to the principle of least privilege. Key elements encompass users, groups, and roles, each fulfilling a distinct function in access control. Policies, scripted in JSON, dictate permissions and can be assigned to entities. IAM incorporates features like Multi-Factor Authentication (MFA) and audit trails, providing additional layers of security and traceability for AWS resources.

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

## IAM Features

IAM is a service offered by AWS that manages access to AWS accounts and resources. It provides a centralized view of authentication (who/what is allowed) and authorization (permissions), allowing sharing access without sharing keys/passwords. Some key features of IAM include:

- **Global:** IAM is a global service, meaning access policies set in IAM apply universally across all regions and resources within an AWS account.
- **Integrated with AWS services:** IAM seamlessly integrates with various AWS services, allowing for fine-grained control over access to resources.
- **Shared access:** IAM enables the sharing of access to AWS resources without the need to share long-term security credentials.
- **Multi-factor authentication:** IAM supports multi-factor authentication, adding an extra layer of security to user accounts.
- **Free to use:** There are no additional charges for using IAM; it's included as part of the AWS services.

### IAM User

An IAM user represents a person or service interacting with AWS. They are billed to your account for any activity and have credentials for accessing the AWS Management Console as well as programmatic access through the AWS CLI and API.

### IAM User Credentials

IAM user credentials can be permanent and stay with the user until forced rotation by admins. These credentials grant access to the AWS Management Console (username and password) and programmatic access (access keys for AWS CLI and API).

### IAM Groups

IAM groups are collections of users sharing inherited permissions. They provide a more convenient and scalable way of managing permissions and are considered a best practice for organizing users in AWS accounts.

### IAM Policies

IAM policies manage access and provide permissions. They are attached to IAM identities (users, groups, roles) and are evaluated when an IAM identity makes a request. Examples of IAM policies include an Admin Access Policy (allowing all actions on all resources) and a Granular S3 Access Policy (denying S3 access outside specified AWS account).

### IAM Roles

IAM roles play a crucial role in managing access to AWS resources, especially when dealing with entities like IAM users, groups, and policies. Key points related to IAM roles include:

- IAM roles provide a secure way to grant permissions to trusted entities.
- Unlike IAM users, roles are not associated with specific users or groups but can be assumed by anyone who needs temporary access to AWS credentials.
- IAM roles have associated AWS credentials used for signing requests but do not have login credentials like a username and password.
- IAM role credentials are programmatically acquired, temporary, and automatically rotated for enhanced security.
- IAM roles are often used for access between AWS services, facilitating role-based access and allowing one service to assume a role and interact with another service.
- External identity providers can also assume IAM roles to gain access to AWS, useful for scenarios where existing enterprise user directories need to be leveraged.

### IAM Best Practices

Some best practices for using IAM include:

- Locking down the AWS root user.
- Following the principle of least privilege.
- Using IAM appropriately for managing access to AWS resources.
- Leveraging IAM roles when possible for temporary access.
- Considering using an identity provider for managing user access.
- Regularly reviewing and removing unused users, roles, and other credentials to maintain security.
