# Lab 04 - Windows Firewall Configuration & Network Security

## Objective
Configure and audit the advanced security capabilities of the Windows Defender Firewall on a Windows Server 2022 instance, establishing custom inbound/outbound rules to enforce host-level network segregation and traffic control.

## Environment
- **Operating System:** Windows Server 2022 Standard Evaluation (Desktop Experience)
- **Virtualization Hypervisor:** Oracle VirtualBox
- **System Hostname:** ET-DC01

## Requirements & Scope
1. Verify the baseline operational status of the Windows Defender Firewall profiles.
2. Create an explicit inbound block rule for Internet Control Message Protocol (ICMP/Ping) to hide the server from basic network discovery.
3. Test and verify rule enforcement from the host or a simulated endpoint network state.
4. Document the security policy baseline change.

## Implementation Steps

### Phase 1: Analyzing the Firewall Baseline
1. Log into `ET-DC01` as the built-in Administrator.
2. Open the Run dialog (`Win + R`), type **`wf.msc`**, and press **Enter** to open the **Windows Defender Firewall with Advanced Security** console.
3. Click on the root folder in the left pane and verify that the Domain, Private, and Public profiles are all actively set to **On**.
   > 📸 **SCREENSHOT #1:** Capture the main Firewall Advanced Security dashboard showing all profiles active. (Save as `01-firewall-baseline.png`)

### Phase 2: Restricting Network Discovery (Blocking ICMP)
1. In the left-hand column, right-click **Inbound Rules** and select **New Rule...**.
2. On the Rule Type step, choose **Custom** and click **Next**.
3. On the Program step, leave it as *All programs* and click **Next**.
4. On the Protocol and Ports step, change the Protocol type dropdown to **ICMPv4**. Click **Next**.
5. On the Scope step, leave IP addresses as *Any IP address* and click **Next**.
6. On the Action step, explicitly select **Block the connection**. Click **Next**.
7. On the Profile step, keep all boxes checked (Domain, Private, Public) and click **Next**.
8. On the Name step, name the rule **`BLOCK-ICMP-PING`** and add the description: `Explicitly blocks all inbound echo requests to prevent network scanning.`
9. Click **Finish**.

### Phase 3: Rule Verification & Testing
1. Select **Inbound Rules** in the left pane and locate your new `BLOCK-ICMP-PING` rule at the top of the middle list.
2. Ensure the rule displays a distinct red stop-sign icon, confirming an active drop policy.
   > 📸 **SCREENSHOT #2:** Capture the Inbound Rules pane highlighting the new active `BLOCK-ICMP-PING` rule properties. (Save as `02-firewall-rule-verification.png`)

---

## Outcome
(To be completed after execution.)

## Lessons Learned
(To be completed after execution.)

## Screenshots
#### 1. Windows Defender Firewall Active Profiles
![Firewall Baseline](../Screenshots/01-firewall-baseline.png)

#### 2. Configured Inbound ICMP Block Rule Policy
![Firewall Rule Verification](../Screenshots/02-firewall-rule-verification.png)
