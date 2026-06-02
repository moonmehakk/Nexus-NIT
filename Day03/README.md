# Welcome to NIT Academy - Day 3

> **Student:** Mehak Ubed
> **Day-3:** Monday 11th May, 2026

---

# Table of Contents

| Task | Title                            | Summary                               |
| ---- | -------------------------------- | ------------------------------------- |
| 1    | Open PowerShell as Administrator | Open elevated PowerShell              |
| 2    | Check if WSL is Installed        | Verify existing WSL installation      |
| 3    | Check Installed Linux Distros    | View installed Linux distributions    |
| 4    | Check Available Distros          | View downloadable Linux distros       |
| 5    | Install WSL                      | Install WSL and Ubuntu                |
| 6    | Install Specific Distro          | Install Ubuntu or other distributions |
| 7    | First Linux Setup                | Configure Linux username and password |
| 8    | Start WSL Manually               | Launch Linux manually                 |
| 9    | Verify Linux Is Working          | Test Linux functionality              |
| 10   | Check WSL Version                | Verify WSL 2 installation             |
| 11   | Convert Existing Distro to WSL 2 | Upgrade distro version                |
| 12   | Set Default Distro               | Configure default Linux distro        |
| 13   | Shutdown and Restart WSL         | Restart Linux environment             |
| 14   | Access Windows Files from Linux  | Access Windows drives                 |
| 15   | Access Linux Files from Windows  | Access Linux files from Explorer      |
| 16   | Common Commands                  | Frequently used commands              |
| 17   | Common Problems and Fixes        | Beginner troubleshooting              |
| 18   | Final Verification Checklist     | Confirm installation success          |

---

# Introduction

## What is WSL?

Windows Subsystem for Linux (WSL) allows users to run a Linux environment directly inside Windows without requiring:

* Dual Boot
* Virtual Machines
* Additional Hypervisors

WSL provides a seamless Linux experience for learning Linux, DevOps, Cloud, and System Administration.

---

# Learning Objectives

By completing Day 3, I learned how to:

* Install WSL on Windows
* Install Ubuntu Linux
* Verify Linux functionality
* Upgrade to WSL 2
* Manage Linux distributions
* Access files between Windows and Linux
* Troubleshoot common WSL issues

---

# Task 1 - Open PowerShell as Administrator

## Objective

Launch PowerShell with administrative privileges.

### Steps

1. Open Start Menu
2. Search for PowerShell
3. Right-click Windows PowerShell
4. Select **Run as Administrator**

---

# Task 2 - Check if WSL is Already Installed

## Command

```powershell
wsl --status
```

## Purpose

Verify whether WSL is already installed and check:

* WSL Version
* Kernel Version
* Default Distribution
* Default Version

---

# Task 3 - Check Installed Linux Distros

## Command

```powershell
wsl --list --verbose
```

or

```powershell
wsl -l -v
```

## Example Output

```text
NAME      STATE           VERSION
Ubuntu    Stopped         2
```

## Learning Outcome

* Identified installed Linux distributions
* Verified WSL version

---

# Task 4 - Check Available Linux Distros

## Command

```powershell
wsl --list --online
```

or

```powershell
wsl -l -o
```

## Purpose

View all Linux distributions available for installation.

Examples:

* Ubuntu
* Debian
* Kali Linux
* openSUSE

---

# Task 5 - Install WSL with Default Ubuntu

## Command

```powershell
wsl --install
```

## Result

This installs:

* WSL
* Ubuntu Linux
* WSL 2

---

# Task 6 - Install a Specific Distro

## View Available Distros

```powershell
wsl --list --online
```

## Install Ubuntu

```powershell
wsl --install -d Ubuntu
```

## Learning Outcome

Successfully installed a specific Linux distribution.

---

# Task 7 - First Linux Setup

## Configure Linux User

Linux requests:

```text
Enter new UNIX username:
New password:
Retype new password:
```

## Notes

