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


### Phase 2: Folder Provisioning & NTFS Permissions
1. Open File Explorer and create a folder on the root of the C:\ drive named `CompanyData`.
2. Right-click the folder, select **Properties**, and navigate to the **Security** tab.
3. Click **Advanced** to modify the Access Control Lists (ACLs).
4. Disable inheritance and remove all pre-existing permissions to ensure a clean slate.
5. Add explicit **Full Control** permissions for the `IT-Admins` group, and **Read/Execute** permissions for `Authenticated Users`.


### Phase 3: Verification & Testing
1. Sign out of the Administrator account.
2. Log into the server using the new standard user account credentials.
3. Attempt to access the `CompanyData` folder to verify read/write access.


---

## Outcome
Successfully provisioned a secure local access framework on ET-DC01. By segregating administrative access into a dedicated security group (IT-Admins) and stripping inherited permissions from the 'CompanyData' folder, access control was strictly verified. Logging in as the standard user 'jdoe' confirmed that group-based permissions effectively map read/write rights without over-privileging accounts.

## Lessons Learned
- **Order of Operations Matters:** Learned that Windows security mechanisms require the target object (user or group) to exist entirely in the system's identity management database before permissions can be evaluated or assigned at the file system level.
- **Inheritance Traps:** Discovered that disabling permission inheritance is a critical step when building secure repositories; otherwise, default wide-open administrative and system permissions persist implicitly.
- **Explicit Access Control:** Practiced the principle of least privilege by ensuring standard users retain only read access, while IT administrators hold full folder authority.

## Screenshots
#### 1. Custom Local Group & User Membership
![IT-Admins Group Properties](../Screenshots/01-group-membership.png)

#### 2. Explicit NTFS Folder Security Configurations
![Advanced NTFS Security](../Screenshots/02-ntfs-permissions.png)

#### 3. Access Control Verification
![User Session Verification](../Screenshots/03-user-verification.png)
