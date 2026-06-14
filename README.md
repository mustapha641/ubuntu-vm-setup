ubuntu-vm-setup

Project Overview

This project demonstrates the setup of a Linux virtual machine using **Oracle VirtualBox** with an Ubuntu operating system. It is part of my DevOps learning journey to build hands-on experience with Linux systems, virtualization, networking, and SSH access.

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

```bash
sudo apt update
sudo apt install openssh-server -y
