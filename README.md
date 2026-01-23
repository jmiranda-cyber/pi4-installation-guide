# pi4-installation-guide
A comprehensive guide to installing Raspberry Pi OS on a Pi 4, featuring solutions for Windows Defender conflicts and SD card recovery.

Raspberry Pi 4: OS Installation & Windows Troubleshooting Guide

Overview
Setting up a Raspberry Pi 4 is usually straightforward, but security features in Windows 11 can often block the imaging process, leading to write errors and "disappearing" SD cards. This guide walks through the full installation process, specifically focusing on how to resolve Windows Defender conflicts and use Disk Management to recover unallocated space on an SD card.

Prerequisites
Before starting, ensure you have the following:

Hardware: Raspberry Pi 4, Micro SD Card 32 GB at least, and a Card Reader.

Software: Raspberry Pi Imager installed on a Windows PC.

🛠️ Installation & Troubleshooting Walkthrough
1. The Initial Setup & Known Error ⚠️
When attempting to flash the OS, you may encounter a "Write Error". This typically happens because Windows Defender blocks the imager from writing to the disk.

[Insert Image: 01_imager_error.png]  ![]images/01_imager_error.png

2. Resolving Security Blocks 🛡️
To allow the imager to work, adjust these settings in Windows Security:

Disable Controlled Folder Access: Navigate to Ransomware Protection and toggle "Controlled folder access" to Off. [Insert Image: 03_ransomware_toggle.png]

Add an Exclusion: Add the file path for the Raspberry Pi imager to the exclusions list. [Insert Image: 02_defender_exclusion.png]

3. Recovering the "Missing" SD Card 💾
A failed write attempt can make the SD card disappear from Windows Explorer because it becomes "unallocated". Fix this in Disk Management:

Locate the Disk: Find the unallocated SD card. [Insert Image: 04_unallocated_disk.png]

Assign Volume: Right-click the space and use the New Simple Volume Wizard to assign a drive letter. [Insert Image: 05_new_volume_wizard.png]

Format & Verify: Once formatted as FAT32, the card will reappear in Explorer. [Insert Image: 06_formatted_explorer.png]

4. Final Verification ✅
With security exclusions set and the SD card partitioned, the installation will complete, and you can boot into the Raspberry Pi OS desktop.

[Insert Image: 07_success_desktop.png]



