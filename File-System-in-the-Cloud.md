# Setup File System in the Cloud

## Learning Objectives

- Setup Amazon Elastic File System
- Create a mount target for the pet client photos repository

## Goals

### Practice Lab Goals

- Configure adn deploy an Amazon Elastic File System.
- Mount EFS in two EC2 Instances.

### DIY (Do It Yourselft) Goals

- Mount an EFS endpoint to the third EC2 Instance.
- Test if the file are accessible from the EC2 Instance.

<p align="center"><img src="./assets/file-system-in-the-cloud/01.PNG"></p>

# Practice for Lab Goals

## File Systsem in the Cloud using Amozone EFS

### Step 1

1. Review the lab objectives in the concepts field.
2. For practice you can use amzone free tier account.
3. Please follow the lab instructions carefully and use the arrows below to navigate between steps.

#### Concept

in the lab you will :

- Launch and configure an Amazon EFS file system.
- Mount the file system to an Amazon EC2 instance.
- Connect a second Amazon EC2 Instance to the same file system.
- Share file between the two Amazon EC2 instances.

### Step 2

1. In the Service search bar, type: `ec2`
2. Click EC2.
3. Go to the next step.

<p align="center"><img src="./assets/file-system-in-the-cloud/02.PNG"></p>

#### Concept

Amazon EFS provide a simple, service, set and forget, elastic file system that let you share file data without provisioning and manage storage.

### Step 3

1. On the left menu, click Instances.
2. Go to the next step.

#### Concept

With Amazon EFS, you can grow and shrink your file system automatically as you add adn remove files, eliminating the need to provision and manage capacity to accommodate growth.

### Step 4

1. Review the names of the three existing instances.
   - In this case : `first create 3 ec2 instance with separate availability zone each instance`
2. Scroll to the right.
3. Go to the next step

<p align="center"><img src="./assets/file-system-in-the-cloud/03.PNG"></p>

#### Concept

Amazon EFS creates a shared storage file system available concurrantly to multiple instance.

### Step 5

1. Under Availability Zone, review the Availability Zone for each instance.
2. On the left menu, click Security Groups.
3. Go to the next step.

<p align="center"><img src="./assets/file-system-in-the-cloud/04.PNG"></p>

#### Concept

After creating an Amazon EFS file system, you create mount target on each subnet. The mounts target enables communication from instances on the subnet. Amazon EFS file system uses the Network File System (NFSv4) protocol. Instances that connect to teh file system are NFS Client.

### Step 6

1. Review the webserver security group which is already linked to the web servers.
2. Click Create security group.
3. Go to the next step.

<p align="center"><img src="./assets/file-system-in-the-cloud/06.PNG"></p>

#### Concept

When you create an Amazon EFS mount target, you must attach a security group. The security groups determines which instances can access teh file system as NFS clients.

### Step 7

1. Under Security group name, type: `PetModels-EFS-1-SG`
2. Under Description, type: `Restrict access to webservers only`
3. Under VPC, choose PetModels.
   - You may need to remove the existing VPC by clicking X.
4. Under Inbound rules, click Add rule.
5. Go to the next step.

<p align="center"><img src="./assets/file-system-in-the-cloud/07.PNG"></p>

#### Concept

Security groups are linked to a single VPC. You can assign a security group to one or more instances, but each instance must be in the same VPC as the security group.

### Step 8

1. Under Type, choose NFS.
2. Under source, choose the webserver security group.
3. Go to the next step.

### Step 9

<p align="center"><img src="./assets/file-system-in-the-cloud/09.PNG"></p>

#### Consept

### Step 10

<p align="center"><img src="./assets/file-system-in-the-cloud/10.PNG"></p>

#### Consept

### Step 11

<p align="center"><img src="./assets/file-system-in-the-cloud/11.PNG"></p>

#### Consept

### Step 12

<p align="center"><img src="./assets/file-system-in-the-cloud/12.PNG"></p>

#### Consept

### Step 13

<p align="center"><img src="./assets/file-system-in-the-cloud/13.PNG"></p>

#### Consept

### Step 14

<p align="center"><img src="./assets/file-system-in-the-cloud/14.PNG"></p>

#### Consept

### Step 15

<p align="center"><img src="./assets/file-system-in-the-cloud/15.PNG"></p>

#### Consept

### Step 16

<p align="center"><img src="./assets/file-system-in-the-cloud/16.PNG"></p>

#### Consept

### Step 17

<p align="center"><img src="./assets/file-system-in-the-cloud/17.PNG"></p>

#### Consept

### Step 18

<p align="center"><img src="./assets/file-system-in-the-cloud/18.PNG"></p>

#### Consept

### Step 19

<p align="center"><img src="./assets/file-system-in-the-cloud/19.PNG"></p>

#### Consept

### Step 20

<p align="center"><img src="./assets/file-system-in-the-cloud/20.PNG"></p>

#### Consept

### Step 21

<p align="center"><img src="./assets/file-system-in-the-cloud/21.PNG"></p>

#### Consept

### Step 22

<p align="center"><img src="./assets/file-system-in-the-cloud/22.PNG"></p>

#### Consept

### Step 23

<p align="center"><img src="./assets/file-system-in-the-cloud/23.PNG"></p>

#### Consept

### Step 24

<p align="center"><img src="./assets/file-system-in-the-cloud/24.PNG"></p>

#### Consept

### Step 25

<p align="center"><img src="./assets/file-system-in-the-cloud/25.PNG"></p>

#### Consept

### Step 26

<p align="center"><img src="./assets/file-system-in-the-cloud/26.PNG"></p>

#### Consept

### Step 27

<p align="center"><img src="./assets/file-system-in-the-cloud/27.PNG"></p>

#### Consept

### Step 28

<p align="center"><img src="./assets/file-system-in-the-cloud/28.PNG"></p>

#### Consept

### Step 29

<p align="center"><img src="./assets/file-system-in-the-cloud/29.PNG"></p>

#### Consept

### Step 30

<p align="center"><img src="./assets/file-system-in-the-cloud/30.PNG"></p>

#### Consept

### Step 31

<p align="center"><img src="./assets/file-system-in-the-cloud/31.PNG"></p>

#### Consept

### Step 32

<p align="center"><img src="./assets/file-system-in-the-cloud/32.PNG"></p>

#### Consept

### Step 33

<p align="center"><img src="./assets/file-system-in-the-cloud/33.PNG"></p>

#### Consept

### Step 34

<p align="center"><img src="./assets/file-system-in-the-cloud/34.PNG"></p>

#### Consept

### Step 35

<p align="center"><img src="./assets/file-system-in-the-cloud/35.PNG"></p>

#### Consept

### Step 36

<p align="center"><img src="./assets/file-system-in-the-cloud/36.PNG"></p>

#### Consept

### Step 37

<p align="center"><img src="./assets/file-system-in-the-cloud/37.PNG"></p>

#### Consept

### Step 38

<p align="center"><img src="./assets/file-system-in-the-cloud/38.PNG"></p>

#### Consept

### Step 39

<p align="center"><img src="./assets/file-system-in-the-cloud/39.PNG"></p>

#### Consept

### Step 40

<p align="center"><img src="./assets/file-system-in-the-cloud/40.PNG"></p>

#### Consept

### Step 41

<p align="center"><img src="./assets/file-system-in-the-cloud/41.PNG"></p>

#### Consept

### Step 42
