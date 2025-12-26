# 🚀 AWS to Azure Server Migration Project

# 📌 1. Project Overview
 This project demonstrates a real-world migration of an AWS server to Azure using Azure Migrate, covering assessment, discovery, application validation, and final migration.
 1) 🌍 Source Cloud: AWS (Mumbai Region)
 2) ☁️ Target Cloud: Microsoft Azure (India Region)

A sample NGINX application server was deployed, assessed, and migrated as part of this implementation.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
![Migration](https://github.com/user-attachments/assets/b2bfcc96-1f01-4631-a24d-cee6add44296)
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# 🏗️ 2. Architecture Summary

## ☁️ AWS – Source Environment

   1) 🧩 VPC with Public Subnet
   2) 🖥️ Assessment Server (Windows EC2)
   3) 🔄 Migration Server (EC2)
   4) 🌐 Application Server (Ubuntu EC2 + NGINX)
   5) 🔐 SSH & HTTPS enabled

## ☁️ Azure – Target Environment

   1) 📦 Azure Subscription
   2) 🌐 Azure Virtual Network (VNet)
   3) 🧭 Azure Migrate Project
   4) 🔁 Azure Migration Service
   5) 🖥️ Target Azure Virtual Machine

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# 🧭 3. High-Level Project Flow

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

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# 🟦 4. AWS Server Preparation

## 🖥️ 4.1 EC2 Servers Created

| Server                | Purpose                |
| --------------------- | ---------------------- |
| 🧪 Assessment Server  | Discovery & assessment |
| 🔄 Migration Server   | Replication traffic    |
| 🌐 Application Server | NGINX workload         |

📍 Region: AWS Mumbai
