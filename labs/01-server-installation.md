# Install Windows Server 2019 and Configure Static IP

This document provides step-by-step instructions for installing Windows Server 2019 and configuring a static IP address.

## Prerequisites
- Windows Server 2019 ISO file
- VMWare Workstation Pro 
  - 4GB+ RAM
  - 2+ CPU cores
  - 40GB+ disk space
- Network connectivity


### 1. Windows Server Installation
- mount the ISO
- Boot the server from the installation media
- Wait for the Windows Setup screen to appear
1. Select your language preferences and click "Next"
2. Click "Install now"
3. Select "Windows Server 2019 Standard (Desktop Experience)" and click "Next"
4. Accept the license terms and click "Next"
5. Select "Custom: Install Windows only"
6. Select the disk for installation and click "Next"
7. Wait for installation to complete (system will restart multiple times)

### 2. Initial Configuration
1. Set administrator password when prompted
2. Press Ctrl+Alt+Del to unlock (if required)
3. Log in with the administrator credentials

### 3. Configuring Static IP Address
1. Right-click on the network icon in the taskbar
2. Select "Open Network & Internet settings"
3. Click on "Change adapter options"
4. Right-click on your network adapter and select "Properties"
5. Select "Internet Protocol Version 4 (TCP/IPv4)" and click "Properties"
6. Select "Use the following IP address" and enter:
   - IP address: 192.168.1.10 (or your preferred IP)
   - Subnet mask: 255.255.255.0
   - Default gateway: 192.168.1.1 (your router IP)
7. Select "Use the following DNS server addresses" and enter:
   - Preferred DNS server: 192.168.1.1 (or your preferred DNS)
   - Alternate DNS server: 8.8.8.8 (Google DNS)
8. Click "OK" to save changes

### 4. Verify Configuration
1. Open Command Prompt
2. Type `ipconfig /all` and press Enter
3. Verify that the IP address, subnet mask, default gateway, and DNS servers match your configuration

## Troubleshooting
- If you can't connect to the network after setting a static IP, verify that the IP address is not already in use on your network
- Ensure the default gateway is correct for your network environment
- If DNS resolution fails, check that your DNS server addresses are correct
