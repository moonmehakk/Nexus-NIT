# Welcome to NIT Academy - Day 09

> **Student:** Mehak Ubed
> **Day-09:** Sunday 17th May, 2026

---

# Table of Contents

| Task | Title                              | Summary                                    |
| ---- | ---------------------------------- | ------------------------------------------ |
| 1    | Understanding the Linux Filesystem | Learn filesystem fundamentals              |
| 2    | Explore the Root Filesystem        | Understand important Linux directories     |
| 3    | Linux Users and Prompts            | Learn user types and shell prompts         |
| 4    | Tree Command Practice              | Visualize directory structures             |
| 5    | Filesystem Layers                  | Understand VFS and filesystem architecture |
| 6    | LS Command Practice                | Learn file listing commands                |
| 7    | Metadata and Inodes                | Understand file tracking in Linux          |
| 8    | Filesystem Snapshot Activity       | Explore filesystem hierarchy               |
| 9    | Absolute vs Relative Paths         | Learn Linux navigation                     |
| 10   | Linux Boot Process                 | Introduction to system startup             |
| 11   | Explore the /boot Directory        | Learn boot-related files                   |
| 12   | BIOS vs UEFI                       | Understand firmware concepts               |
| 13   | POST and Hardware Checks           | Learn startup hardware validation          |
| 14   | Bootloader and Kernel              | Introduction to boot components            |
| 15   | Systemd Targets                    | Understand Linux targets                   |
| 16   | Shutdown and Reboot Commands       | Learn power management                     |
| 17   | Understanding /home                | User home directories                      |
| 18   | Understanding /dev                 | Device files in Linux                      |
| 19   | Block vs Character Devices         | Learn Linux device types                   |
| 20   | TTY and Pseudo Terminals           | Understand Linux terminals                 |
| 21   | Disk Commands Practice             | Learn storage management commands          |
| 22   | Sensors in Linux                   | Hardware monitoring                        |
| 23   | Understanding /etc                 | Linux configuration files                  |
| 24   | Understanding /var                 | Variable data storage                      |
| 25   | Linux Logging System               | Learn log management                       |
| 26   | Understanding logrotate            | Log rotation concepts                      |
| 27   | Final Reflection                   | Review learning outcomes                   |

---

# Introduction

Day 09 focused on one of the most important Linux concepts: the Linux Filesystem.

Understanding the filesystem is essential for Linux administration because every configuration file, application, device, process, and log is represented within the filesystem hierarchy.

---

# Learning Objectives

By completing Day 09, I learned about:

* Linux filesystem structure
* Important system directories
* User permissions and shell prompts
* Inodes and metadata
* Linux boot files
* Device management
* Storage and disk commands
* Linux logging systems
* System administration fundamentals

---

# Task 1 - Understanding the Linux Filesystem

## What is a Filesystem?

A filesystem is the method Linux uses to organize, store, and retrieve files and directories.

## What is the Root Directory?

The root directory (`/`) is the top-level directory in Linux from which all other directories originate.

## Why is Linux Called a Hierarchical Filesystem?

Because files and directories are organized in a tree-like structure with the root directory at the top.

## Purpose of Directories

Directories help organize files logically and make system management easier.

---

# Task 2 - Explore the Root Filesystem

## Important Linux Directories

| Directory | Purpose                                |
| --------- | -------------------------------------- |
| `/boot`   | Bootloader and kernel files            |
| `/home`   | User home directories                  |
| `/etc`    | System configuration files             |
| `/dev`    | Device files                           |
| `/var`    | Variable data such as logs             |
| `/tmp`    | Temporary files                        |
| `/usr`    | User applications and utilities        |
| `/proc`   | Virtual process and kernel information |

---

# Task 3 - Understanding Linux Users and Prompts

## User Types

### Root User

Has unrestricted administrative privileges.

### Sudo User

Can temporarily perform administrative tasks.

### Regular User

Has limited permissions for daily activities.

## Shell Prompt Symbols

```bash
#
```

Represents the root user.

```bash
$
```

