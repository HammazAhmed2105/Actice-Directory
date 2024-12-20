# Part 2: Setting Up Virtual Machines for Active Directory Project

## Objective
In this part of the series, we will install and configure the following virtual machines using VirtualBox:
- Windows 10
- Kali Linux
- Ubuntu Server
- Windows Server 2022

---

## Overview of Active Directory
Active Directory (AD) is a database that contains objects like users, computers, and groups. To enable Active Directory, a server must:
1. Install Active Directory Domain Services (AD DS).
2. Be promoted to a Domain Controller (DC).

The DC will allow:
- **Authentication** via Kerberos.
- **Authorization** for the domain.

---

## Steps to Install Virtual Machines

### Step 1: Install VirtualBox
1. Visit [VirtualBox's official website](https://www.virtualbox.org/).
2. Download the installer for your operating system.
3. Verify the file integrity using SHA-256:
   - Open PowerShell.
   - Run `Get-FileHash` on the downloaded file.
   - Compare the hash with the checksum on the website.
4. Install VirtualBox:
   - Follow the setup wizard and install required dependencies (e.g., Microsoft Visual C++ 2019).

### Step 2: Create a Windows 10 Virtual Machine
1. Download the [Windows Media Creation Tool](https://www.microsoft.com/software-download/windows10).
2. Use the tool to create a Windows 10 ISO file.
3. Open VirtualBox and create a new VM:
   - Name: Choose a name (e.g., `Windows10`).
   - Memory: Set to **4 GB**.
   - Hard Disk: Allocate **50 GB**.
4. At the end you should have the below configuration.
![Windows10 VM](https://i.imgur.com/pcw3EVI.png)
5. Start the VM, and install Windows 10 using the ISO file:
   - Skip the product key during installation.
   - Select **Custom Install** and proceed.
   - ![Custom Install](https://i.imgur.com/mBiBh7E.png)


### Step 3: Create a Kali Linux Virtual Machine
1. Visit [Kali Linux's official website](https://www.kali.org/).
2. Download the pre-built VirtualBox image for **64-bit**.
3. Install [7-Zip](https://www.7-zip.org/) if needed to extract the archive.
4. Extract the downloaded file and double-click the `.vbox` file to import it into VirtualBox.
5. Start Kali Linux using the default credentials:
   - Username: `kali`
   - Password: `kali`.

### Step 4: Create a Windows Server 2022 Virtual Machine
1. Download the [Windows Server 2022 ISO](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2022).
2. Fill in the required information on the website to access the ISO file.
3. Open VirtualBox and create a new VM:
   - Name: Choose a name (e.g., `AD_DC01`).
   - Memory: Set to **4 GB**.
   - Hard Disk: Allocate **50 GB**.
   - Attach the downloaded ISO file as the virtual CD/DVD.
   - ![WindowsServer](https://i.imgur.com/79RnJtc.png)
4. Install Windows Server 2022:
   - Follow the on-screen instructions to complete the installation.

---
### Step 5: Ubuntu Server
1. Download the Ubuntu file from here [Ubuntu Server](https://ubuntu.com/download/server)
2. Head upto ORacle Virtual Box, hit new, and name your ubuntu server.
- ![Ubuntu Server](https://i.imgur.com/79RnJtc.png)
3. Boot up your Splunk Server by Hitting on **Start** in Virtual Box.
  - You should be shown the below screen.
  - ![Ubuntu Server](https://i.imgur.com/F85PKqB.png)
 4. Continue hitting next until you get the below screen.
- ![Ubuntu Server](https://i.imgur.com/DLNSOEj.png)
5. For this screen, choose your username and server name and lastly password. In the next screen skip SSh configuration. And lastly choose done.
6. Now our setup will install ubuntu server on our machine.
7. Once we are shown the below screen that has the *reboot** ption, click on it and we are done.
- ![Ubuntu Server](https://i.imgur.com/D6WpSRc.png)


---
- Your Virtual Box should look like below
- ![Virtual Box](https://i.imgur.com/aT2iBuX.png)
## Final Notes
After completing these steps, you should have the following virtual machines installed:
1. Windows 10 (Target machine).
2. Kali Linux (Attacker machine).
3. Windows Server 2022 (Domain Controller).
4. Ubuntu Server.

