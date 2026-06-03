# IAM (Identity and Access Management)

## What is IAM?

AWS Identity and Access Management (IAM) is a service that allows you to securely manage access to AWS resources.

With IAM, you can control:

* Who can access AWS resources
* What actions they can perform
* Which resources they can access

IAM is a Global Service, meaning it is not tied to a specific AWS Region.

---

## Main Components

### Users

An IAM User represents a person who needs access to AWS.

Examples:

* Ingrid
* A developer
* An administrator

Each user can have:

* Username and password (AWS Management Console)
* Access Keys (Programmatic Access)

---

### Groups

A Group is a collection of IAM Users.

Permissions can be assigned to a Group instead of individual users.

Example:

Developers Group:

* User A
* User B
* User C

If permissions are updated for the group, all users inherit the changes.

Benefits:

* Easier management
* Consistent permissions

---

### Policies

Policies define permissions in AWS.

They are JSON documents that specify:

* Allowed actions
* Resources
* Conditions

Example:

Allow:

* Read objects in an S3 bucket

Deny:

* Delete objects from the bucket

Types:

* AWS Managed Policies
* Customer Managed Policies
* Inline Policies

---

### Roles

IAM Roles provide temporary permissions.

Unlike users, roles do not have permanent credentials.

Common use cases:

* EC2 accessing S3
* Lambda accessing DynamoDB
* Cross-account access

Benefits:

* More secure than storing access keys
* Temporary credentials
* Recommended for applications and AWS services

---

## Accessing AWS

AWS resources can be accessed in different ways.

### AWS Management Console

The AWS Management Console is a web-based interface used to manage AWS services through a graphical interface.

Best for:

* Beginners
* Learning AWS services
* Manual administration

Authentication:

* Username and password
* MFA (recommended)

---

### AWS CLI (Command Line Interface)

The AWS CLI allows users to interact with AWS services through commands in a terminal.

Example:

```bash
aws s3 ls
```

Best for:

* Automation
* Scripting
* Managing resources from the command line

Authentication:

* Access Key ID
* Secret Access Key
* IAM Roles

---

### AWS CloudShell

AWS CloudShell is a browser-based shell that provides a pre-authenticated command-line environment for AWS.

Best for:

* Quick AWS CLI access without installing local tools
* Learning and experimentation
* Running one-off commands from any browser
* Using in environments where local CLI setup is not available

Authentication:

* Uses the IAM permissions of the signed-in console user
* No access keys needed in the shell session

Benefits:

* Pre-authenticated AWS CLI access
* Temporary shell environments stored in the cloud
* Easy access from anywhere with a browser

---

### AWS SDKs

AWS Software Development Kits (SDKs) allow applications to interact with AWS services using programming languages such as Python, Java, JavaScript, and C#.

Example:

A Python application uploading files to Amazon S3.

Best for:

* Application development
* System integrations
* Automated workloads

Authentication:

* Access Keys
* IAM Roles

---

## Security Best Practices

### Follow the Principle of Least Privilege

Grant only the permissions required to perform a task.

Example:

If a user only needs to read data from S3, do not grant delete permissions.

---

### Enable MFA

MFA (Multi-Factor Authentication) adds an extra layer of security.

Examples:

* Authenticator app
* Hardware token

Even if a password is compromised, MFA helps protect the account.

---

### Avoid Using the Root User

The root user has full access to the AWS account.

Best practice:

* Use the root account only for initial setup and specific administrative tasks.
* Create IAM users for daily activities.

---

### Rotate Credentials

Regularly rotate:

* Passwords
* Access keys

This reduces security risks.

---

### IAM Security Tools

AWS offers IAM-focused security tools to help validate access, analyze permissions, and detect risky configurations.

Examples:

* IAM Access Analyzer - analyzes policies and identifies resources shared with external entities.
* IAM Policy Simulator - tests policies to see which permissions are granted without making changes.
* IAM Last Accessed - shows service usage by users, groups, and roles to help remove unused permissions.
* IAM Credential Report - provides a credentials report for all IAM users to review passwords, access keys, and MFA status.

Why use them:

* Verify and correct policies proactively.
* Detect excessive permissions or unexpected access.
* Identify old or unused credentials.
* Improve IAM security without impacting users.

---

## Common Use Cases

* Managing employee access to AWS
* Controlling permissions for AWS services
* Granting temporary access through Roles
* Securing access with MFA
* Enforcing least-privilege permissions

---

## Related Services

* S3
* EC2
* Lambda
* Organizations
* AWS Identity Center

IAM is often the first service configured because it controls access to all other AWS services.

---

## Tips

* IAM is a Global Service.
* Never use the root account for daily activities.
* Enable MFA whenever possible.
* Follow the Principle of Least Privilege.
* Roles provide temporary credentials.
* Applications should use IAM Roles instead of storing access keys.
* Groups contain users, but groups cannot contain other groups.

---

## Quick Summary

| Component | Purpose                                     |
| --------- | ------------------------------------------- |
| User      | Represents a person who needs access to AWS |
| Group     | Collection of users                         |
| Policy    | Defines permissions                         |
| Role      | Temporary access                            |
| MFA       | Additional security layer                   |
| Console   | Web interface for managing AWS              |
| CLI       | Command-line access to AWS                  |
| SDK       | Programmatic access through code            |

### Key Takeaways

* IAM manages authentication and authorization.
* IAM is a Global Service.
* Users represent people.
* Groups simplify permission management.
* Policies define what actions are allowed or denied.
* Roles provide temporary credentials.
* MFA improves security.
* Follow the Principle of Least Privilege.
* Use the root account only when necessary.
* AWS can be accessed through the Console, CLI, or SDKs.
