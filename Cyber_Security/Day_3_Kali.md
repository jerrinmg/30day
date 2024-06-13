# Day 3: ReInstallation Nightmare!

As Kali Linux OS that I had installed earlier was not functioning properly ( No wifi detetction of onboard Laptop WiFi card, No sound and some other issues ) so I decided to reinstall the OS. 

# Dual-Booting Kali Linux and Ubuntu: A Comprehensive Guide

## Introduction

Setting up a dual-boot system with Kali Linux and Ubuntu on separate SSDs was a complex process. This guide chronicles the journey, challenges, and solutions encountered while setting up such a system. It aims to provide a reference for anyone attempting a similar setup.

## Table of Contents
1. [Initial Setup and Preparation](#initial-setup-and-preparation)
2. [Checksum Verification](#checksum-verification)
3. [First Kali Linux Installation Attempt](#first-kali-linux-installation-attempt)
4. [Dealing with GRUB Rescue](#dealing-with-grub-rescue)
5. [Partition Management](#partition-management)
6. [Using Windows `diskpart` for Boot Entry Management](#using-windows-diskpart-for-boot-entry-management)
7. [Creating and Managing EFI Partitions](#creating-and-managing-efi-partitions)
8. [Ubuntu Installation and Swap Area Issues](#ubuntu-installation-and-swap-area-issues)
9. [Final Configuration and Validation](#final-configuration-and-validation)
10. [Key Takeaways](#key-takeaways)

## Initial Setup and Preparation

### Hardware and Software:
- **SSD1:** Contains Windows installation with EFI partition.
- **SSD2:** Dedicated for Kali Linux and Ubuntu installations.

### Tools Used:
- Rufus for creating bootable USB drives.
- GParted for partition management.
- `bcdedit` and `diskpart` for managing boot entries in Windows.

## Checksum Verification

Before proceeding with the installation, it's crucial to verify the integrity of the downloaded ISO files.

1. **Download the SHA256 checksum file** from the official website.
2. **Verify the ISO file** using a tool like `sha256sum` on Linux or PowerShell on Windows.

```sh
# Example command on Linux
sha256sum kali-linux-2023.2-installer-amd64.iso
```

Compare the output with the official checksum provided.
![image](https://github.com/jerrinmg/30day/assets/166682032/7f9b0fab-6569-478c-b656-8dffd4a8767b)

## First Kali Linux Installation Attempt

### Issues Encountered:
- The installer failed to process the pre-config file.
- Encountered checksum errors.

### Solution:
- Verified ISO integrity again.
- Recreated the bootable USB drive using Rufus.

## Dealing with GRUB Rescue

After the first failed installation, booting into Kali Linux led to the `grub rescue` mode.![image](https://github.com/jerrinmg/30day/assets/166682032/15d22ee6-7aca-4f2d-ab6a-edbef774d2bb)


### Steps Taken:
1. **Identified the issue** with GRUB not finding the correct filesystem.
2. **Booted using a live USB** to access the system and attempted to repair GRUB.

```sh
# Example commands to repair GRUB
sudo mount /dev/sdX /mnt
sudo grub-install --root-directory=/mnt /dev/sdX
sudo update-grub
```

## Partition Management

### Partition Setup:
- **SSD1 (Windows)**
  - 100 MB EFI partition
  - Windows partitions
- **SSD2**
  - New EFI partition (550 MB)
  - Boot partition (1 GB)
  - Root partition (206 GB for Kali)
  - Old Ubuntu partition (204 GB)
  - Swap area (8 GB)
  - 40 GB left unallocated

## Using Windows `diskpart` for Boot Entry Management

1. **Opened Command Prompt as Administrator**.
2. **Used `diskpart` to manage and clean disk partitions**.
Refer to this guide:https://www.youtube.com/watch?v=A9ENrfybOq8&t=1s

## Creating and Managing EFI Partitions

### Creation:
- Created a new EFI partition during Kali Linux installation.
- Ensured it was formatted as FAT32.

### Management:
- Verified and set the boot flag using GParted.

## Ubuntu Installation and Swap Area Issues

### Problem:
During the Ubuntu installation, the swap area was not automatically detected.

## Final Configuration and Validation

After installing both operating systems and configuring the necessary partitions and boot entries, the system was tested for proper functionality.

### Verification Steps:
1. **Checked BIOS settings** to ensure correct boot order.
2. **Validated GRUB menu** to ensure all entries were present.
3. **Booted into each OS** to verify successful installation and configuration.

## Key Takeaways

- **Persistence and Problem-Solving:** The process required a methodical approach and continuous learning.
- **Tool Proficiency:** Gained in-depth knowledge of tools like GParted, `diskpart`, and `bcdedit`.
- **Community and Documentation:** Leveraged community support and extensive documentation to navigate complex issues.

---

By sharing this journey, I hope to provide valuable insights and a detailed reference for anyone facing similar challenges with dual-boot setups.

## Troubleshooting and Lessons Learned

### Existing Dual-Boot Setup

Initially, both Kali Linux and Ubuntu were installed on SSD2. However, Kali Linux was not working correctly while Ubuntu was functioning fine. The initial attempt to reinstall Kali Linux without formatting the `/boot` partition led to issues as both Ubuntu and Kali shared the same partition sizes, making it difficult to identify and manage them properly.

### Reinstallation and GRUB Issues

Upon reinstalling Kali Linux, I encountered persistent GRUB-related issues:
- The system fell into `grub rescue` mode.
- Even after formatting the SSD2 partition, the boot menu entries for Kali Linux remained.
- Ubuntu's swap area was also not working post-reinstallation.

### Comprehensive Reinstallation Strategy

Given the persistent issues, I decided to reinstall both operating systems with updated versions:
- Ubuntu 20.04 to 24.04
- Kali Linux 2024.1 to 2024.2
![image](https://github.com/jerrinmg/30day/assets/166682032/43e82748-4418-4f95-8d12-e5381aca49e4)

This approach was chosen to ensure compatibility and resolve the existing boot issues comprehensively.

### Manual GRUB Cleanup and EFI Management

Despite formatting, the old boot entries persisted. This required:
- Using `diskpart` in Windows to manually remove unwanted boot entries.
- Creating and configuring a new EFI partition during the reinstallation process to prevent conflicts.

### Post-Installation Configuration

Upon successful installation:
- **Swap Area Configuration:** Ensured both operating systems correctly utilized the swap area.
- **EFI Management:** Copied necessary EFI files to ensure smooth boot operations.

---

This journey encompassed a range of tools, troubleshooting steps, and extensive learning, ultimately leading to a successful dual-boot setup. 
