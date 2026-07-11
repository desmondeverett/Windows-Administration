# Lab 1: Windows Server 2022 Deployment & Post-Installation

## 🎯 Objective
By the end of this lab, you will be able to provision a virtual machine in VirtualBox, install Windows Server 2022 (Desktop Experience), and configure baseline system metrics.

## 🛠️ Prerequisites & Tools
* Oracle VirtualBox (Latest Version)
* Windows Server 2022 ISO (Evaluation Edition)

---

## 📝 Step-by-Step Instructions

### Step 1: Create the Virtual Machine Container
1. Open VirtualBox and click **New**.
2. Name the VM `ET-DC01` and set the Type to **Microsoft Windows**, Version to **Windows Server 2022 (64-bit)**.
3. Allocate at least **4096 MB (4GB) of RAM** and **2 Processors**.

*Your configuration screen should match the summary below:*
![VirtualBox Environment Summary](../Screenshots/01-vm-summary.png)

### Step 2: Operating System Installation
1. Start the VM and select your Windows Server 2022 ISO.
2. When prompted, choose **Windows Server 2022 Standard Evaluation (Desktop Experience)**. *Do not choose the Server Core option unless you intend to use CLI only.*
3. Follow the prompts to format the unallocated drive space and begin installation.

![Installation Success](../Screenshots/03-installation-success.png)

---

## 🎓 Student Checkpoint & Deliverables
To verify your lab is complete, take a screenshot of your **Server Manager Dashboard** showing your computer name (`ET-DC01`) and upload it to the assignment portal.