Represents a normal user.

## Questions

### Difference Between Root and Regular User

Root has full control of the system, while regular users have restricted permissions.

### What is sudo?

Sudo allows authorized users to execute commands with administrative privileges.

---

# Task 4 - Install and Use the Tree Command

## Installation

```bash
dnf install tree -y
```

## Commands

```bash
tree -d /boot
tree /boot
tree -a -L 2 -h -C
```

## Questions

### What Does tree -d Show?

Displays directories only.

### What Does -L 2 Mean?

Limits output to two directory levels.

### Why Is Tree Useful?

It provides a visual representation of directory structures.

---

# Task 5 - Linux Filesystem Layers

## Logical File System

Provides the user interface for file operations.

## Virtual File System (VFS)

Acts as an abstraction layer between applications and physical filesystems.

## Physical File System

Stores actual data on storage devices.

## Why is /proc/cpuinfo Virtual?

Because the information is generated dynamically by the kernel and not stored on disk.

---

# Task 6 - Practice the LS Command

## Commands

```bash
ll
ls -l /
ls -ld /
ls -al /
ls -il /
```

## Questions

### Difference Between ls -l / and ls -ld /

* `ls -l /` lists directory contents.
* `ls -ld /` shows information about the directory itself.

### What Does -i Display?

Displays inode numbers.

### What is Metadata?

Metadata is information about a file such as permissions, ownership, timestamps, and size.

---

# Task 7 - Understanding Metadata and Inodes

## What is an Inode?

An inode is a data structure that stores metadata about a file.

## Information Stored in an Inode

* File permissions
* Ownership
* File size
* Timestamps
* File type

## Does an Inode Store File Data?

No. It stores metadata and pointers to the data blocks.

## Why Are Inodes Important?

Linux uses them to locate and manage files efficiently.

## Commands Practiced

```bash
df -i
ls -il
stat /boot
```

---

# Task 8 - Filesystem Snapshot Activity

## Linux Filesystem Hierarchy

```text
/
├── boot
├── home
├── etc
├── dev
├── usr
├── var
├── tmp
└── proc
```

---

# Task 9 - Absolute vs Relative Paths

## Absolute Path

Starts from the root directory.

Example:

```bash
/home/mehak
```

## Relative Path

Starts from the current directory.

Example:

```bash
Documents
```

## Commands Practiced

```bash
pwd
cd /home
cd ..
cd .
```

---

# Task 10 - Linux Boot Process

## Question

What Happens if the Bootloader is Corrupted?

The system may fail to boot because it cannot locate or load the operating system kernel.

---

# Task 11 - Explore the /boot Directory

## Commands

```bash
ls -l /boot
tree -d /boot
```

## Important Files

### grub.cfg

GRUB configuration file.

### initramfs

Temporary root filesystem used during boot.

### vmlinuz

Compressed Linux kernel image.

### System.map

Contains kernel symbol information.

---

# Task 12 - BIOS vs UEFI

## BIOS

Traditional firmware used to initialize hardware during startup.

## UEFI

Modern replacement for BIOS with improved functionality and security.

---

# Task 13 - POST and Hardware Checks

## What Does POST Check?

* CPU
* RAM
* Storage Devices
* Keyboard
* GPU

### What Happens if RAM Fails?

The system will usually stop booting and display an error or beep code.

---

# Task 14 - Bootloader and Kernel

## Bootloader

Loads the operating system kernel.

## Kernel

Core component that manages hardware and system resources.

---

# Task 15 - Systemd Targets

Systemd targets define different operating states of a Linux system and replace traditional runlevels.

---

# Task 16 - Shutdown and Reboot Commands

## Commands Studied

```bash
systemctl reboot
shutdown -r now
systemctl poweroff
```

## Difference Between Reboot and Poweroff

* Reboot restarts the system.
* Poweroff shuts the system down completely.

## What Does shutdown -c Do?

Cancels a scheduled shutdown.

---

# Task 17 - Understanding /home

## Purpose of /home

Stores personal files and settings for users.

## Login Location

