# Amazon Web Services

**What is AWS:**  
 "Amazon Web Services (AWS) is the world’s most comprehensive and broadly adopted cloud platform, offering over 175 fully featured services from data centers globally. Millions of customers—including the fastest-growing startups, largest enterprises, and leading government agencies—are using AWS to lower costs, become more agile, and innovate faster."
 
 Source: https://aws.amazon.com/what-is-aws/

# Account Setup

**Create free Account**  
Before you start your journey the important step is to create an aws account. This is the prerequisite for learning. You can read a lot of data but without hands on it will all be futile.  

Start by creating a free tier account (Concentrate on free, what is stopping you to create one then ;) )  
Just to give you a headsup this free comes with a limit depending on the services you use and some of the services are not included in this free tier. Please have a quick glance at https://aws.amazon.com/free so as to make correct decisions.

**Registration page:**  
 - aws.epam.com
 - Basic details (Email/Password/AWS account id)
 - Account type: (Personal/professional)
 - Payment information (in case you exceed the free tier):
    - Rs 2 were deducted for verification in India
    - $ 1 in US
 - Confirm your identity: OTP/voice call on mobile number
 - Select a support plan:
    - Basic Plan (Recommended for new users just getting started with aws)
      - 24x7 self-service access to AWS resources
      - For account and billing issues only
      - Access to Personal Health Dashboard & Trusted Advisor
    - Developer Plan ( Recommended for developers experimenting with AWS )
      - Email access to AWS Support during business hours
      - 12 (business)-hour response times
    - Business Plan (Recommended for running production workloads on AWS)
      - 24x7 tech support via email, phone, and chat
      - 1-hour response times
      - Full set of Trusted Advisor best-practice recommendations
 - Sign in to console:
   - Root User
   - IAM User
   - As we are just starting off we will select root user and sign in with email and password

For understanding of different plans: https://aws.amazon.com/premiumsupport/plans/
Different certifications available: https://aws.amazon.com/certification/

# 1. Cloud Computing:

## 1.1 Traditional Setup:
**Normal Server composition:**  
 - Power
   - Compute: CPU
   - Memory: RAM
 - Storage:
   - Data
 - Database: 
   - Store data in a structured way
   - Network: Routers, Switch, DNS Servers

**Terminologies:**  
`Network:` cables, routers and servers connected with each other
`Router:` A networking device that forwards data packets between computer networks. They know where to send your packets on the internet!
`Switch:` Takes a packet and send it to the correct server / client on your network

**Problems With traditional IT:**  
 - Pay for rent, power supply, cooling, maintenance
 - Adding and replacing hardware takes times
 - Scaling is limited 
 - Hire 24/7 team for monitoring infrastructure/
 - Disaster/Natural calamities are not in control

**Solution for all above problems is : CLOUD**

## 1.2 Cloud setup

**What is Coud computing**
Cloud computing is the on-demand delivery of compute power, database storage,
applications, and other IT resources:
 - Through a cloud services platform with pay-as-you-go pricing
 - You can provision exactly the right type and size of computing resources you need
 - You can access as many resources as you need, almost instantly
 - Simple way to access servers, storage, databases and a set of application services
 - Amazon Web Services owns and maintains the network-connected hardware required for these application services, while you provision and use what you need via a web application.

**Deployment models of the cloud:**

|  Private cloud     | Public cloud | Hybrid cloud |
| ---------------- | -------------------- | --------------------- |
| Cloud services used by a single organization, not exposed to the public. | Cloud resources owned and operated by a thirdparty cloud service provider delivered over the Internet. | Keep some servers on premises and extend some capabilities to the Cloud              |
| Complete control over the infrastructure |                      | Control over sensitive assets in your private infrastructure |
| Security for sensitive applications |                      | Flexibility and costeffectiveness of the public cloud |
| Example: Rackspace| Example: Microsoft Azure, Google cloud platform (GCP), Amazon Web Services (AWS) | Example: private infra + any public cloud provider|

Characterstics of Cloud computing

Advantages:

Problems solved

## 1.2 Types of Cloud Computing:

## 2. Introduction to AWS Services

### 2.1 Infrastructure

The best resource to understand infrastructure is https://www.infrastructure.aws/.  
Here you can click on different sections to understand in detail about them. A brief summary is as below:

