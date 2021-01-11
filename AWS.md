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
 - https://aws.amazon.com/free -> Create a free account
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

# 2. Introduction to AWS Services

## 2.1 Infrastructure

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

## 2.2 AWS account, users and services scope

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

## 2.3 Different services
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

# 3. Identity and Access Management (IAM)

## 1. Basics

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

## 2 How to land to IAM (Common step across this section)
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

## 4. Policies

 - if you remove the user from the group admins having AdministratorAccess policy, user will not be able to create/read groups and users
 - if you add a readonly policy, your user will only be able to read
 - Go to Access Management -> Policies  
 - Here you can see all the policies and can create custom ones as well
 - you can see the policy summary and json tab of policy, where policy summary is human readable and json has the same thing in json format
 - For creating policy: you can do it via visual editor or directly write the json as well

## 5 Multi Factor Authentication - MFA

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

## 6. Ways to access AWS

 - `AWS Management Console:`(Protected by password + MFA)
 - `AWS Command line Interface (CLI):` protected by access keys
 - `AWS Software Development Kit (SDK) for code:` protected by access keys
 - Access keys used above are generated through AWS console
 - Users Manage their own access keys
 - **Access keys are secret like you have passwords, it is recommended not to share them**

Acess keys:  
 - `Access Key Id` which is used like a username but it is not the same
 - `Secret Access Key` which is used like a password but it is not the same.

### 6.1 AWS console
 - All the hands on we dod till now is on console

### 6.2 AWS cli on Windows

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

## 7. IAM Roles for services

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

## 8. IAM Security Tools

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

## 9. IAM Guidelines and Best Practices

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

## 10. Shared Responsibility Model for IAM

| AWS                                           | You                           |
| -------------                                 |:-------------:                      |
| Infrastructure (global network security)      | Users, Groups, Roles, Policies management and monitoring |
| Configuration and vulnerability analysis of services they offer     | Enable MFA on all accounts |
| Compliance Validation                         | Rotate all your keys often |
|                                               | Use IAM tools to apply appropriate permissions|
|                                               | Analyze access patterns and review permissions|

## 11. IAM Summary

 - Users: mapped to physical user, has a password for AWS Console
 - Groups: contains users only
 - Policies: JSOn documents that outlines permissions for users or groups
 - Roles: for EC2 instances or AWS services
 - Security: MFA + password policy
 - Access keys: Access AWS using the CLI/SDK
 - Audit: IAM Credential Reports and IAM Access Advisor

## QUIZ

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

# Manage Billing

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
 

# 4. EC2 - Elastic Compute Cloud

## 4.1 EC2 

**Basics**  
 - EC2 is one of te most popular AWS offering
 - EC2 = Elastic Compute Cloud = Infrastructe as a Service (IaaS)
 - It mainly consiste of capability of:
   - Renting virtual machines **(EC2)**  
   - Storing data on Virtual drives **(EBS)**
   - Distributing load across machines **(ELB)**
   - Scaling the services using an auto-scaling group **(ASG)**
 - Knowing EC2 is fundamental to understand how the Cloud Works

**EC2 Sizing and configuration options**  
 - Operating System (OS): **Linux or Windows**
 - How much compute power and cores **(CPU)**
 - How much random-access memory **(RAM)**
 - How much storage space:
   - Network-attached **(EBS and EFS)**
   - hardware **(EC2 instance store)**
 - Network card: **speed of the card, public IP address**
 - Firewall rules: **security group**
 - **Bootstrap script (configure at first launch)**: EC2 User Data

**EC2 instance types**
 - Different depending on the cpu ram storage and network performance

**Hands on**

Launch EC2 instance running Linux

 - Launch first virtual server using the AWS Console
   - Choose region close to you
   - EC2 dashboard -> instances -> Launch Instance 
   - Step 1: Choose Amazon Machine Image (AMI)
   - These AMI is template image for all your work
   - you have 4 options to chooese from:
     - Quick start
     - My AMIs
     - awS marketPlace 
     - Community AMIs
   - Lets continue with quickstart and free tier option -> Amazon Linux 2 AMI (HVM), SSD Volume Type AMI
   - Step 2: Choose an instance type
     - there are multiple choice avaialble here as well and can be filtered based on instance families and generation, we will select t2.micro (Free tier eligible)
   - Step 3: Configure Instance details
     - Number of instances: 1
     - Network: same as default
     - IAM roles: same as default (none)
     - User data
        - ```cmd
          # Install httpd
          yum update -yaml
          yum install -y httpd
          systemctl start httpd
          systemctl enable httpd
          echo "<h1>hello world from ${hostname -f} </h1>" > /var/www/html/index.html
        ```
   - Step 4: Add storage: keep default
   - Step 5: Add tags -> you can add name for identification
   - Step 6: Configure security groups
     - Here, you have to create new security group, by default option is available for tcp, we will add for http with port 80
   - Step 7: Review and launch
      - Key pair: A key pair consists of a public key that AWS stores, and a private key file that you store. Together, they allow you to connect to your instance securely. For Windows AMIs, the private key file is required to obtain the password used to log into your instance. For Linux AMIs, the private key file allows you to securely SSH into your instance
      - Once you click on launch you are popped up to create a new key pair if not laready have or use and existing one
      - We will create a new one, provide a name and download key pair
      - `.pem` file will be downloaded
      - Launch instances
 - Get a First high-level approach to the various parameters
   - All steps given above
 - Launch a web-server using EC2 user data
   - We achieved this in step 3 above
 - Learn how to start/stop/terminate the instance
   - Actions -> Instance state -> start/stop/terminate
      - Start: Start the instance
      - Stop: Stop the instance, starting again will have new ip address assigned to the instance
      - Terminate: it will delete everything of this instance

## 4.2 introduction to Security Groups

**Basics**  
 - Security Groups are the fundamental of network security in AWS
 - They control how traffic is allowed into or out of our EC2 instances
 - Security Groups only contain allow rules
 - Security groups rules can reference by IP or by security group

**In depth**  
- Security groups are acting as a firewall on EC2 instances
- They regulate:
  - Access to ports
  - Authorized ip ranges: ipv4 and ipv6
  - Control of inbound network (from other to the instance)
  - Control of outbound network (from the instance to other)

**Classic ports to know**  

- 22  : SSH (Secure shell) - Log into a Linux instance
- 21  : FTP (File transfer protocol) - Upload files into a file share
- 22  : SFTP (Secure file transport protocol) - Upload files using SSH
- 80  : HTTP - Access unsecured websites
- 443 : HTTPS - Access secured websites
- 3389: RDP (Remote Desktop Protocol) - log into a Windows instance

**Hands on**

 - EC2 -> Network & Security -> Security Groups
 - You will have 1 default security group that is created by default with the account creation
 - And the another is that we created while creating the EC2 instance
 - [Screenshot]()
 - 0.0.0.0/0 -> Everywhere on ipv4
 - ::/0 -> Everywhere on ipv6
 - If you remove the http rules assigne above, it will affect all the EC2 instances it is assigne to.
 - Most of the time out issues are related to misconfiguration of security group
 - While creating a Security group, you have to select a type and then you can have source as:
   - Custom: ips you configure are allowed
   - Anywhere(0.0.0.0/0 or ::/0): any one is allowed
   - My IP: only your ip is allowed
 - You can resue these security groups
 
## 4.3 SSH Overview

**Summary**  

| OS               | SSH            |  Putty         |  EC2 Instance Connect|
| -------------    |:-------------: |:-------------: |:-------------: |
|  MAC             |    Yes         |                |    Yes         |
|  Linux           |    Yes         |                |    Yes         |
|  Windows < 10    |                |    Yes         |    Yes         | 
|  Windows >= 10   |    Yes         |    Yes         |    Yes         |  

**SSH on Windows 10**  

 - open powershell/cmd -> ssh -> if options comes up, you can continue or else have to use putty
 - [Screenshot]
 - Command to run: ssh -i <path to pem file downloaded> ec2-user@<ip addres of EC2 instance>
 - eg: ssh -i D:\Data\aws\firstEC2instance.pem ec2-user@3.135.188.103
 - ec2-user is the default user that is logged in to the ec2 instances
 - Confirm yes
 - [Screenshot]
 - bad permissions error
 - [Screenshot]
 - go to pem file -> right click -> security -> advanced
   - update owner to yourself
   - remove other users by first disabling inheritance
   - done
 - now you will be able to login

