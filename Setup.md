# Proxmox VE Setup Guide

## Introduction

Proxmox Virtual Environment (VE) is an open-source platform for enterprise virtualization. This guide will walk you through the installation and initial configuration of Proxmox VE on your server.

## Prerequisites

- Hardware capable of running promox 
- A bootable USB drive or CD with the Proxmox VE ISO.
- Basic knowledge of server hardware and networking.

## Step 1: Download Proxmox VE

1. Go to the Proxmox VE Download Page
2. Download the latest Proxmox VE ISO image.

## Step 2: Create Bootable Installation Media

1. **Using a USB Drive:**
   - Use tools like Rufus, Etcher (Windows) or `dd` (Linux/macOS) to create a bootable USB drive.
     ```bash
     dd if=/path/to/proxmox-ve.iso of=/dev/sdX bs=4M
     ```
   - Replace `/dev/sdX` with your USB device identifier.

2. **Using a CD/DVD:**
   - Burn the ISO to a CD/DVD using your preferred burning software.

## Step 3: Install Proxmox VE

1. **Boot from Installation Media:**
   - Insert the USB drive or CD/DVD into the server and boot from it.

2. **Start the Installer:**
   - Select `Install Proxmox VE` from the boot menu.

3. **Follow the Installation Wizard:**
   - Accept the EULA.
   - Select the target hard drive for installation.
   - Configure the country, time zone, and keyboard layout.
   - Set up the network configuration (IP address, gateway, DNS).
   - Create the root password and provide an email address for notifications.

4. **Complete Installation:**
   - The installer will copy files and configure the system.
   - Once complete, remove the installation media and reboot the server.

## Step 4: Initial Configuration

1. **Access the Web Interface:**
   - Open a web browser and navigate to `https://<your-server-ip>:8006`.
   - Log in using the `root` user and the password you set during installation.

2. **Configure Storage:**
   - Go to `Datacenter` > `Storage`.
   - Add or configure storage options based on your needs (e.g., local storage, network storage).

3. **Set Up Networking:**
   - Go to `Datacenter` > `Nodes` > `<Your Node>` > `Network`.
   - Configure network interfaces and VLANs as needed.

4. **Create Virtual Machines or Containers:**
   - Navigate to `Datacenter` > `Nodes` > `<Your Node>` > `Create VM` or `Create CT`.
   - Follow the wizard to set up new virtual machines or containers.

5. **Update Proxmox VE:**
   - Go to `Node` > `Updates`.
   - Click `Refresh` to check for updates and install them as needed.

## Step 5: Backup and Maintenance

1. **Set Up Backups:**
   - Go to `Datacenter` > `Backup`.
   - Configure backup schedules and targets.

2. **Regular Maintenance:**
   - Monitor system performance and logs.
   - Regularly check for updates and apply them.