**AWS global datacentres:**  
 - It is important to know how many regions and availability zones does aws provide
 - You can always get the latest data at: :https://aws.amazon.com/about-aws/global-infrastructure/
 - For, Instance, India has 1 region and USA has 7 
 - While deploying we can decide which region to deploy in
 - Each region will have typically 2 or more data centers for hig availability of services and hence called availability zones
 - Edge locations are the place where the data is cached to the nearest location from where it is accessed
 - 175+ services

**Region and Availability zones:**  
 - `Region:` Independent geographic area, typically has 2 or more availability zones
 - `Availability zones:` Multiple isolated locations/data centers within a region

### 2.2 AWS account, users and services scope

**AWS account (Global)**
 - IAM{Identity and Access Management} users. (User management)
 - Billing
 - Route53

**Region level services**
 - S3 Bucket
 - Dynamo DB (NoSQL db)

**Availability zones services**
 - EC2 it is vm
 - RDS relational databases
 - EBS Elastic block storage

### 2.3 Different services
ElasticCache - Redis and memcached  
ELB - Elastic load balancer  
VPC - Virtual private cloud  
Route53 - DNS service  
S3 - Simple storage service (External storage)  
Rekognition - Content filter  
Lambda - Serverless service  
Kinesis - Click stream analysis  
EMR - aggregation, processig spark/hadoop cluster  
GLUE - ETL  
Redshift - data warehouse can store petabytes  
Quicksight - Bi analysis  
Athena - SQL tool for BI  
Cloudfront - Content delivery network (cache). It does this with the help of edgelocation  
SNS - Simple notification service - for mobile push notifications/SMS  
SES - Simple email service - for sending mails/ bulk emails  
SQS - Simle queue service - messaging queues or chatting app  
Cloudwatch - Monitor all the services, set alarms  

**Expose API**  
API Gateway - Rest API  
Cognito - web and mobile user management  

**Security**  
IAM - manage all accesses in AWS  
KMS - Key management service  
ACM - Digital certificates for https ssl connection Amazon certification management  
WAF - Web application firewalls (Prevents ddos, sql injection, cross site scripting, etc)  
Inspector - PCI DSS compliance, HIPPA compliance: scans for any known vulnerabilities  

**Development and Devops services**  
CloudFormation: code your infrastructure/Infrastructure as a code (json/yaml)  
CodeCommit: Code repo:  (similar to github)  
CodeBuild: Build tool (ant/maven)  
CodeDeploy: Deployment  
CodePipeline: (covers all above 3 service)  
CodeStar: Project managing/issue tracking/   

**Video converter from 1 s3 to another**  
option 1:  
 - EC2 instance watches s3 for a new video  
 - downloads - converts it - puts in another s3  
Option 2:  
 - Lambda  
  - specify how to converter  
  - triggered when video uploaded  
  - scales automatically  

**AWS Networking services**  
**Developer**  
 - VPC basics
    - CIDR
    - Internet Gateway
    - Subnets
    - Route tables
    - NAT
    - IP (Public, private, Elastic), NAT
    - Security Group
    - Network ACl
 - ELB/Cloudfront
 - Route53 (DNS)
 - VPC Endpoint
 - Private Link
 - VPC Peering

**DevOps**  
 - All Services for Developer
 - Transit VPC
 - Transit Gateway
 - Site to Site VPN
 - Client VPN
 - Other Topics
   - Network automation (CloudFormation, CLI)
   - Logging and Monitoring

**Network Administrator**  
 - All Services for Developer and Devops
 - Direct Connect
 - VPC Advanced
 - Other Topics
    - Enhanced Networking
    - hybrid connectivity
    - Network Performance
    - Network Security (Layer 3, Layer 7)

## 3. Identity and Access Management (IAM)

### 1. Basics

**Components:**  
 - It is a global Services
 - Root account is created by default when you create your account
 - It is recommended to not use or share this and should only be used for user creation
 - Users: These are the people within the organization and can be grouped based on departments, roles, etc
 - Groups: These contains only the users created above and no other groups
 - Note: It is not mandatory for Users to be assigned to a group. It can be the case that a user does not belong to any group or it can belong to multiple groups as well

