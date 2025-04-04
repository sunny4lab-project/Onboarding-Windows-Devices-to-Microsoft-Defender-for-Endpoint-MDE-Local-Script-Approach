# 🔥 Onboarding Windows Devices to MDE  

Overview

This project provides a step-by-step guide to onboarding Windows devices to Microsoft Defender for Endpoint (MDE) using the Local Script method. This approach is ideal for environments where Intune or Group Policy is not available for deployment.

  
#
<div align="center">
  
![ChatGPT Image Apr 3, 2025, 04_25_36 PM](https://github.com/user-attachments/assets/b3376878-e6d5-43c7-b3dd-55d9b23e5156) </div>


# Prerequisites

Before starting, ensure you have:

- A valid Microsoft Defender for Endpoint (MDE) license

- Administrator access to the Windows devices

- PowerShell with administrator privileges

- Internet connectivity on the target device

<details><summary>Click here for details</summary>

**Step 1: Download the Onboarding Script**

Log in to Microsoft Defender Security Center: security.microsoft.com

Navigate to Settings > Device Management > Onboarding
![Screenshot 2025-04-04 132959](https://github.com/user-attachments/assets/052c2c9b-46e1-4ea0-af56-d9389f71c7f7)


![Screenshot 2025-04-04 133508](https://github.com/user-attachments/assets/a0abdc8c-5e98-4588-8bd9-1831866c4cdb)


![Screenshot 2025-04-04 133050](https://github.com/user-attachments/assets/9582a5a6-0b17-4156-b30d-1fb391983b45)

#
Select Windows 10 or Windows Server
![Screenshot 2025-04-04 134339](https://github.com/user-attachments/assets/248ceb05-46e4-4044-887b-6548bd15635d)


#
Choose Local Script as the onboarding method
![Screenshot 2025-04-04 134421](https://github.com/user-attachments/assets/992139cd-de5a-45be-b206-9130a1d685e7)

#
Click Download package to get the onboarding script
![Screenshot 2025-04-04 142333](https://github.com/user-attachments/assets/93c2ae83-d10b-4f36-b5c5-f6fdba63703d)

#
**Step 2: Running the Onboarding Script**

Copy the downloaded WindowsDefenderATPOnboardingScript.cmd file to the target device.
![Screenshot 2025-04-04 134500](https://github.com/user-attachments/assets/d597f7e7-3f43-4668-b03d-9b913c04dfcf)

#
Open PowerShell as Administrator.
![Screenshot 2025-04-04 142523](https://github.com/user-attachments/assets/32980cc2-7be2-41ad-847c-91675b1b3ae3)

Navigate to the script's location:

cd C:\Path\To\Script

Run the onboarding script:

powershell -ExecutionPolicy Bypass -File WindowsDefenderATPOnboardingScript.cmd

Wait for the process to complete.

Step 3: Verifying Onboarding Status

Option 1: Check via PowerShell

Run the following command:

Get-MpComputerStatus | Select MDEOnboardingState

1 → Successfully onboarded ✅

0 → Not onboarded ❌

Option 2: Check in Microsoft Defender Security Center

Go to Microsoft Defender Security Center (security.microsoft.com)

Navigate to Devices > Device Inventory

Search for the device by name
