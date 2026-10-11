# Lab 01: Windows Server 2016 Installation and Initial Setup

## 1. Objective

Install Windows Server 2016 in Oracle VirtualBox and complete the initial server configuration.

## 2. Environment

- Operating system: Windows Server 2016
- Hypervisor: Oracle VirtualBox
- Network configuration: To be documented
- Server role: Standalone server

## 3. Tasks

- [ ] Install Windows Server 2016
- [ ] Set the computer name
- [ ] Configure the administrator account
- [ ] Review server configuration in Server Manager
- [ ] Inspect the network adapter configuration
- [ ] Test network connectivity
- [ ] Document any issues encountered

## 4. Implementation

### a INSTALL WINDOWS SERVER 2016
---------------------------
First, I created a new virtual machine in Oracle VirtualBox and installed Windows Server 2016.
![Windows Server 2016 virtual machine in VirtualBox](./../images/vb.png)


After installation: The machine booted with success and desktop was displayed after login.
![Windows Server 2016 Desktop](./../images/desktop.png)



Changed the hostname of the server to WINDO-SERVER01 using the shell command 
``` powershell
Rename-Computer -NewName "WINDO-SERVER01"
Restart-Computer
```
![Windows Server 2016 Hostname Change](./../images/hostname.png)

 .. CHECKED NETWORK CONFIGURATIONS USING THE 'IPCONFIG /ALL' COMMAND AND VERIFIED THAT THE IP ADDRESS IS 10.0.2.100
 ```bash
 PS C:\WINDOWS\system32> ipconfig /all
```

![Windows Server 2016 Network Configuration](./../images/ip-add.png)

 ..Tested if Connection to the internet is active using
 ```bash
 ping 8.8.8.8
 ```
 which failed, i got error "DESTINATION HOST UNREACHABLE", on my host's side the NAT Adapter had no connection to the internet. I then reconfigured the NAT Adapter on my host's side and it worked
 
tried again
```bash
ping 8.8.8.8
```
and it worked

### UPDATED THE WINDOWS SERVER

Running the system update through the control panel
![Windows Updates Screen](./../images/windows-updates.png)

### Perfomed Date  and Time settings with correct time zone
![Windows Date and Time Settings](./../images/time.png)