**Permissions:**  
 - Users or Groups can be assigned JSON documents called `policies`
 - Policies define what users/groups are allowed or in short the permissions of the users
 - [Least privilege access](http://docs.aws.amazon.com/wellarchitected/latest/security-pillar/permissions-management.html): It is recommended to follow this principle that states dont give user more permissions that he needs 

### 2 How to land to IAM (Common step across this section)
 - Go to: https://aws.amazon.com -> login with root user
 - You can use the Global search -> Search IAM -> Select
 - Or go to Services -> Security, Identity and compliance -> IAM
 - You will be landed to Dashboard of IAM
 
### 3 Add User:  
 - Go to Access Management -> Users -> Add Users

Step 1:  
 - User Name: johndoe
 - Access type 
   - Programmatic Access: check
   - AWS Managemenet Console access: check
 - Console password
   - Autogenerate Pasword: unchecked
   - Custom Password: checked
 - Require Password Reset Checkbox: unchecked

Step 2: Set Permissions
 - Add user to group: In case you donot have groups already, "get started with group"
 - Copy permissions from existing user
 - Add existing policies directly

get started with group  
 - Group Name: admins
 - Create policy/ add policies
 - For starter add AdministratorAccess policy to make the users in group as admins

Step 3: Add tags (Optional)
 - for eg: Department as key and value as Enineering

Step 4: Review whatever you have selected till now

Step 5: Success, you have created an user.
 - There is a one time option to download the csv that contains every information including how to login and passwords, etc
 - A link will also be generated that can be shared with the user directly.

Detailed steps:
 - Step by step screenshots are available [here]

Tip:  
In IAM dashboard, set Sign-in URL for IAM users in the account, you will have a default value by default or you can edit and see if you have an alias available

**How to differentiate a root user or IAM user?**
 - root user: you will directly have name 
 - IAM user: username @ account name

### 4. Policies

 - if you remove the user from the group admins having AdministratorAccess policy, user will not be able to create/read groups and users
 - if you add a readonly policy, your user will only be able to read
 - Go to Access Management -> Policies  
 - Here you can see all the policies and can create custom ones as well
 - you can see the policy summary and json tab of policy, where policy summary is human readable and json has the same thing in json format
 - For creating policy: you can do it via visual editor or directly write the json as well

### 5 Multi Factor Authentication - MFA

**Password policy Basics**  
 - String password means higher security for your account
 - In AWS, you can setup a password policy:
   - set a min password length
   - Require specific character types:
     - including uppercase letters
     - lowercase letters
     - numbers
     - non-alphanumeric characters
 - Allow All IAM users to change their own passwords
 - Require users to change their password after some time (password expiration)
 - prevent password re-use

**Hands on console**  
- Go to Access Management -> Account settings -> Password policy
- Default password policy:
  - Minimum password length is 8 characters
  - Include a minimum of three of the following mix of character types: uppercase, lowercase, numbers, and ! @ # $ % ^ & * ( ) _ + - = [ ] { } | '
  - Must not be identical to your AWS account name or email address
- now you can modify the options as per yor org guidelines

**MFA device options:**  
 - Virtual MFA device (Support for multiple tokens on a single device)
   - Google authenticator (phone only)
   - Authy (multi-device)
 - Universal 2nd Factor (U2F) Security Key 
   - Support for multiple root and IAM users using a single security key
   - YubiKey by Yubico (3rd party)
 - Hardware Key Fob MFA Device
   - provided by Gemalto (3rd party)
 - Hardware Key Fob MFA Device for AWS GovCloud (US)
   - Provided by Surepassid (3rd party)

**Hands on console**  
 - Activate MFA
   - Virtual MFA Device
   - U2F security key
   - Other Hardware MFA device
 - We select Virtual MFA Device
   - List of supported devices: https://aws.amazon.com/iam/features/mfa/?audit=2019q1
   - Install any of the above apps
   - Scan QR code
   - Type 2 consecutive MFA codes
   - Success
 - Next time you login via your root account you have to provide MFA token along with your password

### 6. Ways to access AWS

 - `AWS Management Console:`(Protected by password + MFA)
 - `AWS Command line Interface (CLI):` protected by access keys
 - `AWS Software Development Kit (SDK) for code:` protected by access keys
 - Access keys used above are generated through AWS console
 - Users Manage their own access keys
 - **Access keys are secret like you have passwords, it is recommended not to share them**

Acess keys:  
 - `Access Key Id` which is used like a username but it is not the same
 - `Secret Access Key` which is used like a password but it is not the same.

#### 6.1 AWS console
 - All the hands on we dod till now is on console

#### 6.2 AWS cli on Windows

**Installation:**  
 - Google -> Download aws cli on windows -> [Link](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2-windows.html)
 - Install the downloaded msi file. for me it was 28 MB.
 - After finishing installation, go to cmd -> type aws --version -> you will get the result as below
 - [Successful installation]()
 - In case you want to upgrade, you have to download the latest version of msi and install again

**Hands On:**  
 - Do not use your root account to create security credentials
 - Login via IAM user -> IAM -> Access management -> Users -> select your name -> Security credentials tab
 - Access keys -> Create access keys (Single time download and next time you have to create a new one in case you forgot or missed)
 - Open cmd prompt -> type `aws configure` -> 
   - provide access key id: one you created just above
   - access key secret: one you created just above
   - Default region name: the region close to you
   - Default output format: nothing, just press enter
 - verify if aws is configured correctly by: `aws iam list-users`
 - [output]()
 - permissions updated via console will reflect in console as well.
 - in case you do not have permissions, there will be a blank response

### 7. IAM Roles for services

**Basics**  
 - Some AWS services will need to perform actions on your behalf
 - To achieve that, we will assign permissions to AWS serviceswith IAM Roles.
 - Common roles:
   - EC2 Instance roles
   - Lambda Function roles
   - Roles for CloudFormation

**Form AWS console**  
IAM roles are a secure way to grant permissions to entities that you trust. Examples of entities include the following:  
 - IAM user in another account
 - Application code running on an EC2 instance that needs to perform actions on AWS resources
 - An AWS service that needs to act on resources in your account to provide its features
 - Users from a corporate directory who use identity federation with SAML
 - IAM roles issue keys that are valid for short durations, making them a more secure way to grant access.

**Hands on**  
 - Go to Access Management -> Roles -> Create Roles
 - You can create role for:
    - AWS service:EC2, Lambda and others
    - Another AWS account: Belonging to you or any third party
    - Web identity: Cognito or any openId provider
    - SAML 2.0 federation: your corporate directory
 - We will do only for `AWS service` as of now, select EC2 and click `Next:Permissions`
 - Lets provide **IAMReadOnlyAccess** to this role and `Next:Tags`
 - We can skip this and do `Next:Review`
 - Provide Role name -> Create Role

### 8. IAM Security Tools

**Basics**  
 - IAM Credentials Report(account-level)
   - A report that lists all your account's users and the status of their various credentials
 
 - IAM Acess Advisor (user-level)
   - Access Advisor shows the service permissions granted to a user and when those services were last accessed.
   - You can use this information to revise your policies. (Enforce policy of least privilege)

**Hands On**  
Credentila Report  
 - Go to Access Reports -> Credential Report
 - you will get complete summary of all the users

Access Advisor
 - Go to Access Management -> Users -> select user -> Access Advisor
 - Gives you detailed summary of the services used and in turn helps in effectively managing the access
 - Ref: https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_access-advisor.html

### 9. IAM Guidelines and Best Practices

 - Don't use the root account except for AWS account setup
 - One Physical user = One AWS user
 - Assign Users to groups and assign permissions to groups to make sure security is maintained at group level
 - Create a Strong password policy/
 - Use and enforce the use of Multi Factor Authentication (MFA)
 - Create and use Roles for giving permissions to AWS services.
 - Use access keys for Programatic access (CLI/SDK)
 - Audit permissions of your account with the IAM Credentials Report and IAM Access Advisor
 - **Never share IAM users and Access Keys**

**Best practices from IAM Dashboard in AWS console**  
 - [Grant least privilege access](http://docs.aws.amazon.com/wellarchitected/latest/security-pillar/permissions-management.html) : Establishing a principle of least privilege ensures that identities are only permitted to perform the most minimal set of functions necessary to fulfill a specific task, while balancing usability and efficiency.
 - Enable Identity federation: Centrally manage users and access across multiple applications and services. For federation to multiple accounts in your AWS Organization, you can configure your identity source in [AWS Single Sign-on](https://console.aws.amazon.com/singlesignon/home).
 - Enable MFA: For extra security, we recommend that you require multi-factor authentication (MFA) for [all users](https://console.aws.amazon.com/iam/home?region=us-east-2#users).
 - [Rotate credentials regularly](https://console.aws.amazon.com/iam/home?region=us-east-2#security_credentials): Change your own passwords and access keys regularly, and make sure that all users in your account do as well.
 - Enable [IAM Access Analyzer](https://console.aws.amazon.com/access-analyzer/home): Enable IAM Access Analyzer to analyze public, cross-account, and cross-organization access.
 - Learn more about all **[security best practices](https://console.aws.amazon.com/access-analyzer/home)**.

### 10. Shared Responsibility Model for IAM

| AWS                                           | You                           |
| -------------                                 |:-------------:                      |
| Infrastructure (global network security)      | Users, Groups, Roles, Policies management and monitoring |
| Configuration and vulnerability analysis of services they offer     | Enable MFA on all accounts |
| Compliance Validation                         | Rotate all your keys often |
|                                               | Use IAM tools to apply appropriate permissions|
|                                               | Analyze access patterns and review permissions|

### 11. IAM Summary

 - Users: mapped to physical user, has a password for AWS Console
 - Groups: contains users only
 - Policies: JSOn documents that outlines permissions for users or groups
 - Roles: for EC2 instances or AWS services
 - Security: MFA + password policy
 - Access keys: Access AWS using the CLI/SDK
 - Audit: IAM Credential Reports and IAM Access Advisor

### QUIZ

What is a proper Definition of IAM roles:
 - An IAM entity that defines a set of permissions for making AWS service requests, that will be used by AWS services
 - Some AWS service will need to perform actions on your behalf. To do so, you assign permissions to aws services with IAM Roles

Which is an IAM Security Tool?
 - IAM Credential Report
 - IAM Credentials report lists all your account's users and the status of their various credentials. The other IAM security Tool is IAM Access Advisor. It shows the service permissions granted to a user and when those services were last accessed.
 
What are IAM Policies?
 - JSON Documents to define Users, Groups or Roles' permissions
 - An IAM policy is an entity that, when attached to an identity or resource, defines their permissions.

### Reference:
 - [Identity Management](https://www.aws.training/Details/eLearning?id=55148)

## Manage Billing

In case you access the billing module from IAM user, you igt get below permissions error  
```cmd
You Need Permissions
You don't have permission to access billing information for this account. Contact your AWS administrator if you need help. If you are an AWS administrator, you can provide permissions for your users or groups by making sure that (1) this account allows IAM and federated users to access billing information and (2) you have the required IAM permissions.
```

You have to update the access via root account
 - Account name -> My Account -> IAM User and Role Access to Billing Information -> Edit -> Activate IAM Access -> Update
 - Go to IAM user account and refresh to see it refkects now

Now to setup a budgetgo
 - Go to Budgets -> Create a Budget -> you have below options
   - Cost Budget: Monitor your costs against a specified amount and receive alerts when your user defined thresholds are met
   - Usage Budget: Monitor your usage of one or more specified usage types or usage type groups and receive alrets when your user-defined thresholds are met
   - Reservation Budget: Track the RI Utilization or RI Coverage associated with your reservations. Thses budgets supports Amazon EC2, RDS, Redshift, ElasticCache and ElasticSearch reservation models
   - Savings plan budget: Track the utilization and coverage associated with your Savings plans
 - Lets create `Cost Budget`, provide name, recurring type monthly, threshold amount at which alert will be triggered. and create
 

## 4. EC2 - Elastic Compute Cloud

- EC2 is one of te most popular AWS offering
- 



# Resources

 - [Introduction to AWS Services](https://www.youtube.com/watch?v=Z3SYDTMP3ME)
 - [Introduction to AWS Networking](https://www.youtube.com/watch?v=XZbvQWkpJTI)
 - [Open guides AWS](https://github.com/open-guides/og-aws)
 - [Resources with most stars on github are listed here](https://github.com/donnemartin/awesome-aws)
 - [Ultimate AWS Certified Cloud Practitioner - 2020](https://www.udemy.com/course/aws-certified-cloud-practitioner-new/)