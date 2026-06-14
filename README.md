ubuntu-vm-setup

Project Overview

This project demonstrates the setup of a Linux virtual machine using Oracle VirtualBox with an Ubuntu operating system. It is part of my DevOps learning journey to build hands-on experience with Linux systems, virtualization, networking, and SSH access.

The lab environment created here serves as a foundation for practicing real-world DevOps and system administration tasks.


        Objectives

- Install and configure Oracle VirtualBox
- Create and set up an Ubuntu virtual machine
- Understand virtualization concepts
- Configure networking (NAT / Bridged Adapter)
- Enable and use SSH for remote access
- Build a reusable Linux lab environment for DevOps practice

       Tools & Technologies

- Oracle VirtualBox
- Ubuntu (Intel/AMD64 version)
- Windows Host Machine (HP EliteBook 840 G5)
- SSH (OpenSSH Server)
- Linux Command Line

---

      Virtual Machine Configuration

- OS Type: Ubuntu 64-bit  
- RAM: 2GB – 4GB  
- CPU: 2 Cores  
- Storage: 20GB Dynamic Disk  
- Network Mode: NAT (with optional Bridged Adapter)


       Setup Process Summary

1. Install VirtualBox
Downloaded and installed Oracle VirtualBox and Extension Pack.

2. Download Ubuntu ISO
Downloaded Ubuntu ISO (Intel/AMD64 architecture).

3. Create Virtual Machine
Created a new VM and allocated memory, CPU, and storage.

4. Install Ubuntu OS
Mounted ISO and completed Ubuntu installation process.

5. Configure Networking
Configured NAT for internet access and optionally Bridged Adapter for local network access.

6. Install SSH Server
Installed and enabled OpenSSH server:

sudo apt update
sudo apt install openssh-server -y


    Virtual Machine Boot & Installation Process

This section documents the process of booting and installing Ubuntu on a VirtualBox virtual machine.

                                              Boot Menu

After starting the virtual machine, the following boot options appeared:

- Try or Install Ubuntu
- Ubuntu (Safe Graphics Mode)

The standard option selected: Try or Install Ubuntu 

This launches the Ubuntu installer environment.

                                             Installation Steps

The installation process follows these stages:
1. Language Selection
- English (or preferred language)

2. Keyboard Layout
- Default layout selected

3. Updates & Software
- Normal installation selected
- Option to download updates enabled (recommended)

4. Installation Type
- Erase disk and install Ubuntu (virtual disk only)

5. User Setup
- Username created
- Password configured
- Hostname defined (e.g., ubuntu-vm)

                                       Virtual Machine Configuration

- RAM: 2GB – 4GB  
- CPU: 2 cores  
- Storage: 20GB – 25GB (dynamic disk)  
- Network Mode: NAT  

                                        Screenshots (To Be Added)

The following screenshots will be included in the `images/` folder:

- VirtualBox VM creation screen  
- Ubuntu boot menu  
- Installation wizard steps  
- User account setup  
- Installation progress screen  
- Successful login screen  


                                                Objective

The goal of this setup is to:

- Build a Linux-based development environment
- Practice system administration skills
- Understand virtualization concepts
- Prepare a foundation for DevOps tools (SSH, Docker, etc.)

                                        Ubuntu Installation Completion

Status
The Ubuntu virtual machine has been successfully installed and is now running inside Oracle VirtualBox.

The system booted into the Ubuntu desktop environment after completing the installation process.

                                            Post-Installation Setup

After installation, the following steps were completed:
System Boot
- Ubuntu successfully booted into the desktop environment
- Virtual machine is running normally on VirtualBox

                                               System Update
The system was updated using:
sudo apt update && sudo apt upgrade -y
                                     SSH Setup and Remote Access Configuration

                                              Overview of SSH

SSH (Secure Shell) is a network protocol used to securely access and manage a remote machine over an unsecured network.

In this project, SSH is used to:
- Access the Ubuntu virtual machine remotely from the host system
- Practice basic Linux server management
- Simulate real-world DevOps remote server administration

SSH is a fundamental tool in DevOps, Cloud Computing, and System Administration.

                                            SSH Installation Process

1. Install OpenSSH Server
Run the following command inside the Ubuntu VM:
sudo apt install openssh-server -y
System Issue: Debian Package Manager DPKG Configuration Error

Problem Description

During system setup and package installation, an error was encountered indicating that some packages were not fully configured.

The system displayed the following message:
> "You must manually run `sudo dpkg --configure -a` to correct the problem"

This indicates that the package installation process was interrupted or not completed successfully.

Cause of the Issue
This issue commonly occurs due to:
- Interrupted installation or update process
- System shutdown during package configuration
- Background package installation not completing properly
- Virtual machine instability during setup

Solution Applied
To resolve the issue, the following steps were executed:
1. Reconfigure dpkg
sudo dpkg --configure -a

                                Starting and Checking SSH Service on Ubuntu VM

Objective
This section documents how the SSH service was started, enabled, and verified on an Ubuntu Virtual Machine to ensure remote access is working properly.

Starting the SSH Service

After installing OpenSSH Server, the SSH service was started using:
sudo systemctl start ssh

To ensure SSH starts automatically on system boot:
sudo systemctl enable ssh

Checking SSH Service Status
The status of the SSH service was verified using:
sudo systemctl status ssh