**SSH Instance Connect**  

 - Go to instances -> connect -> you have 3 choices here
   - A standalone ssh client
   - session manager
   - EC2 instance Connect (browser-based SSH connection)
 - We will select 3rd option -> ec2-user will be autopopulated -> Connect
 - SSH is mandatory for above to work, in case the security group attached to this instance does not have SSH enabled, it wont work
 - Works only with Amazon Linux 2 AMI

**EC2 Instance roles**

 - Connect via Instance connect
 - type `ping google.com` to verify if the connection is working from ec2 instance
 - lets try `aws --version` to check if aws-cli is installed
 - As it is installed lets try to fetch all users: `aws iam list-users`
 - [screenshot]
 - we do not have permissions to do so, we can try `aws configure` and provide our access key, but this will enable all the users login into this instance to use our credentials and hence we achieve this via roles.
 - NEVER USE `aws configure` in EC2 instance
 - Verify from: go to IAM -> Roles -> DemoRoleForEC2 is already created in above steps
 - EC2 -> instances -> Actions -> Instance Settings -> Attach/Replace IAM roles -> Assign DemoRoleForEC2 -> Apply
 - try again `aws iam list-users` and it will work for you this time.

## 4.4 EC2 Instance Launch types

**Summary**  
  - **On Demand**: Ideal for short workload, predictable procing
  - **Reserved**: Minimum 1 year is required
    - **Reserved Instances:** long workloads like databases
    - **Convertible Reserved Instances:** long workloads with flexible instances
    - **Scheduled Reserved Instances:** example is "every sunday 3 pm to 6 pm"
  - **Spot Instances:** short workloads, cheap, can lose instances (less reliable)
  - **Dedicated Hosts** book an entire physical server, control instance placement

**On Demand**  
 - Pay for what you use
   - Linux: billing per second, after the first minute
   - All other OS: billing per hour
 - Has the highest cost but no upfront payment
 - No long term commitment
 - Recommended for: 
   - Short term and uniterrupted workloads, where you cant predict how the application wwill behave

**Reserved Insances**
 - Upto 75% dicount compared to On-demand
 - Reservatio period: 1 year = discount +, 3 year = discount +++
 - Purchasing options: no upfront,  partial upfront = discount +, All upfront = discount +++
 - Reserve a specific instance type
 - Recommended for: 
   - steady state usage applications (think database)

 - **Convertible Reserved Instance:**
   - Can change the EC2 instance type
   - Upto 54% discount
 - **Scheduled Reserved Instances**
   - launch withing timewindow you reserve
   - when you require a fraction of day/week/month
   - still commintment over 1 to 3 years

**EC2 Spot instances**  

 - Can get a discount of upto 90% compared to On-Demand
 - Instances that you can "lose" at any point of time if your max price is less than the current spot price
 - The most cost efficient instances in AWS
 - Useful for workloads that are resilient to failure
   - batch jobs
   - data analysis
   - image processing
   - Any distributed workloads
   - workloads with a flexible start and end time
 - Not suitable for critical jobs and databases

**Dedicated Hosts**

 - An Amazon EC2 Dedicated host is a physical server with EC2 instance capacity fully dedicated to your use
 - Dedicated hosts can help you address "Compliance requirements" and reduce costs by allowing you to **use your existing server bound software licenses**
 - Allocated for your account for a 3 year period reservation
 - They are expensive
 - Useful for software that have complicated licensing model (BYOL - Bring your own license)
 - or for companies that have strong regulatory or compliance needs

**Dedicated Instances**

 - Instances running on hardware that's dedicated to you
 - may share hardware with other instances in same account
 - No control over instance placement (can move hardware after stop/start)
 - Soft version of dedicated host

## 4.5. Shared Responsibility Model for IAM

| AWS                                           | You                           |
| -------------                                 |:-------------:                      |
| Infrastructure (global network security)      | Security group rules|
| Isolation on physical hosts                   | OS patches and updates|
| Replacing faulty hardware                     | Software and utilities installed on the EC2 instance|
| Compliance Validation                         | IAM Roles assigned to EC2 and IAM user access management|
|                                               | Data security on your instance|

## 4.6 EC2 Summary
 
 - EC2 Instance:
   - AMI(OS)
   - Instance size (CPU + RAM)
   - Storage
   - Security groups
   - EC2 User data
 - Security groups: Firewall attached to the EC2 instance
 - EC2 User data: Script launched at the first start of an instance
 - SSH: start a terminal into our EC2 instances (port 22)
 - EC2 Instance Role: link to IAM roles
 - Purchasing Options:
   - On-demand
   - Reserved (Standard, Convertible, Scheduled)
   - Spot
   - Dedicated Hosts
   - Dedicated Insance

## 4.7 EC2 Quiz

Which network security tool can you use to control traffic in and out of EC2 instances?
 - Security groups

How long can you reserve an EC2 Reserved instance?
 - 1 or 3 years (Not anytime between 1 and 3 years)

Which EC2 purchasing option should you use for an application you plan on running on a server continously for 1 year?
 - Reserved Instances

# 5. EC2 Instance Storage

## 5.1 Whats an EBS Volume

**Basics**  
 - An EBS (Elastoc Block Store) Volume is a network drive you can attach to your instances while they run
 - It allows your instances to persist data, even after their termination
 - They can **only be mounnted to one instance at a time (at the Certified cloud Practitioner level)**
 - They are **bound to a specific availability zone** and cannot be attached to another zone
 - Free tier: 30gb of free EBs storage of type gp2 per month
 - Its a network drive (i.e not a physical drive)
   - It uses a network to communicate the instance, which means there might be a bit of latency
   - It can be detached from an EC2 instance and attached to another one quickly
 - Its locked to an avaialbility zone (AZ)
   - An EBS volume in `us-east-1a` cannot be attached to `us-east-1b`
   - To move a volume across, you first need to snapshot it
 - Have a provisioned capacity (size in GBs and IOPS - I/O operations per second)
   - You get billed for all the provisioned capacity
   - You can increase the capacity of the drive over time