* Username can be different from Windows username.
* Password characters are hidden while typing.
* Password should be remembered securely.

---

# Task 8 - Start WSL Manually

## Start Default Distro

```powershell
wsl
```

## Start Ubuntu Directly

```powershell
wsl -d Ubuntu
```

---

# Task 9 - Verify Linux Is Working

## Commands Executed

```bash
whoami
pwd
uname -a
cat /etc/os-release
```

## Purpose

Verify Linux installation and distribution details.

---

# Linux Package Updates

## Update Package Repository

```bash
sudo apt update
```

## Upgrade Installed Packages

```bash
sudo apt upgrade -y
```

---

# Task 10 - Check WSL Version

## Commands

```powershell
wsl --version
```

```powershell
wsl -l -v
```

## Expected Result

```text
VERSION
2
```

---

# Task 11 - Convert Existing Distro to WSL 2

## Command

```powershell
wsl --set-version Ubuntu 2
```

## Verification

```powershell
wsl -l -v
```

## Learning Outcome

Successfully converted Ubuntu to WSL 2.

---

# Task 12 - Set Default Distro

## Command

```powershell
wsl --set-default Ubuntu
```

## Purpose

Set Ubuntu as the default Linux distribution.

---

# Task 13 - Shutdown and Restart WSL

## Shutdown

```powershell
wsl --shutdown
```

## Restart

```powershell
wsl -d Ubuntu
```

---

# Task 14 - Access Windows Files from Linux

## Example

```bash
cd /mnt/c/Users
ls
```

## Learning Outcome

Accessed Windows files directly from Linux.

---

# Task 15 - Access Linux Files from Windows

## Open File Explorer

```text
\\wsl$
```

## Example

```text
\\wsl$\Ubuntu
```

## Learning Outcome

Accessed Linux files directly from Windows Explorer.

---

# Task 16 - Common Commands for Students

| Task                   | Command                       |
| ---------------------- | ----------------------------- |
| Check WSL status       | `wsl --status`                |
| List installed distros | `wsl -l -v`                   |
| List online distros    | `wsl -l -o`                   |
| Install WSL            | `wsl --install`               |
| Install Ubuntu         | `wsl --install -d Ubuntu`     |
| Start WSL              | `wsl`                         |
| Start Ubuntu           | `wsl -d Ubuntu`               |
| Shutdown WSL           | `wsl --shutdown`              |
| Set WSL2 default       | `wsl --set-default-version 2` |
| Set default distro     | `wsl --set-default Ubuntu`    |

---

# Task 17 - Common Problems and Fixes

## Problem 1 - WSL Command Not Recognized

### Solution

```powershell
wsl --install
```

Restart the computer and try again.

---

## Problem 2 - No Linux Distro Installed

### Solution

```powershell
wsl --install -d Ubuntu
```

---

## Problem 3 - Ubuntu Opens Then Closes

### Solution

```powershell
wsl -d Ubuntu
```

Review any error messages displayed.

---

## Problem 4 - Forgot Linux Password

### Open Root Shell

```powershell
wsl -u root
```

### Reset Password

```bash
passwd username
```

---

## Problem 5 - Distro Running WSL 1

### Convert to WSL 2

```powershell
wsl --set-version Ubuntu 2
```

---

# Task 18 - Final Verification Checklist

## PowerShell Verification

```powershell
wsl --status
wsl -l -v
```

## Start Ubuntu

```powershell
wsl -d Ubuntu
```

## Linux Verification

```bash
whoami
pwd
cat /etc/os-release
sudo apt update
```

If all commands execute successfully, WSL installation is complete.

---

# Final Summary

## Skills Learned

* Installing WSL
* Installing Ubuntu Linux
* Managing Linux distributions
* Upgrading to WSL 2
* Accessing files between Windows and Linux
* Troubleshooting WSL issues
* Working with Linux commands

---

# Author

**Mehak Ubed**
NIT Academy – Linux, DevOps & SRE Learning Journey 🚀
