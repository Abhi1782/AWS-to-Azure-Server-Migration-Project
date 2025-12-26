# 🚀 AWS to Azure Server Migration Project

## 📌 1. Project Overview
 This project demonstrates a real-world migration of an AWS server to Azure using Azure Migrate, covering assessment, discovery, application validation, and final migration.
 1) 🌍 Source Cloud: AWS (Mumbai Region)
 2) ☁️ Target Cloud: Microsoft Azure (India Region)

A sample NGINX application server was deployed, assessed, and migrated as part of this implementation.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

![Migration](https://github.com/user-attachments/assets/b2bfcc96-1f01-4631-a24d-cee6add44296)

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🏗️ 2. Architecture Summary

### ☁️ AWS – Source Environment

   1) 🧩 VPC with Public Subnet
   2) 🖥️ Assessment Server (Windows EC2)
   3) 🔄 Migration Server (EC2)
   4) 🌐 Application Server (Ubuntu EC2 + NGINX)
   5) 🔐 SSH & HTTPS enabled

### ☁️ Azure – Target Environment

   1) 📦 Azure Subscription
   2) 🌐 Azure Virtual Network (VNet)
   3) 🧭 Azure Migrate Project
   4) 🔁 Azure Migration Service
   5) 🖥️ Target Azure Virtual Machine

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🧭 3. High-Level Project Flow

    🟦 AWS Server Setup
            ↓
    🟩 Azure Migrate Project
            ↓
    🟨 Assessment Appliance Setup
            ↓
    🟧 Application Deployment (NGINX)
            ↓
    🟪 Discovery & Assessment
            ↓
    🔵 Replication
            ↓
    🟢 Test Migration
            ↓
    🔴 Final Cutover

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🟦 4. AWS Server Preparation

### 🖥️ 4.1 EC2 Servers Created

| Server                | Purpose                |
| --------------------- | ---------------------- |
| 🧪 Assessment Server  | Discovery & assessment |
| 🔄 Migration Server   | Replication traffic    |
| 🌐 Application Server | NGINX workload         |

📍 Region: AWS Mumbai

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<img width="1366" height="768" alt="Screenshot (32)" src="https://github.com/user-attachments/assets/264b12ce-135e-4eb9-ab03-d46ba005526e" />

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<img width="1366" height="768" alt="Screenshot (37)" src="https://github.com/user-attachments/assets/6ba65887-129d-47f5-96fe-8ecccb262e32" />

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🌐 5. Application Server Setup (NGINX)

### 🔐 5.1 SSH Access

   1) Connected to Ubuntu EC2 via SSH
   2) Verified OS & network connectivity

### ⚙️ 5.2 NGINX Installation

   1) Installed NGINX
   2) Enabled & started service
   3) Verified service status
   4) Deployed sample web content

#### ✅ Result:
Application accessible via browser and ready for migration

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<img width="1366" height="768" alt="Screenshot (33)" src="https://github.com/user-attachments/assets/d446cd37-90d9-4dfa-9064-50a84dc1ee83" />

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## ☁️ 6. Azure Migrate Project Setup

### 🧭 6.1 Azure Migrate Creation

   1) Created Azure Migrate Project
   2) Selected:
      A) Servers → Azure Virtual Machines
   3) Chosen Azure India Region

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<img width="1366" height="768" alt="Screenshot (36)" src="https://github.com/user-attachments/assets/f5549d6e-b7d5-49c5-83d6-93166d6bc7ba" />

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🔑 6.2 Registration Key Generation

   1) Generated Azure Migrate registration key
   2) Downloaded the Assessment appliance file
   3) Used to securely connect AWS to Azure

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<img width="1366" height="768" alt="Screenshot (41)" src="https://github.com/user-attachments/assets/3c0fbe87-a861-4f3b-a6fb-d24deb9759c4" />

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🟨 7. Assessment Server Configuration (AWS)

### 📥 7.1 Installer Download
   
   1) Downloaded AzureMigrateInstaller.ps1
   2) Extracted required components

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<img width="1366" height="768" alt="Screenshot (40)" src="https://github.com/user-attachments/assets/ae1edd7f-b946-4346-b954-bc4aa03aaefe" />

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<img width="1366" height="768" alt="Screenshot (1)" src="https://github.com/user-attachments/assets/33f0dc74-6726-439f-b3be-1590ac62b152" />

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🧰 7.2 Appliance Installation

   Executed via PowerShell (Admin):
     1) OS & PowerShell checks
     2) 64-bit validation
     3) Selected:
        A) Physical or other (AWS, GCP, Xen)

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<img width="1366" height="768" alt="Screenshot (4)" src="https://github.com/user-attachments/assets/4ca1e780-d730-442e-8c18-50ced6a52d1e" />

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

##  🔗 7.3 Appliance Registration

   1) Opened Appliance Configuration Manager
   2) Entered Azure Migrate key
   3) Registration successful

### ✅ Appliance connected to Azure Migrate

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

<img width="1366" height="768" alt="Screenshot (5)" src="https://github.com/user-attachments/assets/01f88f0c-14dd-4c5c-b7f2-85c4ca930fa1" />

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🔐 8. Credential Configuration