**Hands on**  
 - EC2 -> instances -> already one instance created -> verify `Root device` and `Block devices` in the details which links to an EBS volume -> you can click on the link or go as below
 - EC2 -> Elastic Block Store -> Volume -> a root block store is already avaialble (this is the one we provisioned while creating an EC2 instance)
 - Create new Volume: EC2 -> Elastic Block Store -> Volumes -> Create Volume -> 
   - Volume type: default (General Purpose SSD (gp2))
   - Size (GiB): 2
   - Availability zone: (should be same that of an EC2 instance you are planning to attach, you can verify via EC2 -> instances -> "Availability zone" column of your instance)
   - Create Volume
 - Created vilume will be populated in the list-users`
 - you can attach this volume via Actions -> attach Volume -> Select your instance from dropdown -> attach
 - Verify via EC2 -> instances -> already one instance created -> `Block devices` -> 2 entries now
 - If you delete an EC2 instance, an EBS volume attached to that instance if marked `delete on termination` to true while creating that instance will also be deleted

## 5.2 EBS Snapshots

**Basics**  
 - Make a backup (snapshot) of your EBS volume at a point in time
 - Not necessary to detach volume to do snapshot, **but recommended**
 - Can copy snapshots across AZ or Region

**Hands on**  
 - EC2 -> Elastic Block Store -> Volume -> select volume -> Actions -> Create snapshot 
   - Add Description
   - Create
   - Verify it is created via EC2 -> Elastic Block Store -> Snapshots
   - Now you can copy this snapshot anywhere to get that data via Actions -> Copy
   - Also, a volume can be created from this snapshot via Actions -> Create Volume -> now you can select the availability zone -> Create Volume

## 5.3 AMI Overview

**Basics**  
 - AMI - Amazon Machine Image
 - AMI are a customization of an EC2 instance
   - You add your own software, configuration, operating system, monitoring, etc
   - Faster boot/configuration time because all your software is pre-packaged
 - AMI are built for a specific region (and can be copied across regions)
 - You can launch EC2 instances from:
   - A public AMI: AWS provided
   - Your Oen AMI: you make and maintain them yourself
   - An AWS Marketplace AMI: An AMI someone lese made (and potentially sells)

**How to create an Custom AMI**  
 - Start an EC2 instance and customize it
 - Stop the instance (for data integrity)
 - Build an AMI - this will also create EBS snapshots
 - Launch instances from other AMIs

**Hands on**  
 - We already have an EC2 instance created, in case it is not dn follow the steps defined above to create the same
 - Instances -> Action -> Image -> Create Image -> provide name and then create
 - Go to Images -> AMI -> it will take some time(3 to 5 minutes for me) to create and will be in pending state.
 - Now lets use this above created custom AMI to create an Instance
 - Instances -> Instance -> Launch Instance -> My AMIs -> Select AMI that you just created -> t2.micro next -> Next (no user data as we will be having this from AMI created above) -> Next -> reuse all existing keys and security group -> launch
 - now you can hit the ip and you will get the same ip that you had before as we are using the same image and that ip was hard coded in index.html already
 
## 5.4 EC2 Instance Store

 - EBS volumes are network drives with good but "limited" performance
 - If you need high-performance hardware disk, use EC2 instance store
 - Better I/O Performance
 - EC2 Instance store lose their storage if they're stopped (ephermal)
 - Good to buffer/cache/scratch data/temporary content
 - Risk of data loss if hardware fails
 - Backups and replication are your responsibility

## 5.5 EFS - Elastic File System

**Basics**  
 - Managed NFS (Network file system) that can be mounted on 100s of EC2
 - EFS works with linux EC2 instances in multi avaialbility zones
 - High available, Scalable, expensive (3x gp2), pay per use, no capacity planning 

## 5.6 Shared responsibility model for EC2 storage

| AWS                                                 | You                           |
| -------------                                       |:-------------:                      |
| Infrastructure (global network security)            | Setting up backup/snapshot peocedures |
| Replication for data for EBS volumes and EFS drives | Setting up data encryption for additional security|
| Replacing faulty hardware                           | Responsibility of any data on the drives|
| Ensuring their employees cannot access your data    | Understanding the risk of using EC2 instance store|

## 5.7 EC2 instance Storage - Summary

 - **EBS Volumes**
   - network drives attached to one EC2 instance at a time
   - mapped to an avaialbility zones
   - Can use EBS snapshots for backups/transferring EBS volumes across avaialbility zones
 - **AMI**
   - Create ready-to-use EC2 instance with our customizations
 - **EC2 instance store**
   - High performance hardware disk attached to our EC2 instance
   - Lost if our instance is stopped/terminated
 - **EFS**
   - Network file system, can ve attached to 100s of instances in a region

## Quiz

Which EC2 storage would you use to create a shared network file system for your EC2 instances?
 - EFS is a fully managd service that makes it easy to setup, scale, and cost-optimize file storage in the Amazon cloud

# 6. Elastic Load balancing and Auto scaling groups

## 6.1 Scalability and Hiogh Availability

**Basics**  
 - Scalability means that an application/system can handle greater loads by adapting
 - There are two kinds of scalability:
   - Vertical scalability (increase cpu power)
   - Horizontal scalability (=elasticity)
 - Scalability is linked but different to high availability

**Vertical Scalability**  
 - Vertical Scalability means increasing the size of the instance 
   - eg: upgrading from t2.micro to t2.large
 - Vertical Scalability is very common for non distributed systems, such as database
 - There's a limit to how much you can vertically scale (hardware limit)

**Horizontal Scalability**  
 - Horizontal Scalability means increasing the number of instances /systems for your application
 - Horizontal scaling implies distributed systems.
 - This is very common for web applications/modern applications
 - Its easy to horizontally scale thanks to the cloud offerings such as Amazon EC2

**High Availability**  
 - High availability usually goes hand in hand with horizontal scaling
 - High availability means running your application/system in atleast 2 Availability zones
 - The goal of high availability is to survive a data center loss (disaster)

**Summary**  
 - Vertical scaling: increase instance size ( = scale up/down)
   - from t2.nano (0.5Gb of RAM, 1vCPU) to u-12tbl.metal (12.3 TB of RAM, 448 vCpus) 
 - Horizontal Scaling: increase number of instances ( = scaling out), decrease number of instances (scaling in)
   - Auto Scaling Group
   - Load balancer
 - High Availability: Run instances for the same application across multi Availability Zones
   - Auto Scaling Group in Multi AZ mode
   - Load balancer in multi AZ Mode

**Scalability vs Elasticity vs Agility**  

 - Scalability: Ability to accomodate a larger load by making the hardware stronger (i.e scaling up) or by adding nodes (i.e scale out)
 - Elasticity: Once a system ois scalable, elasticity means that there will be some auto-scaling so that the system can scale based on the load. this is "cloud-friendly" i.e pay-per-us, match demand, optimize costs.
 - Agility(not related to scalability <ins>distractor</ins>): new IT resources are only a click away, which means that you reduce the time to make those resources available to your developers from weeks to just minutes.

## 6.2 Elastic load balancing (ELB) Overview

**What is load balancing**  
 - Load balancers are servers that forward internet traffic to multiple servers (ec2 instances) downstream

**Why use Load balancers**  
 - Spread load across multiple downstream instances
 - Expose a single point of access (DNS) to your application
 - Seamlessly handle failures of downstream instances
 - Do regular health checks to your instances
 - Provide SSL termination (Https) for your websites
 - High avaialbility across zones

**Why use ElastiC Load balancers (ELB)**  

 - An ELB is a managed load balancer
   - AWS guarantees that it will be working
   - AWS takes care of upgrades, maintenance, high avaialbility
   - AWS provides only a few configurations knob
 - It costs less to setup your own load balancer but it will be a lot more effort on your end (maintenance, integrations)
 - 3 kinds of load balancer:
   - Application Load Balancer (HTTP/HTTPS only) - Layer 7
   - Network Load Balancer (ultra-high performance, allows for TCP) = Layer 4
   - Classic Load Balancer (retiring soon) - Layer 4 and 7 (Previous generation)

## 6.3 Application Load Balancer hands on

 - Create 2 EC2 instances with the user data script to differentiate between them
 - First create 1 instance -> right click -> "Launch more like this" -> Edit instance details -> change subnet i.e change the zone now so that it is highly available
 - Verify both the instances are up via hitting the public ip
 - EC2 -> LOAD BALANCING -> Load Balancers -> Create Load balancer -> Select Application Load Balancer as we are using http over browser-based
 - 1. Configure load balancer: Provide Name and all the avaialbility zones 
 - 2. Configure security settings: it suggests to have https, we ignore for now
 - 3. Configure Security groups: create new security group -> next 
 - 4. Configure Routing: Create new target group via giving name
 - 5. Register Targets: Select the instances and use Add to registered to add them
 - 6. review and create
 - It takes some time to create, 
 - Now, use DNS name to verify if it is working and you can refresh the page to verify if it is sending request to different servers
 - In case you stop one of the instance, then elb will redirect all the calls to the instance that is up (I got 502 bad gateway once and then it was flawless)

## 6.4 Auto Scaling Groups (ASG)

**Whats an Auto Scaling Group**
 - In real life, the load on your websites and application can change
 - In the cloud, you can create and get rid of servers very quickly
 - The goal of an AutoScaling Group (ASG) is to:
   - Scale out (Add EC2 instances) to match an increased load
   - Scale in (remove EC2 instances) to match a decreased load
   - Ensure we have a minimum and a maximum number of machines running
   - Automatically register new instances to a load balancer
   - Replace unhealthy instances
 - Cost savings: Only run at an optimal capacity (principal of the cloud)
 - Define minimum size, Actual size/ Desired capacity, Maximum size of your ASG
 - Load balancer automatically registers the instances added by ASG

**Hands on**  
 - EC2 -> AUTO SCALING -> Auto Scaling Groups -> Create Auto Scaling Group 
 - 1. Choose launch template or configuration: Provide name
   - As we donot have Launch template, Create a launch template. This helps in defining the type of instances we want ASG to spinoff
     - Launch Template name
     - Amazon Machine Image (AMI): Amazon Linux 2 AMI
     - Instance type: t2.micro
     - Key pair : use laready created key
     - Network settings: Virtual Private Cloud (VPC)
     - Security groups: use already created SG
     - Storage: Default
     - Expand Advanced settings -> use User data
   - Use the template created above -> Next
 - 2. Configure Settings
   - Instance Purchase Options: Adhere to launch template
   - Network -> Subnets: select all for higher availability -> Next
 - 3. Configure Advanced options
   - Load balancing -> Attach to an existing load balancer -> Choose from Application or network load balancer target groups -> select the target group already created
   - Health checks: check ELB option as well -> Next
 - 4. Configure group size and scaling options
   - Desired Capacity: 2 (number of instances that will be created)
   - Minimum Capacity: 1
   - Maximum Capacity: 4
   - Scaling policies: None
   - Next
 - 5. Add Notifications: Next
 - 6. Add tags: Next
 - Create Auto Scaling Group
 - Now you can go to Instance Management section to verify if the instances are created
 - Verification:
   - You can verify that 2 instances are created in the INSTANCES -> instances section
   - They are registerd in the target groups via LOAD BALANCING -> Target Groups
   - Open the DNS from load balancer and see it gives you the result

## 6.5 Summary

 - High Availability vs Scalability (Vertical and horizontal) vs Elasticity vs Agility in the cloud
 - Elastic Load Balancers (ELB)
   - Disctribute traffic across backend EC2 instances, can be Multi-AZ
   - Supports health checks
   - 3 types: Application LB (HTTP-L7), Network LB (TCP-L4), Classic LB (old)
 - Auto Scaling Groups (ASG)
   - Implement Elasticity for your application, across multiple AZ
   - Scale EC2 instances based on the demand on your system, replace unhealthy
   - Integrated with the ELB

## 6.6 Quiz

Which load balancer should you use to handle hundreds of thousands of connections with low latency
 - Network Load balancer: A network load balancer can handle millions of requests per second with low-latency. It operates at Layer 4 and is best suited for load-balancing TCP, UDP and TLS traffic with ultra high-performance


## 6.7 Resources

 - https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/what-is-load-balancing.html?icmpid=docs_elbv2_console#elb-features

# 7. Amaozon S3 (Simple storage Service)

## 7.1 S3 Overview

**Basics**  
 - S3 is one of the main building blocks of AWS
 - Its advertised as "infinity scaling" storage
 - Many website use Amazon S3 as a backbone
 - Many AWS Services uses Amazon S3 as an integration as well
 - EBS snapshots are stored in S3 in backend
 - Certified cloud Practitioner requires deeper knowledge of S3

**Use Cases**  
 - Backup and Storage
 - Disaster recovery
 - Archive
 - Hybrid Cloud Storage
 - Application Hosting
 - Media hosting
 - Data lakes and big data analytics
 - Software delivery
 - Static website

**Buckets**  
 - Amazon S3 allows people to store object (files) in "buckets" (directories)
 - Buckets must have a globally unique name (across all regions and all accounts)
 - Bucktes are defined ate the region level
 - S3 looks like a global service but buckets are created in a region
 - Naming Convention
   - No uppercase
   - No Underscore
   - 3-62 characters long
   - Not an IP
   - Must start with lowercase letter or number

**Objects**  
 - Objects (files) have a key
 - The key is the full path:
   - s3://my-bucket/my_file.txt
   - s3://my-bucket/my_folder/another_folder/my_file.txt
 - The key is composed of `prefix` + *object name*
   - s3://my-bucket/`my_folder/another_folder/`*my_file.txt*
 - Theres no concept of "directories" within buckets (although the UI will trick you to think otherwise)
 - Just keys with very long names that contains slashes ("/")
 - Object values are the content of the body
   - Max Object size is 5TB (5000GB)
   - If uploading more that 5 GB, must use "multi-part upload"
 - Metadata (list of text key/value pairs - system or metadata)
 - Tags (Unicode key / value pair - upto 10) - useful for security/lifecycle
 - Version ID (if Versioning is enabled)

**S3 Hands on**  

 - S3 -> buckets -> Create Bucket -> provide uniques bucket name and region along with default options
 - [Bucket naming rules](https://docs.aws.amazon.com/AmazonS3/latest/dev/BucketRestrictions.html#bucketnamingrules)
 - Add files -> select file -> upload
 - Now, if you select the uploaded file, you will get the details about that file
 - You will see the Object url under Object Overview heading in Properties tag
 - Now, as we had chosen all the default options that means block public access included in it and hence if you click on object URL, you will not be able to access the same
 - Whereas clicking on Object Actions -> Open will open the file in new tab

## 7.1 Bucket Policy

**S3 Security**  
 - User Based
   - IAM policies - Which API calls should be allowed for a specific user from IAM console
 Resource Based
   - Bucket Policies - bucket wide rules from the S3 console - allows cross account
   - Object Access Control List (ACL) - Fine grained
   - Bucket Access Control List (ACL) - Less Common

 - Note: An IAM principal can access an S3 object if
   - the user IAM permissions allow it **OR** the resource policy allows it
   - **AND** there's no explicit DENY
 - Encryption: encrypt objects in Amazon S3 using encryption keys

**Examples**  
 - Public Access ->   Use Bucket policy (Allow S3 bucket policy)
 - IAM User Access -> IAM Policy only will be sufficient
 - EC2 Instance -> Create EC2 instance role and assign IAM permissions to this role
 - Cross-Account access -> S3 bucket policy allow cross account policy

**Policy**  
 - JSON based Policies
   - Resources: buckets and Objects
   - Actions: Set of API to allow or Deny
   - Effect: Allow/Deny
   - Principal: The Account or user to apply the policy to
 - Use S3 bucket for policy to:
   - Grant public access to the bucket
   - Force Objects to be encrypted at upload
   - Grant Access to another Account (Cross Account)

**Bucket Settings for Block public access**  
[Screenshot]

 - These settings were created to prevent company data leaks
 - If you know your bucket should never be public, leave thse on
 - Can be set at the account level

**Hands On**  

 - go to S3 bucket created above -> permissions -> Bucket policy
 - To enable this, you have to uncheck "block public access" policies
 - Once done, you can click on edit button in edit bucket policy 
   - Select "policy generator" as it provides a nice ui to generate a policy -> select
   - Also notice you have Bucket ARN that will be used in next steps
   - Select type of policy: S3 bucket policy
   - Principal: *
   - Actions: getObject
   - ARN: copy from the step above with `/*`
   - Add statement
   - Generate Policy -> copy content 
   - now go back to previous tab and update the copied policy and save
   - now you will have the objects inside this bucket as accessible

## 7.2 S3 Websites

**basics**  
 - S3 can host static websites and have them accessible on the www
 - The website URL will be:
   - <bucket-name>.s3-website-<aws-region>.amazonaws.com or
   - <bucket-name>.s3-website.<aws-region>.amazonaws.com
 - If you get a 403 (Forbidden) error, make sure the bucket policy allows public reads

**hands on**  
 - upload your static content
 - in Properties tab -> Static website hosting -> Enable
 - host a static wbesite
 - provide name of your index and error document
 - save
 - now you get the url for the newly hosted website
 
## 7.3 S3 Versioning

**basics**
 - you can version your files in Amazon S3
 - It is enabled at the biucket level
 - Same key overrite will increment the version: 1,2,3..
 - It is best practice to version your buckets
   - protect against unintended deletes (ability to restore a version)
   - Easy roll back to previous version
 - Notes: 
   - Any file that is not versioned prior to enabling versioning will have version null
   - Suspending versioning does not delete the previous versions

**hands on**
 - S3 -> Select the bucket you created above -> properties tab -> Bucket versioning -> edit -> Enable -> Save changes
 - Now any file uploaded from now on will have version in it
 - you can select the file and click on versions tab you will see the versions
 - Also in S3 bucket level -> Objects section -> List Versions and you will see the versions of the file
 - you can select the version you want to rollback and delete that so it will be rolled back to the previous version
 - Deleting a file with list versions enabled will do a soft delete.
   - To get back this file you have to enable List versions and then you will see the deleted file with "Delete marker" and then select delete tp restore

## 7.4 S3 Access logs

**basics**  
 - For audit purpose, you may want to log all access to S3 buckets
 - Any request made to S3, from any account, authorized or denied will be logged into another S3 bucket
 - That data can be analyzed using data analysis tools..
 - Very helpful to come down to the root cause of an issue, or audit usage, view suspicious patterns, etc..

**Hands on**  
 - To enable logging you have to create a new bucket where access logs will be written
 - Go to original S3 bucket -> Properties -> Server access logging setting -> edit -> enable and provide the target bucket that we created above.
 - You can access the objects and then these logs will be reflected in another s3 bucket after an hour or two.

## 7.5 S3 Replication (CRR and SRR)

**basics**  
 - Must enable versioning in source and destination
 - Cross Region Replication (CRR) 
 - Same Region Replication (SRR)
 - Buckets can be in different accounts
 - Copying is asynchronous
 - Must give proper IAM permissions to S3
 - CRR use cases
   - Compliance
   - lower latency access
   - Replication across accounts
 - SRR use cases
   - log aggregation
   - live replication between production and test accounts

**hands on**  
 - create a new S3 bucket where you need data to be replicated
 - enable versioning in source and target bucket
 - go to main bucket -> management tab -> Replication rule -> Create replication rule
   - provide rule name
   - status : enabled
   - Source bucket
   - Destination: buckte in this account, provide the name
   - IAM role: Create a new role
   - Save
   - Replication rule created
 - Replication will work only for objects that are being uploaded after enabling the replication rule

## 7.6 S3 Storage classes

**Types**  
 - Amazon S3 Standard - General purpose
 - Amazon S3 Standard-Infrequent Access (not accessed ver often)
 - Amazon S3 one Zone-Infrequent Access (you can recreate and fine with losing it)
 - Amazon S3 Intelligent tiering (Not sure which one to choose between frquent and infrequent access)
 - Amazon Glacier (Backups and archives)
 - Amazon Glacier Deep Archive (Backups and archives)

**Durability and Availability**  
**Durability:**  
 - High durability (99.99999999999, 11 time 9) of objects across multiple Azure
 - If you store 10,000,000 objects with Amazon S3, you can on average expect to incur a loss of a single object once every 10,000 years
 - `Same for all storage classess`

**Availability**  
 - Measures how readily available a service is
 - S3 standard has 99.99% availability, which means it wil not be available 53 minutes a year
 - `Varies depending on storage class`

** 1. Amazon S3 Standard - General purpose**  
 - 99.99% availability
 - Used for frequently accessed data
 - low latency and high throughput
 - sustain 2 concurrent facility failures
 - Use cases:
   - Big Data analytics
   - Mobile and gamin applications
   - content distribution

** 2. Amazon S3 Standard-Infrequent Access (IA)**  
 - Suitable for data that is less frequently accessed, but requires rapid access when needed
 - 99.9% Availability
 - Lower cost compared to Amazon S3 standard, but retrieval fee
 - Sustain 2 concurrent facility failures
 - Use Cases: 
   - As a data store for disaster recovery
   - backups

** 3. Amazon S3 one Zone-Infrequent Access (IA)**  
 - Same as IA but data is stored in a single Azure
 - 99.5% Availability
 - Low latency and high throughput performance
 - Lower cost compared to S3-IA (by 20%)
 - Use Cases:
   - Storing secondary backup copies of on premise data or
   - storing data you can recreate

** 4. Amazon S3 Intelligent tiering**  
 - 99.9% Availability
 - Same low latency and high throughput performance of S3 Standard
 - Cost optimized by automatically moving objects between two access tiers based on changing access patterns:
   - frequent access
   - Infrequent access
 - Resilient against events that impact an entire Availability zone

** 5. Amazon Glacier and Amazon Glacier Deep Archive**  
 - Low cost object storage (in GB/month) meant for archiving/backup
 - Data is retained for the longer term (years)
 - Various retrieval options of time + fees for retrieval
 - Amazon Glacier: Cheap
   - Expedited (1 to 5 minutes)
   - Standard (3 to 5 hours)
   - Bulk (5 to 12 hours)
 - Amazon Glacier Deep Archive: Cheapest
   - Standard (12 hours)
   - Bulk (48 hours)

**Summary**  
 - https://aws.amazon.com/s3/storage-classes/

**Moving between storage classes**  
 - You can transition objects between storage classes
 - For infrequently accessed object, move them to Standard_IA
 - For archive objects you dont need in real-time, GLACIER or DEEP_ARCHIVE
 - Moving Objects can be automated using a lifecycle configuration

**Hands on**  
 - S3 -> Objects -> upload -> Additional upload options, here you can select the storage class and details are also available on the same -> upload
 - if you select the uploaded file, yyou can verify the storage class and you can update the same if needed
 - S3 -> Buckets -> Select bucket -> management tab -> Create lifecycle rule
   - LifeCycle Rule name
   - Choose a rule scope
   - Lifecycle Rule actions: depending on the checkboxes you select, you will be provided with the options to configure below
   - Create Rule

## 7.7 Snowball, Snowball Edge and SnowMobile Overview

**Snowball**  
 - Physical data transport solution that heps moving TBs or PBs of data in or out of AWS
 - Alternative to moving data over the network (and paying network fees)
 - pay per data transfer jobs
 - Use cases:
   - LArge data cloud migrations
   - Data center decommision
   - Disaster recovery
 - if it takes more than a week to transfer over the network, use snowball devices

**Snowball Process**  
 - Request snowball devices from the AWS console for delivery
 - Install the snowball client on your servers
 - Connect the snowball to your servers and copy files using the client
 - Ship back the device when you are done (goes to the right AWS facility)
 - Data will be loaded into an S3 bucket
 - Snowball is completely wiped

**Snowball Edge**  
 - Snowball Edge (100 TB) add computational capability to the device
 - Supports a custom EC2 AMI so you cab perform processing on the go
 - Supports customm lambda functions
 - Very useful to pre-process the data while moving
 - Use case:
   - data migrations
   - image collation
   - IoT capture
   - Machine Learning
 - "Snowball" is deprecated in favour of "Snowball Edge"

**AWS Snowmobile (Truck)**  
 - Transfer exabytes of data (1 EB = 1,000 PB = 10,000,00 TBs)
 - Each Snowmobile has 100PB of capacity (use multiple in parallel)
 - Better than snowball if you transfer more than 10 PB

## 7.8 Storage gateway overview

**Where do we need?**  
 - AWS is pushing for "hybrid cloud"
   - Part of your infrastructure is on-premises
   - Part of your infrastructure is on the cloud
 - This can be due to
   - Long cloud migrations
   - Security requirements
   - Compliance requirements
   - IT strategy
 - S3 is a propritary storage technology (unlike EFS/NFS), **so how do you expose the S3 data in-premise?**
    - via AWS Storage Gateway

**AWS Storage Cloud Native Options**  
 - Block storage
   - Amazon EBS
   - EC2 instance store
 - File Syorage
   - Amazon EFS
 - Object storage
   - Amazon S3
   - Glacier

**AWS storage gateway**  
 - Bridge between on-premise data and cloud data in S3
 - Hybrid storage service to allow on-premises to seamlessly use the AWS Cloud
 - Use cases:
   - Disaster recovery
   - Backup and restore
   - Tiered storage
 - Types of storage gateway
   - File gateway
   - Volume gateway
   - Tape gateway
 - No need to know the types at the exam

## 7.9 Shared responsibility model for S3

| AWS                                                 | You                           |
| -------------                                       |:-------------:                      |
| Infrastructure (global security, durability, availability, sustain concurrent loss of data in two facilities) | S3 Versioning |
| Configuration and vulnerability analysis            | S3 Bucket Policies|
| Compliance Validation                               | S3 Replication Setup |
|                                                     | Logging and Monitoring |
|                                                     | S3 Storage Classes |
|                                                     | Data encryption at rest and in transit |

## 7.10 S3 Summary

 - Buckets vs Objects: global unique name, tied to a region
 - S3 security: IAM policy, S3 bucket Policy (public access), S3 encryption
 - S3 Websites: host a static website on Amazon S3
 - S3 Versioning: Multiple versions for files, prevents accidental deletes
 - S3 Access Logs: Log requests made within your S3 buckets
 - S3 Replication: Same-region or Cross-Region, must enable versioning
 - S3 Storage Classes: Standard. IA, IZ-IA, Intelligent, Glacier, Deep Archive
 - S3 Lifecycle Rules: transition objects between classes
 - Snowball/Snowmobile: import data into S3 through a physical device
 - Storage gateway: hybrid solution to extend on-premises storage to S3

## Quiz


# 8. Databases Introduction

**Basics**  
 - Storing data on disk (EFS, EBS, EC2 instance Store, S3) can have its limits
 - Sometimes, you want to store data in a database, you can structure the data
 - You build indexes to efficientlt quey/search through the datasets
 - Databases are optimized for a purpose and come with different features, shapes and constraints

**Relational Databases**  
 - Looks just like excel spreadsheets, with links between them

**NoSQL Databases**
 - NoSQL - non-SQL = non relational databases
 - NoSQL databases are purpose built for specific data models and have flexible schemes for building modern applications.
 - Benefits:
   - Flexibility: Easy to evolve data model
   - Scalability: designed to scale-out by using distributed clusters
   - High-performance: optimized for a specific data model
   - Higly functional: types optimized for the dta model
 - Examples:
   - key-value
   - documents
   - graph
   - in-memory
   - search databases
 - data example: JSON
   - JSON = JavaScript Object Notation
   - JSON is a common for of data that fits into a NoSQL model
   - Data can be nested
   - Fields can change over time
   - Support for new types: arrays, etc

**Databases and shared Responsibility on AWS**  
 - AWS offers use to manage different databases
 - Benefits:
   - Quick provisioning, High Availability, Vertical and Horizontal Scaling
   - Automated Backup and Restore, Operations, Upgrades
  - Operating system patching is handled by AWS**
  - Monitoring, alerting

Note: Many database technologies could be run on EC2, but you must handle yourself the resiliency, backup, patching, high availability, fault tolerance, scaling,..

## 8.1 AWS RDS Overview

**basics**  
 - RDS stands for Relational Database Service
 - Its a managed DB Service for DB using SQL as a query language
 - It allows you to create databases in the cloud that are managed by AWS
   - Postgres
   - MySQL
   - MariaDB
   - Oracle
   - Microsoft SQL Server
 - Aurora (AWS Proprietary database)

**Advantage of using RDS over deploying DB on EC2**  
 - RDS is a managed service:
   - Automated provisioning, OS patching
   - Continous backups and restore to specific timestamp (point in time Restore)
   - Monitoring dashboards
   - Read replicas for improved read performance
   - Multi AZ setup for Disaster Recovery
   - Maintenance windows for upgrades
   - Scaing capability (Vertical and horizontal)
   - Storage backed by EBS (type may be gp2 or io1)
 - **You cant SSH into your instances**

**Amazon Aurora**  
 - Aurora is a proprietary technology from AWS (not open sourced)
 - PostgreSQL and MySQL are both supported as Aurora DB
 - Aurora is "AWS cloud optimized" and claims 5x performance improvement over MySQL on RDS. over 3x the performance of Postgres on RDS
 - Aurora storage automatically grows in increments of 1-GB, up to 64 TB
 - Aurora costs more than RDS (20% more) - but is more efficient
 - Not in the free tier

**hands on**  
 - RDS -> Databases -> create databases 
   - creation method: standard create and easy create, we will select standard
   - Engine options: MySQL
   - Templates: Free tier
   - DB interface identidier: provide name for eg: databasedemo
   - Credentials settings: 
     - Master username: admin
     - Master password: 
     - Confirm password
   - Instance type: t2.micro
   - All other default values
   - Create database

## 8.2 Amazon ElasticCache 

**basics**  
 - The same way RDS is to get managed Relational Databases, ElasticCache is to get managed Redis or Memcached
 - Caches are in-memory databases with **high performance, low latency**
 - Helps reduce load off databases for read intensive workloads
 - AWS takes care of OS maintenance/patching, optimizations, setup, configuration, monitoring, failure recovery and backups

## 8.3 DynamoDB

**basics**  
 - Fully managed highly available with replication across 3 Azure
 - No SQL database - not a relational database
 - Scales to massive workloads, distributes **"serverless"** database
 - Millions of requests per seconds, trillions of row, 100s of TB of storage
 - Fast and consistent in performance
 - **Single-digit millisecond latency - low latency retrieval**
 - Integrated with IAM for security, authorization and administration
 - Low cost and auto scaling capabilities
 - Type of data:
   - key/value database
   - https://aws.amazon.com/nosql/key-value/

**hands on**  
 - DynamoDB -> Create table
   - tablename: 
   - primary key: 

## 8.4 Redshift Overview

 - Redshift is based on PostgresSQL, but its not used for Online transaction processing (OLTP)
 - Its used for OLAP - Online Analytical Processing (analytics and data warehousing)
 - Load data once every hour, not every second
 - 10x better performance than other data warehouses, scales to PBs of data
 - Columnar storage of data (instead of row based)
 - Massively Parallel Query Execution (MPP), highly available
 - Pay as you go based on the instances provisioned
 - Has a SQL interface for performing the queries
 - BI tools such as AWS Quicksight or Tableau integrate with it

## 8.5 AWS EMR

 - EMR stands for "Elastic MapReduce"
 - EMR helps creating Hadoop clusters (Big Data) to analyze and process vast amount of data
 - The clusters can be made of hundreds of EC2 instances
 - Also supports Apache Spark, HBase, Presto, Flink
 - EMR takes care of all the provisioning and configuration
 - Auto scaling and integrated with spot instances
 - Use Cases:
   - Data Processing
   - Machine Learning
   - Web Indexing
   - Big Data

## 8.6 AWS Athena

 - Fully Serverless database with SQL capabilities
 - Used to query data in S3
 - Pay per query
 - Output results back to S3
 - Secured through IAM
 - Use Case: 
   - one time SQL queries
   - queries
   - serverless queries on S3
   - log analytics

## 8.7 AWS DMS

 - Data Migration Service (Source DB ---> (EC2 Instance Running DMS) ---> Target DB)
 - Quickly and securelt migrate databases to AWS, resilient, self healing
 - The Source database remains available during the migrations
 - Supports:
   - Homogeneous migrations, eg: Oracle to Oracle
   - Heterogenous migrations: eg: SQL Server to Aurora

## 8.8 AWS Glue

 - Manages extract, transform, and Load (ETL) service
 - Useful to prepare and transform data for analytics
 - Fully Serverless service
 - Glue Data Catalog: catalog of datasets
   - Can be used by Athena, Redshift, EMR to provide metadata

## 8.9 Summary

 - Relational Database - OLTP: RDS and Aurora (SQL)
 - In-memory database: ElasticCache
 - Key/Value Databse: DynamoDB (serverless)
 - Warehouse - OLAP: Redshift (SQL)
 - Hadoop Cluster: EMR
 - Athena: query data on Amazon S3 (Serverless and SQL)
 - Glue: Managed ETL (extract Transform Load) and Data Catalog service
 - Database Migration: DMS

Quiz:

# 9. Compute Services Overview

## 9.1 What is Docker

**basics**  
 - Docker is a software development platform to deploy apps
 - Apps are packaged in containers that can be run on any OS
 - Apps run the same, regardless of where they're run
   - Any machine
   - No Compliance issues
   - Predictable behaviour
   - Less work
   - Easier to maintain and deploy
   - Works with any language, any OS, any technology

**Docker on an OS**  
 - SIngle EC2 instance will have docker running Java, docker runnning MySql

**Where docker images are stored**  
 - Docker images are stored in Docker repositories
 - Public repository: Docker Hub (https://hub.docker.com)
   - Find base images for may technologies or OS:
     - Ubuntu
     - MySQL
     - NodeJS
     - Java
 - Private Repository: Amazon ECR (Elastic COntainer Registry)  

**Docker vs Virtual machines**
 - Docker is "sort of" a virtualization technology, but not exactly
 - Resources are shared with host -> many containers on one server

## 9.2 ECS, Fargate and ECR 

**ECS**  
 - ECS stands for Elastic Container Service
 - Launch Docker containers on AWS
 - **You must provision and maintain the infrastructure (the EC2 instances)**
 - AWS takes care of starting/stopping containers
 - Has integrations with the Application Load Balancer

**Fargate**  
 - Launch Docker containers on AWS
 - You **do not provision the infrastructure (no EC2 instances to manage)** - simpler than ECS
 - Serverless Offering
 - AWS just runs containers for you based in the CPU/RAM you need

**ECR**
 - Elastic Container Registry
 - Private Docker Registry on AWS
 - This is where you store your Docker images so they can be run by ECS or Fargate

## 9.3 Serverless introduction
 - Serverless is a new paradigm in which the developers dont have to manage servers anymore
 - they just deploy code, functions
 - Initially Serverless == Faas (Function as a Service)
 - Serverless was pioneered by AWS Lambda but now also includes anything that's managed: "databases, messaging, Storage, etc"
 - Serverless does not mean there are no servers, it just means as a end user you just dont manage/provision/see them
 - Serverless services we saw till now:
   - S3
   - DynamoDB
   - Fargate
   - Lambda

## 9.4 AWS Lambda

**Why Lambda**  
| AWS EC2                                           | AWS Lambda                               |
| -------------                                     |:-------------:                           |
| Virtual servers in the cloud                      | Virtual Functions - no servers to manage |
| Limited by RAM and CPU                            | Limited by time - short executions       |
| Continously Running                               | Run on demand                            |
| Scaling means intervention to add/remove servers  | Scaling is automated                     |

**Benefits**  
 - Easy pricing:
   - Pay per request and compute time
   - Free tier of 10,000,00 AWS Lambda requests and 4,000,00 GBs of compute time
 - Integrated with the whole AWS suite of services
 - Event-Driven: functions get invokded by AWS when needed
 - Integrated with many programming languages
 - Easy monitoring through AWS Cloudwatch
 - Easy to get more resources per functions (upto 3GB of RAM)
 - Increasing RAM will also improve CPU and Network

**Languages supported**  
 - Node.js (JavaScript)
 - Python
 - Java (Java 8/11 compatible)
 - C# (.NET Core)
 - Golang
 - C#/Powershell
 - Ruby
 - Custom Runtime API (Community supported example Rust)
 - **Important: Docker is not for AWS Lambda, its for ECS/Fargate**

**Examples:**  
 - Serverless thumbnail creation
 - Serverless CRON job

**Pricing Example**  
 - Detailed pricing information: https://aws.amazon.com/lambda/pricing/
 - Pay per calls:
   - First 10,000,00 requests are free (in free tier)
   - $0,20 per 1 million requests thereafter ($0.0000002 per request)
 - Pay per duration: (in increment of 1ms)
   - 4,000,00 GB seconds of compute time per month if Free
   - == 4,000,00 seconds if function is 1 GB RAM
   - == 32,000,00 seconds if function is 128 MB RAM
 - After this $1.00 for 6,000,00 GB-seconds
 - It is usually very cheap to run AWS Lambda so its very popular

**hands on**  
 - Lambda -> you do not get the begin screen, to get that replace the last  word in URL with begin 
   - eg: https://us-east-2.console.aws.amazon.com/lambda/home?region=us-east-2#/begin
   - here you can explore the Lambda via going Next
 - Lambda -> Functions -> Create Function
   - Select blueprint -> hello-world-python blueprint -> configure
   - Basic information -> Function name: demo-lambda
   - Keep evrything default -> Create function -> Lambda Function created
 - To test the created lambda: Test -> provide name -> create -> test
 - Basic settings -> configure memory(max 3008 MB) and timeout(max 15 mins) setting
 - Monitoring tab provides you the place to monitor

## 9.5 AWS Batch

**basics**  
 - Fully Managed batch processing at any scale
 - Efficint run 1,000,00s of Computeing batch jobs on AWS
 - A "batch" job is a jo with a start and an end (opposed to continous)
 - Batch will dynamically launch EC2 instances or SPOT instances
 - AWS Batch provisions the righ amount of compute/memory
 - You submit or schedule batch jobs and AWS batch does the rest
 - Batch Jobs are defined as Docker images adn run on ECS
 - Helpful for cost optimizations and focusing less on the infrastructure

**Batch vs Lambda**  
 - Lambda:
   - Time limit
   - Limited runtimes ex java, python..
   - Limited temporary disk space
   - Serverless
 - Batch:
   - No time limit
   - Any runtime as long as its packages as Docker image
   - rely on EBS/instance store for disk space
   - Relies on EC2 (can be managed by AWS)

**Amazon LightSail**  

**basics**  
 - Virtual Servers, Storage, databases, and networking
 - Low and predicatble pricing
 - Simpler alternative to using EC2, RDS, ELB, EBS, Route 53
 - Great for people with little cloud experience
 - Can setup notifications and monitoring of your lightsail resources
 - Use cases:
   - Simple web applications (has templates for LAMP, Nginx, MEAN, Node.js, etc)
   - Websites (templates for Wordpress, Magento, Plesk, Joomla)
   - Dev/Test environment
 - Has High availability but no auto-scaling, limited aws integrations

## 9.6 Summary

**Other Compute Services**  
 - Docker: Container technology to run applications
 - ECS: Run Docker containers on EC2 instances
 -- Fargate:
   - Run Docker containers without provisioning the infrastructure
   - Serverless offering (No EC2 instances)
 - ECR: Private Docker images repository
 - Batch: Run Batch jobs on AWS across managed EC2 instances
 - LightSail: Predictable and low pricing for simple application and DB stacks

**Lambda Summary**
 - Lambda is Serverless, Function as a Service, Seamless scaling, reactive
 - Lambda billing:
   - By the time run **X** by the RAM provisioned
   - By the number of invocations
 - Language Support: Many programming languages except docker
 - Invocation Time: upto 15 minutes
 - Use Cases:
   - Create thumbnails for images uploaded into S3
   - Run a Serverless Cron job

# 10. Deployments and managing infrastructure at scale

## 10.1 Cloud Formation

**basics**  
 - CloudFormation is a declarative way of outlining your AWS infrastructure, for any resources (Most of them are supported).
 - For Example: Within a CloudFormation template, you say:
   - I want a security group
   - I want two EC2 instances using this security group
   - I want an S3 bucket
   - I want a load Balancer (ELB) in front of these machines
 - Then CloudFormation creates those for you, in the right order, with the exact configuration that you specify

**benefits**  
 - Infrastructure as a Code:
   - No resources are manually created, which is excellent for control
   - Changes to the infrastructure are reviewed through code
 - Cost:
   - Each resources within the stack is tagged with an identifier so you can easily see how much a stack costs you
   - you can estimate the costs of your resources using the ClopudFormation template
   - Savings strategy: In Dev, you could automate deletion of templates at 5 pm and recreated at 8 am safely
 - Productivity:
   - Ability to destroy and re-create an infrastructure on the cloud in the fly
   - Automated generation of Diagram for your templates
   - Declarative programming (no need to figure out ordering and orchestration)
 - Dont reinvent the wheel:
   - Leverage existing templates on the web
   - Leverage the documentation
 - Supports (almost) all AWS resources
   - Everything we will see here is supported
   - You can use "Custom resources" for resources that are not supported

**CloudFormation Stack Designer**  
 - We can see all the resources
 - We can see the relationships between the components

**hands on**  
 - CloudFormation -> Create Stack -> multiple options and can be created via designer

## 10.3 Beanstalk Overview

**basics**  
 - Typical Architecture: Webapp 3 tier
   - ELB (load balancer) ---- Auto Scaling Group of EC2 instances ---- ElasticCache/RDS

**developer problems on AWS**  
 - Dont want to manage infrastructure, just want to Deploy code
 - Configureing all the databases, load balancers, etc
 - Scaling concerns
 - Most web apps have the same architecture (ALB + ASG)
 - All developers want is for their code to run
 - Possibly, consistently across different applications and environments

**Elastic Beanstalk**  
 - Elastic Beanstalk is a developer centric view of deploying an application on AWS
 - It uses all the component's we have seen before: EC2, ASG, ELB, RDS, etc..
 - But its all in one view thats easy to make sense of
 - we still have full control over the configuration
 - Beanstalk = Platform as a Service (PaaS)
 - Beanstalk is free but you pay for the underlying instances
 - Managed Service
   - Instance configuration/ OS is handled by Beanstalk
   - Deployment strategy is configurable but performed by Elastic Beanstalk
 - Just the application code is the responsibility of the developer
 - Three architecture models:
   - Single instance deployment: good for dev
   - LB + ASG: great for production or pre-production web applications
   - ASG only: great for non-web apps in production (workers, etc)
 - Support for many platforms, 2 eg below:
   - Java Se
   - Java with Tomcat

**hands on**  
 - Beanstalk -> Create Application -> 
   - Name: DemoApp
   - Platform:
     - platform: Java
     - recommended branch and version are autopoulated
   - Application code
     - Sample application
   - Create Application
 - This internally uses CloudFormation to create the complete environment, this can be verified with 
   - CloudFormation -> Stacks -> you will see a stack with "CREATE_IN_PROGRESS"
   - If you select this stack 
     - you can see in tags beanstalk 
     - events has all the events occured
     - Resources tells you about all the resources created
     - Template: it has the template used by BeanStalk
   - EC2 -> instances - yu will find the instance created by BeanStalk
 - It takes almost 5 minutes to create this. once done, you have an url where you can acces the same
 - <yourAppName> -> Configuration

**CloudFormation vs BeanStalk**  

**Resources**  
 - https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/Welcome.html
 - https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/concepts.html 

## 10.4 AWS CodeDeploy
 - We want to deploy our application automatically
 - Works with EC2 instances
 - Works with On-premises servers
 - Hybrid service
 - Servers/Instances must be provisioned and configured ahead of time with the CodeDeploy Agent

## 10.5 AWS Systems Manager (SSM)
**basics**  
 - Helps you manage your EC2 and On-Premises systems at scale, Hence Hybrid AWS Service
 - Get Operational insights about the state of your infrastructure
 - Suite of 10+ products
 - Most important features are:
   - Patching automation for enhanced compliance
   - Run commands across an entire fleet of servers
   - Store parameter configuration with the SSM Parameter Store
 - Works for both Windows and Linux OS

**How Systems Manager works**  
 - We need to install the SSM agent onto the systems we control
 - Installed by default on Amazon Linux AMI and some Ubuntu AMI
 - If an instance cant be controlled with SSM, its probably and issue with the SSM agent
 - Thanks to the SSM Agent, we can run commands, patch and configure our servers

## 10.6 OpsWorks Overview
**basics**  
 - Chef and Puppet help you perform server configuration automatically, or repetitive actions
 - They work great with EC2 and On-Premises VM
 - AWS OpsWorks = Managed Chef and Puppet
 - Its and alternative to AWS SSM
 - Only provision standard AWS resources:
   - EC2 instances, Databases, Load Balancers, EBS volumes..
 - In the exam: Chef or Puppet needed => AWS OpsWorks

## 10.7 Summary 
 - CloudFormation (AWS Only):
   - Infrastructure as a Code, works with almost all of AWS resources
   - Repeat across Regions and Accounts
 - BeanStalk (AWS Only): 
   - Platform as a Service (PaaS), limited to certain programing languages or Docker
   - Deploy code consistently with a known architecture, eg: ALB+EC2+RDS
 - CodeDeploy (Hybrid): Deploy and Upgrade any application onto servers
 - Systems Manager (Hybrid): Patch, Configure and run commands at scale
 - OpsWorks (Hybrid): Managed Chef and Puppet in AWS

Quiz

## 11 Global Applications 

**Why make a Global Application?**  
 - A global application is an application deployed in multiple geographies
 - On AWS: this could be Regions and/or Edge locations
 - **Decreased Latency:**  
   - Latency is the time it takes for a network packet to reach a server
   - It takes time for a packet rom Asia to reach the US
   - Deploy your applications closer to your users to decrease latency, better experience.
 - **Disaster Recovery (DR)**  
   - If an AWS region goes down (earthquake, storms, power shutdown, politics), you can failover to another region and have your application still working
   - A DR plan is important to increase the availability of your application
 - **Attack Protection:** distributed global infrastructure is harder to attack

**Global AWS Infrastructure**  
 - Regions: For deploying applications and infrastructure
 - Availability zones: Made of multiple data centers
 - Edge Locations (Points of Presence): For content delivery as close as possible to users
 - More at: https://infrastructure.aws/

**Global Apps**  
 - **Global DNS: Route 53**
   - Great to eoute users to the closest deployment with least latency
   - Great for disaster recovery strategies
 - **Global Content Delivery Network (CDN): CloudFront**
   - Replicate part of your application to AWS Edge Locations - decrease latency
   - Cache common requests - improved user experience and decreased latency
 - **S3 Transfer Acceleration**
   - Accelerate global uploads and downloads into Amazon S3
 - **AWS Global Accelerator**
   - Improve global application availability and performance using the AWS global network

## 11.1 Amazon Route 53
**basics**  
 - Route53 is a managed DNS (Domain Name System)
 - DNS is a collection of rules and records which helps clients understand how to reach a server through URLs
 - In AWS, the most common records are:
   - www.google.com => 12.34.56.78 = A record (IPv4)
   - www.google.com => 2001:0db9:99a9:0000:0000:9a9e:9999:9889 == AAAA IPv6
   - search.google.com => www.google.com == CNAME: hostname to hostname
   - example.com => AWS resource == Alias (eg: ELB, CloudFront, S3, RDS, etc)
 - **Routing Policies**
   - Simple Routing Policy (No Health checks)
   - Weighted Routing Policy (Distribute traffic across multiple instances)
   - Latency Routing Policy (Minimize Latency)
   - Failover Routing Policy (helps in Disaster Recover)
**hands on**  
 - Create 2 EC2 instances in 2 different regions (Note the ip for easy access later)
 - Route 53 -> Domain registration -> provide details -> register
 - Route 53 -> Hosted zones -> Create Record Set
   - Name: www (and the domain you bought above is already available)
   - Type: A - ipv4 address
   - Value: provide ip of any one instance
   - Routing Policy: Latency
   - Region: select region
   - Set ID: my region <name > access
 - Repeat the process  with another ip

## 11.3 CloudFront
**basics**  
 - Content Delivery Network (CDN)
 - Improves read performance, content is cached at the edge
 - Improves users experience
 - 216 Points of Presence globally (edge locations)
 - DDoS protection (because worldwide), integration with Shield, AWS Web Application Firewall
 - https://aws.amazon.com/cloudfront/featuresp

**CloudFront Origins**  
 - From S3 bucket:
   - For distributing files and caching them at the edge
   - Enhanced security with CloudFront Origin Access Identity (OAI)
   - CloudFront can be used as an ingrass (to upload files to S3)
 - From Custom Origin (HTTP):
   - Application Load balancer
   - EC2 Instance
   - S3 website (must first enable the bucket as a static S3 webisite)
   - Any Http backend you want

**CloudFront vs S3 Cross region Replication**  
 - CloudFront:
   - GlobalEdge network
   - Files are cached for a TTL (may be a day)
   - Great for static content that muste be available everywhere
 - S3 Cross Region Replication
   - Must be setup for each region you want replication to happen
   - Files are updated in near real-time
   - Read only
   - Great for dynamic content that needs to be available at low-latency in few regions

**hands on**  
 - Create S3 bucket without bucket policies to expose publicly
 - Cloudfront -> Create Distribution -> Web distribution -> Get started

## 11.4 S3 Transfer acceleration

 - Increase transfer speed by transferring file onto an AWS edge location which will forward the data to the S3 bucket in the target region
 - Tool: https://s3-accelerate-speedtest.s3-accelerate.amazonaws.com/en/accelerate-speed-compaison.html

## 11.5 AWS Global Accelerator**

 - Improve global application availability and performance using the aws global network
 - Leverage the AWS internal network to optimize the route to your application (60% improvement)


