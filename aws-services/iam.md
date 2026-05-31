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

An IAM User represents a person or application that needs access to AWS.

Examples:

* Ingrid
* A developer
* An application

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

## Key Concepts

* IAM is a Global Service.
* IAM manages authentication and authorization.
* Users are individuals.
* Groups contain users.
* Policies define permissions.
* Roles provide temporary access.
* MFA increases account security.
* Follow the Principle of Least Privilege.
* Avoid using the root account for daily work.

---

## Quick Summary

| Component | Purpose                            |
| --------- | ---------------------------------- |
| User      | Represents a person or application |
| Group     | Collection of users                |
| Policy    | Defines permissions                |
| Role      | Temporary access                   |
| MFA       | Additional security layer          |
