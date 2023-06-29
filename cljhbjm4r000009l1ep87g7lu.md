---
title: "Aws Iam"
datePublished: Thu Jun 29 2023 15:47:06 GMT+0000 (Coordinated Universal Time)
cuid: cljhbjm4r000009l1ep87g7lu
slug: aws-iam

---

AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources. With IAM, you can centrally manage permissions that control which AWS resources users can access. You use IAM to control who is authenticated (signed in) and authorized (has permissions) to use resources.

IAM stands for Identity Access Management.

* IAM allows you to manage users and their level of access to the AWS console.
    
* It is used to set users, permissions and roles. It allows you to grant access to the different parts of the AWS platform.
    
* AWS Identity and Access Management is a web service that enables Amazon Web Services (AWS) customers to manage users and user permissions in AWS.
    
* With IAM, Organizations can centrally manage users, security credentials such as access keys, and permissions that control which AWS resources users can access.
    
* Without IAM, Organizations with multiple users must either create multiple user accounts, each with its billing and subscriptions to AWS products or share an account with a single security credential. Without IAM, you also don't have control over the tasks that the users can do.
    
* IAM enables the organization to create multiple users, each with its security credentials, controlled and billed to a single AWS account. IAM allows the user to do only what they need to do as a part of the user's job.
    

## **IAM features**

IAM gives you the following features:

**Granular permissions:** It is used to set a permission that the user can use a particular service but not other services.

* **Identity Federation:** An Identity Federation means that we can use Facebook, Active Directory, LinkedIn, etc with IAM. Users can log in to the AWS Console with the same username and password as we log in with the Active Directory, Facebook, etc.
    
* **Multifactor Authentication:** An AWS provides multifactor authentication as we need to enter the username, password, and security check code to log in to the AWS Management Console.
    
* **Secure access to AWS resources for applications that run on Amazon EC2**
    
    You can use IAM features to securely provide credentials for applications that run on EC2 instances. These credentials provide permissions for your application to access other AWS resources. Examples include S3 buckets and DynamoDB tables.
    
* **Free to use:**
    
    AWS IAM is a feature of the AWS account that is offered at no additional charge. You will be charged only when you access other AWS services by using an IAM user.
    
* By using AWS IAM, you can effectively manage and secure access to your AWS resources, ensuring that only authorized individuals have appropriate permissions and that actions are logged for accountability and compliance purposes. Overall, IAM is an essential component of AWS security, providing granular control over access to your AWS account and resources, reducing the risk of unauthorized access and helping maintain a secure environment.
    

# IAM Components:

An *<mark>IAM user</mark>* is an identity within your AWS account that has specific permissions for a single person or application. Where possible, best practices recommend relying on temporary credentials instead of creating IAM users who have long-term credentials such as passwords and access keys. However, if you have specific use cases that require long-term credentials with IAM users, we recommend that you rotate access keys. For more information, see Rotate access keys regularly for use cases that require long-term credentials. To add IAM users to your AWS account, see Creating an IAM user in your AWS account.

**IAM user groups**

An ***<mark>IAM group</mark>*** is an identity that specifies a collection of IAM users. You can't use a group to sign in. You can use groups to specify permissions for multiple users at a time. Groups make permissions easier to manage for large sets of users.

### Roles:

<mark>IAM roles</mark> are used to grant temporary access to AWS resources. Roles are typically used by applications or services that need to access AWS resources on behalf of users or other services. Roles have associated policies that define the permissions and actions allowed for the role.

## **Policies and groups**

You can organize IAM users into *IAM groups* and attach a policy to a group. In that case, individual users still have their credentials, but all the users in a group have the permissions that are attached to the group.