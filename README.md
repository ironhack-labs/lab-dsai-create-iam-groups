![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Lab | IAM Users, Groups & Policies

## Introduction

In this hands-on lab, you will learn how to create **IAM Users**, **IAM Groups**, and **attach policies** to enforce access control within AWS.

## **Pre-Requisites**

- A valid **AWS account** (free-trial or pay-as-you-go subscription).
- Access to the **AWS Management Console**.

## Lab Instructions

### **Step 1: Log in to AWS Console**
1. Open a web browser and navigate to [AWS Console](https://aws.amazon.com/console/).
2. Enter your **AWS credentials** and log in.

### **Step 2: Create IAM Users 👤**
1. In the AWS Console, search for **IAM** and select the service.
2. In the **left pane**, click on **Users**.
3. Click **Create User**.
4. Enter the following details:
   - **User name**: `user1`
   - **Enable AWS Management Console access** (check the box).
   - Select **“I want to create an IAM User”** when prompted.
   - **Set a custom password** or generate a new one.
5. Click **Next**, keeping all default settings.
6. Click **Create User**.
7. **Download the .csv file** with login credentials.
8. Repeat **steps 3–7** to create **user2, user3, and user4**.

### **Step 3: Create IAM Groups**
1. In the **left pane**, select **User Groups**.
2. Click **Create group**.
3. Enter the **Group name** as `developer`.
4. Click **Create group**.
5. Repeat steps **1–4** to create another group named `finance`.

### **Step 4: Attach IAM Policies to Groups**
#### **Assign Policies to Developer Group**
1. Select the **developer** group.
2. Click **Permissions** → **Add Permissions** → **Attach Policies**.
3. Search for and select the following policies:
   - `AmazonRDSFullAccess`
   - `AmazonEC2FullAccess`
   - `AmazonEC2ContainerRegistryFullAccess`
   - `AmazonSageMakerFullAccess`
   -  `AmazonS3FullAccess`
4. Click **Attach policies**.

#### **Assign Policies to Finance Group**
1. Select the **finance** group.
2. Click **Permissions** → **Add Permissions** → **Attach Policies**.
3. Search for and select:
   - `Billing`.
4. Click **Attach policies**.

### **Step 5: Add Users to Groups 👥**
#### **Add Users to Developer Group**
1. Select the **developer** group.
2. Click **Add users**.
3. Select **user1, user2, and user3**.
4. Click **Add users**.

#### **Add Users to Finance Group**
1. Select the **finance** group.
2. Click **Add users**.
3. Select **user2 and user4**.
4. Click **Add users**.

### **Step 6: Verify User Permissions**
1. **Log out** of your AWS account.
2. Use the credentials from the `.csv` file to log in as each user.
3. Test the permissions by attempting to access AWS services:
   - Developer users should access **EC2 and RDS**.
   - Finance users should only access **Billing**.
4. If access is restricted, verify the group policies.

## Submission Guidelines
To complete this lab:

1. Take **screenshots** of IAM Users, Groups, and Policies applied.
2. Paste the screenshots into a **Google Doc**.
3. Upload the document to **Google Drive**.
4. Share the **Google Drive link** with your instructor.

This lab provides **hands-on experience** in **managing IAM users, groups, and permissions** in AWS, ensuring proper access control and security within an AWS environment.