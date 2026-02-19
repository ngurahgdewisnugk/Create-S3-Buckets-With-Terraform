<div align="center">
  <img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />
  
  # 🚀 Create S3 Buckets with Terraform
  
  **Automating AWS Infrastructure Deployment with Infrastructure as Code**
  
  [![Project Link](https://img.shields.io/badge/View-Project-blue?style=for-the-badge)](http://learn.nextwork.org/projects/aws-devops-terraform1)

[![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)](https://www.terraform.io/)
[![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)
[![S3](https://img.shields.io/badge/Amazon_S3-569A31?style=for-the-badge&logo=amazon-s3&logoColor=white)](https://aws.amazon.com/s3/)
[![IAM](https://img.shields.io/badge/IAM-DD344C?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/iam/) 
  ---
  
  **Author:** Ngurah Gede Wisnu Gudakesa  
  **Email:** ngurahgedewisnugk@gmail.com
  
</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Tools & Technologies](#️-tools--technologies)
- [Key Concepts](#-key-concepts)
- [System Archchitecture](#️-system-architecture)
- [Project Reflection](#-project-reflection)
- [Introduction to Terraform](#-introduction-to-terraform)
- [Configuration Files](#-configuration-files)
- [Customizing S3 Buckets](#-customizing-s3-buckets)
- [Terraform Commands](#-Terraform-Commands)
- [AWS CLI Setup](#-aws-cli-setup)
- [Launching the S3 Bucket](#-launching-the-s3-bucket)
- [Uploading S3 Objects](#-uploading-s3-objects)

---

## 🎯 Overview

<div align="center">
  <img src="http://learn.nextwork.org/motivated_teal_shy_hog/uploads/aws-devops-terraform1_9i0j1k2l" alt="Project Overview" width="1000" />
</div>

In this project, I learned to **automate the deployment of Amazon S3 buckets** using Terraform. The main goal is to understand how automation streamlines the development and deployment of cloud resources, making the process more efficient and reducing the potential for manual errors.

---

## 🛠️ Tools & Technologies

<div align="left">

| Category | Technology | Purpose |
|----------|-----------|---------|
| **Orchestration** | ![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white) | Infrastructure as Code engine |
| **Cloud Provider** | ![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white) | Cloud infrastructure platform |
| **Storage** | ![S3](https://img.shields.io/badge/S3-569A31?style=flat-square&logo=amazon-s3&logoColor=white) | Object storage service |
| **Security** | ![IAM](https://img.shields.io/badge/IAM-DD344C?style=flat-square&logo=amazon-aws&logoColor=white) | Identity and access management |
| **CLI** | ![AWS CLI](https://img.shields.io/badge/AWS_CLI-232F3E?style=flat-square&logo=amazon-aws&logoColor=white) | Command-line interface |

</div>

---

## 💡 Key Concepts

### What I Learned

- ✅ Using **Infrastructure as Code (IaC)** with Terraform to create and deploy Amazon S3 buckets and objects.
- ✅ Authenticating Terraform's communication with AWS by configuring AWS CLI with credentials granted by AWS IAM.
- ✅ Managing cloud resources through declarative configuration files.
- ✅ Understanding Terraform workflow: `init`, `plan`, and `apply`.

---

## 🏛️ System Architecture

![system-architecture](https://github.com/user-attachments/assets/06c0a693-ca5d-4612-8a66-d13a3c64c184)


### 🔄 Workflow Breakdown

1. **🔵 SETUP**: Download and install Terraform CLI, Create Project Directory, and write configuration file with AWS provider and S3 Resources. 
2. **📋 PLANNING**: Initialize project, check credential, Preview infrastructure changes and validate configuration.
3. **🔴 TROUBLESHOOTING**: Install AWS CLI, Configure credentials, Verify authentication.
4. **⚙️ DEPLOYMENT**: Run terraform apply, Confirm changes, Monitor progress.
5. **🟢 OUTPUT**: Verify deployment, Validate settings, Success.
---

# 🔍 Project Reflection

## Challenges Faced

### 🎓 Key Takeaways

> **Challenge:** S3 bucket names only allow lowercase characters  
> **Solution:** Always validate naming conventions before running `terraform apply`

> **Challenge:** "No valid credential sources found" error  
> **Solution:** Configure AWS CLI with `aws configure` before running Terraform commands

> **Best Practice:** Always run `terraform plan` before `apply` to catch errors early

### ⏱️ Project Metrics

- **Time Investment:** ~3 hours.
- **Most Challenging:** Bucket naming conventions and IAM credential setup.
- **Most Rewarding:** Successfully deploying infrastructure from code.
- **Skills Gained:** IaC fundamentals, AWS authentication, Terraform workflow.

### 💡 Why This Project?

I chose this project because it directly aligns with my goal of transitioning into **Cloud Native Orchestration**, particularly with AWS. I'm enthusiastic about this area because these skills are highly in-demand, and this project helps build foundational knowledge for Infrastructure as Code (IaC) with Terraform.

---

## 📚 Introduction to Terraform

<div align="center">
  <img src="http://learn.nextwork.org/motivated_teal_shy_hog/uploads/aws-devops-terraform1_9i0j1k2l" alt="Terraform Introduction" width="1000" />
</div>

### What is Terraform?

**Terraform** is an Infrastructure as Code (IaC) tool that helps you build and manage your cloud infrastructure using code. Instead of manual setup, you write scripts that act as blueprints, telling Terraform exactly what cloud resources (like servers, databases, and networks) you want. It then automatically builds them for you.

### Key Benefits

- 🌐 **Multi-cloud support** - Works across AWS, Azure, Google Cloud, and more
- 📝 **Version control** - Track infrastructure changes like application code
- 🔄 **Consistency** - Recreate the same environment reliably
- 👥 **Collaboration** - Share infrastructure definitions with your team

### Infrastructure as Code (IaC)

Infrastructure as Code (IaC) is the practice of defining your cloud setup (like servers, storage, and networks) using code in plain text files. Instead of manually clicking through a web console, you write these files, and the cloud builds everything exactly as you've described.

### The main.tf File

`main.tf` is a central file in a Terraform project where you write down what you want your infrastructure to look like. Think of it as the **blueprint for building your cloud resources**.

Terraform uses these configuration files to define and manage your infrastructure by describing its desired state, and then Terraform figures out how to achieve that state.

---

## 📝 Configuration Files

<div align="center">
  <img src="http://learn.nextwork.org/motivated_teal_shy_hog/uploads/aws-devops-terraform1_ljvh9876" alt="Configuration Files" width="1000" />
</div>

The configuration is structured in **blocks**. The advantage of doing this is the file stays easy to read and you can tweak one part without touching the rest of your setup.

### My main.tf Configuration

My `main.tf` configuration has **three main blocks**:

#### 1️⃣ Provider Block

```hcl
provider "aws" {
  # AWS provider configuration
}
```

- Indicates that Terraform should use AWS
- Acts as a plugin, allowing Terraform to interact with AWS services
- Converts configuration into API calls to create and manage infrastructure

#### 2️⃣ S3 Bucket Resource

```hcl
resource "aws_s3_bucket" "my_bucket" {
  # S3 bucket configuration
}
```

- Creates an S3 bucket
- `my_bucket` is an internal reference for other parts of the configuration

#### 3️⃣ Public Access Block

```hcl
resource "aws_s3_bucket_public_access_block" "my_bucket_public_access_block" {
  block_public_acls       = true
  ignore_public_acls      = true
  block_public_policy     = true
  restrict_public_buckets = true
}
```

- Controls public access to the S3 bucket
- All settings set to `true` to prevent any public access
- Ensures bucket and contents remain private

---

## 🎨 Customizing S3 Buckets

<div align="center">
  <img src="http://learn.nextwork.org/motivated_teal_shy_hog/uploads/aws-devops-terraform1_ffe757cd3" alt="Customizing S3 Buckets" width="1000" />
</div>

### Project Extension

For my project extension, I visited the [official Terraform documentation](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/s3_bucket) to look for ways to customize my bucket's configurations.

### Adding Tags

I chose to customize my S3 bucket by adding **'Owner' and 'Project' tags** to the `aws_s3_bucket` resource:

```hcl
resource "aws_s3_bucket" "my_bucket" {
  bucket = "my-unique-bucket-name"
  
  tags = {
	Owner   = "DummyWsWorskpace"
	Project = "accelerate S3 Buckets from scratch with Terraform then deploy to AWS Cloud Provider"
  }
}
```

### Benefits of Tagging

- 🏷️ Easily identify who created the bucket
- 📊 Track which project the bucket belongs to
- 💰 Better cost allocation and management
- 🔍 Improved resource organization

---

## ⚙️ Terraform Commands

<div align="center">
  <img src="http://learn.nextwork.org/motivated_teal_shy_hog/uploads/aws-devops-terraform1_3g4h5i6j" alt="Terraform Commands" width="1000" />
</div>

### 1. `terraform init`

The **first command** to run for a new Terraform project. It sets up your working directory by:

- 📦 **Downloading necessary plugins** - Fetches providers (like AWS) that allow Terraform to interact with cloud services
- 💾 **Setting up the backend** - Prepares where Terraform state files will be stored
- 🧩 **Preparing modules** - Downloads reusable code blocks if used
- 🔒 **Creating a lock file** - Generates `.terraform.lock.hcl` to record exact provider versions

```bash
terraform init
```

### 2. `terraform plan`

Creates an **execution plan** showing exactly what changes Terraform will make:

- ✅ Preview resources to be created
- 🔄 Preview resources to be updated
- ❌ Preview resources to be destroyed

```bash
terraform plan
```

> 💡 **Best Practice:** Always run `terraform plan` before applying changes to catch potential errors!

### 3. `terraform apply`

Executes the plan and **applies changes** to your infrastructure:

```bash
terraform apply
```

### Command Sequence

The sequence is crucial because each command builds upon the previous one:

```
terraform init → terraform plan → terraform apply
```

1. **init** - Sets up the project
2. **plan** - Shows what will change
3. **apply** - Makes the changes

---

## 🔐 AWS CLI Setup

<div align="center">
  <img src="http://learn.nextwork.org/motivated_teal_shy_hog/uploads/aws-devops-terraform1_7j8k9l0m" alt="AWS CLI Setup" width="1000" />
</div>

### The Credential Error

When I ran `terraform plan`, I received the error:

```
❌ No valid credential sources found
```

This happened because Terraform didn't have the necessary credentials to authenticate with my AWS account.

### What is AWS CLI?

The **AWS CLI** is a powerful tool that lets you manage AWS services from your terminal, instead of using the AWS Management Console. In this project, I'm using the CLI so that Terraform can create AWS resources from my local computer.

### Setting Up Access Keys

I set up AWS access keys to allow the AWS CLI to authenticate and interact with AWS services:

```bash
aws configure
```

You'll be prompted to enter:

- 🔑 **Access Key ID**
- 🔐 **Secret Access Key**
- 🌍 **Default region** (e.g., `us-east-1`)
- 📄 **Default output format** (e.g., `json`)

> ⚠️ **Security Note:** Keep your access keys secure and never commit them to version control!

---

## 🚀 Launching the S3 Bucket

<div align="center">
  <img src="http://learn.nextwork.org/motivated_teal_shy_hog/uploads/aws-devops-terraform1_1q2w3e4r" alt="Launching S3 Bucket" width="1000" />
</div>

### Running terraform apply

<div align="left">
  <img src="assets/terraform applu.png" alt="Terraform a" width="1000" />
</div>

I ran `terraform apply` to apply the changes written in my Terraform configuration:

```bash
terraform apply
```

### What Happens?

Running `terraform apply` will:

- ✅ Create the S3 bucket on AWS
- 📝 Update the Terraform state file
- 🔒 Apply the public access block settings
- 🏷️ Add the custom tags

### Verification

After successful deployment, I verified the bucket creation by:

1. Opening the **AWS Management Console**
2. Navigating to **S3 service**
3. Confirming the bucket exists with correct settings
4. Checking the tags are properly applied

---

## 📤 Uploading S3 Objects

<div align="center">
  <img src="http://learn.nextwork.org/motivated_teal_shy_hog/uploads/aws-devops-terraform1_9o0p1a2s" alt="Uploading S3 Objects" width="1000" />
</div>

### Adding an S3 Object

I added a new resource block to upload an image to my S3 bucket:

```hcl
resource "aws_s3_object" "my_image" {
  bucket = aws_s3_bucket.my_bucket.id
  key    = "my-image.jpg"
  source = "path/to/local/image.jpg"
}
```

### Applying the Changes

<div align="left">
  <img src="assets/terraform apply object.png" alt="Terraform a" width="1000" />
</div>

Since I updated my Terraform configuration, I needed to run `terraform apply` again:

```bash
terraform apply
```

This tells Terraform to:

- 🔍 Review the new changes
- 📊 Compare them with existing infrastructure
- 📤 Upload the S3 object to the bucket

### Validation

<div align="left">
  <img src="assets/verify object.png" alt="Terraform a" width="1000" />
</div>

To validate the successful upload, I:

1. Opened the **AWS Management Console**
2. Navigated to my **S3 bucket**
3. Confirmed the file was present in the **Objects** tab
4. Downloaded the file to verify its content

---

## 🎓 Conclusion

This project provided hands-on experience with:

- ✅ Infrastructure as Code principles
- ✅ Terraform workflow and commands
- ✅ AWS S3 bucket creation and management
- ✅ AWS CLI configuration and authentication
- ✅ Resource tagging and customization

### Next Steps

- 🔄 Explore Terraform modules for reusable configurations
- 🌐 Deploy multi-region infrastructure
- 🔒 Implement remote state management
- 📊 Add more AWS resources to the configuration

---
