## Installation Steps

### Phase 1: Virtual Machine Creation
1. Open VirtualBox and click **New**.
2. Name the VM `ET-DC01`, select your Windows Server 2022 ISO, and check **Skip Unattended Installation**.
3. Allocate **4 GB RAM** and **2 vCPUs**.
4. Create a **80 GB Dynamic Virtual Hard Disk**.
5. On the final Summary screen, pause. 
   > 📸 **SCREENSHOT #1:** Capture the VirtualBox Summary window showing your hardware configurations before clicking **Finish**. (Save as `01-vm-summary.png`)

### Phase 2: Operating System Setup
1. Start the VM and press any key to boot from the ISO.
2. Select your language preferences and click **Install Now**.
3. When prompted to select the operating system, highlight **Windows Server 2022 Standard Evaluation (Desktop Experience)**.
   > 📸 **SCREENSHOT #2:** Capture the OS selection screen with the Desktop Experience option highlighted. (Save as `02-os-selection.png`)
4. Choose **Custom Installation**, select the 80 GB unallocated drive, and click **Next**.

### Phase 3: Post-Installation & Verification
1. Set a secure password for the built-in `Administrator` account.
2. Log into the server using `Input > Keyboard > Insert Ctrl-Alt-Del`.
3. Open **Server Manager**, click on **Local Server**, and verify the computer name.
   > 📸 **SCREENSHOT #3:** Capture the full desktop view showing the Server Manager dashboard and the System Properties displaying the hostname `ET-DC01`. (Save as `03-installation-success.png`)