Users typically start in their home directory after logging in.

## Why Are Initialization Files Important?

They customize the user environment and shell behavior.

---

# Task 18 - Understanding /dev

## Commands

```bash
ls /dev
ls -l /dev/sda1
```

## Questions

### Why is Everything Treated as a File?

Linux follows the philosophy that devices and resources can be accessed like files.

### What is /dev/sda?

Represents a storage device.

### What is udev?

A device manager responsible for dynamically creating device files.

---

# Task 19 - Block Devices vs Character Devices

## Block Devices

Transfer data in blocks.

Example:

* Hard Drives
* SSDs

## Character Devices

Transfer data one character at a time.

Example:

* Keyboard
* Mouse
* Serial Ports

---

# Task 20 - TTY and Pseudo Terminals

## Commands

```bash
tty
w
who
ls /dev/pts
```

## Questions

### What is tty1?

A physical virtual terminal.

### What is pts/0?

A pseudo-terminal used by terminal emulators and remote sessions.

### What Does the w Command Display?

Shows logged-in users and their current activities.

---

# Task 21 - Disk Commands Practice

## Commands

```bash
df -hT
lsblk
fdisk -l
```

### Purpose

These commands display:

* Disk usage
* Block devices
* Partition information

---

# Task 22 - Sensors in Linux

## Installation

```bash
dnf install lm_sensors -y
```

## Commands

```bash
sensors-detect
sensors
```

## Questions

### What Does lm_sensors Do?

Monitors hardware temperatures, voltages, and fan speeds.

### Why Are Sensors Important?

They help prevent overheating and hardware failures.

---

# Task 23 - Understanding /etc

## Command

```bash
ls /etc
```

## Important Files

* `/etc/passwd`
* `/etc/shadow`
* `/etc/group`
* `/etc/sudoers`

### Why Should /etc Be Backed Up?

Because it contains critical system configuration files.

---

# Task 24 - Understanding /var

## Command

```bash
ls /var
```

## Important Directories

* `/var/log`
* `/var/cache`
* `/var/tmp`
* `/var/spool`

### Why Can /var Grow Large?

Because logs, caches, and temporary application data accumulate over time.

---

# Task 25 - Linux Logging System

## Commands

```bash
journalctl
tail -f /var/log/messages
```

## Questions

### Difference Between rsyslog and journald

* journald is part of systemd.
* rsyslog manages traditional log files.

### What Does journalctl Do?

Displays logs stored by systemd-journald.

### Where Are Logs Stored?

Typically inside:

```bash
/var/log
```

---

# Task 26 - Understanding logrotate

## Commands

```bash
cat /etc/logrotate.conf
ls /etc/logrotate.d/
```

## Questions

### What is logrotate?

A utility that manages and archives old log files.

### Why Is Log Rotation Important?

Prevents logs from consuming all available disk space.

### What Happens if Logs Are Never Rotated?

Disk storage may become full, causing system problems.

---

# Task 27 - Final Reflection

Module 02 provided a deeper understanding of the Linux filesystem and how Linux organizes files, directories, devices, and logs.

The most interesting directories were `/proc` and `/dev` because they demonstrate how Linux interacts with hardware and system processes.

The most useful commands were `tree`, `ls`, and `df` because they provide valuable information about the system structure and storage usage.

The most challenging topics were inodes and filesystem layers, but they became easier to understand through practice.

I would like to continue practicing filesystem navigation, permissions, storage management, and system administration commands.

---

# Skills Learned

* Linux Filesystem Structure
* Directory Management
* Metadata and Inodes
* Linux Boot Concepts
* Device Management
* Storage Administration
* Linux Logging
* System Administration Fundamentals

---

# Final Summary

Day 09 focused on understanding the Linux Filesystem, which is a core skill for every Linux Administrator.

The knowledge gained from exploring directories, inodes, devices, logs, and storage management provides a strong foundation for future Linux administration and RHCSA studies.

---

# Author

**Mehak Ubed**
NIT Academy – Linux, DevOps & SRE Learning Journey 🚀
