# ☁️ How to Create a Virtual Machine in Microsoft Azure

## 🧭 Prerequisites

* An active **Microsoft Azure account**
* Access to the **Azure portal**: [https://portal.azure.com](https://portal.azure.com)

---

## 🛠️ Step-by-Step Instructions

### ✅ Step 1: Sign in to the Azure Portal

Go to [https://portal.azure.com](https://portal.azure.com) and log in using your Microsoft credentials.

---

### 🆕 Step 2: Create a New Virtual Machine

1. In the **Azure portal**, search for **"Virtual machines"** in the search bar and select it.
2. Click on **+ Create > Azure virtual machine**.

---

### 🧾 Step 3: Configure Basic Settings

Fill out the following fields:

| Field                    | Description                                          |
| ------------------------ | ---------------------------------------------------- |
| **Subscription**         | Choose your subscription                             |
| **Resource Group**       | Create new or use an existing group                  |
| **Virtual machine name** | e.g., `MyTestVM`                                     |
| **Region**               | Choose a region close to you                         |
| **Availability options** | Default is fine for basic setup                      |
| **Image**                | Choose an OS, e.g., **Windows 11**, **Ubuntu 22.04** |
| **Size**                 | Click "See all sizes" and choose one (e.g., B1s)     |

---

### 🔐 Step 4: Set Admin Username and Password

* **Username**: Choose a secure name (e.g., `adminuser`)
* **Password / SSH Key**:

  * For **Windows**, set a **username/password**
  * For **Linux**, use **SSH public key** or **password**

---

### 🌐 Step 5: Configure Inbound Port Rules

* Select **Allow selected ports**
* Choose:

  * **RDP (3389)** for Windows
  * **SSH (22)** for Linux

---

### 📦 Step 6: Configure Disks (Optional)

* Choose **OS disk type** (e.g., Standard SSD for cost savings)
* Optionally add data disks

---

### 🌍 Step 7: Networking

* Use default virtual network and subnet
* Public IP: Enabled
* NIC network security group: Use basic and select ports

---

### 📋 Step 8: Review + Create

1. Click **"Review + create"**
2. Azure will validate your configuration
3. If validation passes, click **"Create"**

---

### ⏳ Step 9: Deployment and Access

* Wait for deployment to complete (about 2-3 minutes)
* Once done, click **"Go to resource"**

---

### 🖥️ Step 10: Connect to Your VM

#### For Windows:

1. Click **Connect > RDP**
2. Download RDP file and log in using credentials

#### For Linux:

1. Click **Connect > SSH**
2. Follow SSH command instructions (e.g., `ssh azureuser@<public_ip>`)

---

## 📌 Notes

* Always **shut down** or **delete** your VM when done to avoid charges.
* Configure **NSG rules**, **automatic updates**, and **backups** for production use.
* Enable **monitoring** and **diagnostics** for better visibility.
