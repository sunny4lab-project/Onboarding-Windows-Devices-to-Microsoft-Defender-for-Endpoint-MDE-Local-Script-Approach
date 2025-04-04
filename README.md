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


Select Windows 10 or Windows Server

Choose Local Script as the onboarding method

Click Download package to get the onboarding script

Step 2: Running the Onboarding Script

Copy the downloaded WindowsDefenderATPOnboardingScript.cmd file to the target device.

Open PowerShell as Administrator.
