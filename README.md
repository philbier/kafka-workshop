# Apache Kafka Workshop

## Set up environment
### Install WSL
#### Enable the Windows Subsystem for Linux
Turn on the Windows Subsystem for Linux feature before installing a Linux distribution. Open PowerShell as an administrator, and run the following command:
```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```
This may take a minute or two. Your output should resemble the following:
```powershell
Deployment Image Servicing and Management tool
Version: 10.0.18362.1139

Image Version: 10.0.18363.1139

Enabling feature(s)
[==========================100.0%==========================]
The operation completed successfully.
```

#### Enable the Virtual Machine feature
WSL 2 requires the Virtual Machine Platform feature. In PowerShell, run the following command:
```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

#### Get the Linux kernel update
[Download the Linux kernel update package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi), which is a regular Windows Installer (.msi) file.
Double-click the .msi file to install the WSL 2 update. If you’re prompted for elevated permissions, select Yes to approve the installation.

#### Set the default WSL version
In PowerShell, run the following command to set WSL 2 as the default version for your Linux distributions:
```powershell
wsl --set-default-version 2
```
Your output should resemble the following:
```powershell
For information on key differences with WSL 2 please visit https://aka.ms/wsl2
```
:congratulations: WSL 2 is ready to use. For more information on installing WSL 2, including troubleshooting, see Windows Subsystem for Linux Installation Guide for Windows 10.


### Install your preferred Linux distribution
Install Linux from the Microsoft Store, the same way you install other applications on Windows. 
Open the Microsoft Store app and search for “Linux.”

![Linux Distributions in Microsoft Store](./img/ms_store.png)

Select **Ubuntu 20.04** LTS and click **Install**.

When the installation is complete, click **Launch**. The shell opens and displays the following message:
```powershell
Installing, this may take a few minutes...
Please create a default UNIX user account. The username does not need to match your Windows username.
For more information visit: https://aka.ms/wslusers
Enter new UNIX username:
```
Enter a username and password to complete the installation.

![Linux Distributions in Microsoft Store](./img/ubuntu_shell.png)

### Install Java
Run the package manager to get the latest updates. In the Ubuntu shell window that opened above, run the following commands:
```bash
sudo apt-get update && sudo apt-get upgrade -y
```

> :information_source: Tip: Right-click pastes text into the terminal window.

Kafka requires the Java runtime to be version 8 or higher. Check the Java version in your Linux installation:
```bash
java -version
```

Your output should resemble this:
```bash
openjdk version "1.8.0_265"
OpenJDK Runtime Environment (build 1.8.0_265-8u265-b01-0ubuntu2~20.04-b01)
OpenJDK 64-Bit Server VM (build 25.265-b01, mixed mode)
```

If Java isn’t installed (likely) or it’s not the right version, install it by using your distribution’s package manager. There are a lot of ways to install Java. On Ubuntu, this is one of the simplest:
```bash
sudo apt install openjdk-8-jdk -y
```







<TODO: Add link Screencast on YouTube>


