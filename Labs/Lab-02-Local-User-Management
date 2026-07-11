# Lab 02 - Local User and Group Management

## Objective
Configure and manage local user accounts, administrative groups, and security permissions on a standalone Windows Server 2022 instance to demonstrate foundational identity and access management (IAM) principles.

## Environment
- **Operating System:** Windows Server 2022 Standard Evaluation (Desktop Experience)
- **Virtualization Hypervisor:** Oracle VirtualBox
- **System Hostname:** ET-DC01

## Requirements & Scope
1. Create a standard local user account simulating a new employee.
2. Create a custom local IT security group.
3. Assign the new user to the security group.
4. Provision a secured local folder structure and configure explicit NTFS permissions, ensuring only authorized group members have access.

## Implementation Steps

### Phase 1: Local User & Group Creation
1. Log into `ET-DC01` as the built-in Administrator.
2. Open the **Computer Management** console (`compmgmt.msc`) and navigate to **System Tools > Local Users and Groups**.
3. Right-click **Users** and select **New User**. Create a user account (e.g., `jdoe` for John Doe) with a secure password.
4. Right-click **Groups** and select **New Group**. Name the group `IT-Admins`.
5. Add the newly created user account as a member of the `IT-Admins` group.
   > 📸 **SCREENSHOT #1:** Capture the properties window of the `IT-Admins` group showing your new user listed as a member. (Save as `01-group-membership.png`)

### Phase 2: Folder Provisioning & NTFS Permissions
1. Open File Explorer and create a folder on the root of the C:\ drive named `CompanyData`.
2. Right-click the folder, select **Properties**, and navigate to the **Security** tab.
3. Click **Advanced** to modify the Access Control Lists (ACLs).
4. Disable inheritance and remove all pre-existing permissions to ensure a clean slate.
5. Add explicit **Full Control** permissions for the `IT-Admins` group, and **Read/Execute** permissions for `Authenticated Users`.
   > 📸 **SCREENSHOT #2:** Capture the Advanced Security Settings window showing the clean, explicit permission entries for your custom group. (Save as `02-ntfs-permissions.png`)

### Phase 3: Verification & Testing
1. Sign out of the Administrator account.
2. Log into the server using the new standard user account credentials.
3. Attempt to access the `CompanyData` folder to verify read/write access.
   > 📸 **SCREENSHOT #3:** Capture the desktop view showing the successful login session under the new user account profile alongside an open, accessible `CompanyData` folder view. (Save as `03-user-verification.png`)

---

## Outcome
(To be completed after execution.)

## Lessons Learned
(To be completed after execution.)

## Screenshots
#### 1. Custom Local Group & User Membership
![IT-Admins Group Properties](../Screenshots/01-group-membership.png)

#### 2. Explicit NTFS Folder Security Configurations
![Advanced NTFS Security](../Screenshots/02-ntfs-permissions.png)

#### 3. Access Control Verification
![User Session Verification](../Screenshots/03-user-verification.png)
