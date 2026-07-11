# 💻 Windows Server 2022 & Active Directory Administration Sandbox

Welcome to my enterprise Windows Administration laboratory. This repository serves as an open-source, hands-on instructional guide and implementation portfolio for deploying, managing, and securing a Windows Server 2022 infrastructure. 

Whether you are a recruiter auditing my technical skills or a student looking to replicate these environments step-by-step, this documentation provides full visibility into enterprise administration baselines.

---

## 🏗️ Core Laboratory Architecture
* **Host Hypervisor:** Oracle VirtualBox
* **Operating System:** Windows Server 2022 Standard Evaluation (Desktop Experience)
* **Target Domain Deployment:** `ET-DC01` (Enterprise Topology Domain Controller)

---

## 🧭 Laboratory Index & Execution Milestones

### 🟢 [Lab 1: Windows Server 2022 Deployment & Post-Installation](./Labs/Lab-01-Installing-Windows-Server.md)
* **The Blueprint:** Provisioning virtual hardware containers and executing clean OS baselines.
* **Key Skills Demonstrated:** Hypervisor hardware allocation (RAM/vCPU optimization), evaluation ISO deployment, and initial system metrics auditing.

### 🟢 [Lab 2: Local User Management & Security Groups](./Labs/Lab-02-Local-User-Management.md)
* **The Blueprint:** Identity and Access Management (IAM) applying the principle of least privilege.
* **Key Skills Demonstrated:** Provisioning local administrator and standard accounts via `lusrmgr.msc`, security group nesting, and PowerShell user auditing (`Get-LocalGroupMember`).

### 🟢 [Lab 3: Event Viewer & Proactive System Auditing](./Labs/Lab-03-Event-Viewer.md)
* **The Blueprint:** Analyzing system logging logs to diagnose anomalies and audit infrastructure security.
* **Key Skills Demonstrated:** Event log filtering (`eventvwr.msc`), isolating system/application errors, and setting local security policies to track failed logon attempts.

### 🟢 [Lab 4: Windows Firewall with Advanced Security](./Labs/Lab-04-Windows-Firewall.md)
* **The Blueprint:** Implementing host-based perimeter defense and granular network traffic control.
* **Key Skills Demonstrated:** Evaluating default inbound/outbound connection rules, establishing custom protocol filters, and verifying active packet blocks.

### 🔵
