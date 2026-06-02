# Welcome to NIT Academy - Day 08

> **Student:** Mehak Ubed
> **Day-08:** Saturday 16th May, 2026

---

# Table of Contents

| Task | Title                               | Summary                                     |
| ---- | ----------------------------------- | ------------------------------------------- |
| 1    | Student Introduction & Goal Setting | Define personal learning objectives         |
| 2    | Understanding the IT Ecosystem      | Explore Linux and IT careers                |
| 3    | Home Network Exploration            | Understand networking fundamentals          |
| 4    | Router Functions                    | Learn DHCP, DNS, NAT, and Firewall concepts |
| 5    | Data Center and Server Concepts     | Understand modern infrastructure            |
| 6    | Server vs Laptop Comparison         | Compare enterprise and personal systems     |
| 7    | Server Hardware Identification      | Learn key hardware components               |
| 8    | Linux Boot Process                  | Understand system startup                   |
| 9    | Linux History                       | Research Linux origins                      |
| 10   | Linux Distribution Research         | Explore Linux distributions                 |
| 11   | Linux Shell Exploration             | Learn shell fundamentals                    |
| 12   | Basic Linux Commands                | Practice essential commands                 |
| 13   | Linux Help Commands                 | Learn how to find documentation             |
| 14   | Keyboard Shortcuts                  | Improve command-line productivity           |
| 15   | Provisioning vs Configuration       | Understand system management concepts       |
| 16   | Virtualization Concepts             | Learn virtualization fundamentals           |
| 17   | Final Reflection                    | Reflect on learning progress                |

---

# Introduction

Day 08 focused on building a strong foundation in Information Technology, Linux, Networking, Servers, and Virtualization.

The objective was to understand how Linux fits into modern IT environments and prepare for future RHCSA and Linux Administration studies.

---

# Learning Objectives

By completing Day 08, I learned about:

* Linux fundamentals
* Networking basics
* Server concepts
* Data centers and cloud computing
* Linux history and distributions
* Virtualization technologies
* Linux shell usage
* System administration concepts

---

# Task 1 - Student Introduction & Goal Setting

## Objective

Define personal learning goals and career aspirations.

### Personal Introduction

**Name:** Mehak Ubed

### Why I Joined Linux Training

I joined Linux training to build practical Linux administration skills and prepare for a career in IT, DevOps, and Cloud Computing.

### Career Goal

To become a skilled Linux System Administrator and continue developing expertise in DevOps and Cloud technologies.

### Learning Expectations

Over the next several weeks, I aim to improve my Linux knowledge, command-line skills, troubleshooting abilities, and understanding of enterprise infrastructure.

---

# Task 2 - Understanding the IT Ecosystem

## Linux in the Real World

Linux powers many modern technologies including:

* Web Servers
* Cloud Platforms
* Android Devices
* Supercomputers
* Data Centers
* Companies such as Uber, Google, Amazon, and Netflix

## What is a Linux Distribution?

A Linux Distribution (Distro) is a complete operating system built around the Linux Kernel and bundled with software, tools, and package management systems.

Examples:

* Red Hat Enterprise Linux
* Rocky Linux
* Ubuntu
* Debian
* Fedora

## What is Virtualization?

Virtualization allows multiple virtual machines to run on a single physical server, improving resource utilization and reducing infrastructure costs.

## What is a Server?

A server is a computer designed to provide services, resources, or applications to other computers over a network.

## Why is RHCSA Important?

RHCSA validates Linux administration skills and is recognized worldwide as a valuable certification for Linux professionals.

---

# Task 3 - Home Network Exploration

## Concepts Learned

### LAN

A Local Area Network (LAN) connects devices within a limited geographical area such as a home or office.

### Gateway

A gateway acts as the connection point between a local network and external networks such as the Internet.

### Public IP vs Private IP

| Public IP               | Private IP                 |
| ----------------------- | -------------------------- |
| Visible on the Internet | Used inside local networks |
| Assigned by ISP         | Assigned by router         |
| Globally unique         | Reusable across networks   |

---

# Task 4 - Router Functions

## DHCP

Automatically assigns IP addresses to devices.

## DNS

Translates domain names into IP addresses.

## NAT

Allows multiple private devices to share a single public IP address.

## Firewall

Protects the network from unauthorized access.

## Port Forwarding

Directs incoming traffic to a specific internal device.

---

# Task 5 - Data Center and Server Concepts

## What is a Server?

A server provides services to users and applications over a network.

## Common Server Services

* Web Hosting
* File Sharing
* Database Hosting
* Email Services
* DNS Services

## What is a Data Center?

A data center is a facility that houses servers, networking equipment, storage systems, and supporting infrastructure.

## AWS and Azure

AWS and Azure provide cloud-based data center services that organizations use instead of building their own infrastructure.

---

# Task 6 - Server vs Laptop Comparison

| Server                         | Laptop                  |
| ------------------------------ | ----------------------- |
| Built for continuous operation | Built for personal use  |
| High reliability               | Portable                |
| Enterprise hardware            | Consumer hardware       |
| Supports many users            | Usually serves one user |

---

# Task 7 - Server Hardware Identification

## Components Studied

* CPU
* RAM
* Disk Storage
* RAID
* NIC
* GPU
* iDRAC

## Why is RAID Important?

RAID improves data protection, fault tolerance, performance, and storage reliability.

---

# Task 8 - Understanding the Linux Boot Process

## Boot Sequence

1. BIOS
2. POST
3. Boot Loader
4. Linux Kernel
5. Operating System

### GRUB

GRUB is the boot loader commonly used by Linux systems to load the operating system.

---

# Task 9 - Linux History

## Important Terms

### UNIX

The operating system that inspired Linux.

### Linus Torvalds

Creator of the Linux Kernel.

### GNU Project

A project focused on creating free software tools and utilities.

### Linux Kernel

The core component that manages hardware and system resources.

## Why Was Linux Revolutionary?

Linux provided a free and open-source alternative to proprietary operating systems.

## Why Was Rewriting UNIX in C Important?

Using C made UNIX portable across different hardware platforms.

---

# Task 10 - Linux Distribution Research

## Common Linux Distributions

* Red Hat Enterprise Linux
* Rocky Linux
* Ubuntu
* Debian
* Fedora
* SUSE

### Lightweight Distribution

Among these distributions, Debian is generally considered one of the lighter options in terms of resource usage.

---

# Task 11 - Linux Shell Exploration

## Commands Practiced

```bash
cat /etc/shells
echo $SHELL
ps $$
date
whereis date
```

## What is a Shell?

A shell is a command-line interface that allows users to communicate with the operating system.

## What Shell Am I Using?

Typically:

```bash
/bin/bash
```

## What Does ps $$ Display?

It displays information about the current shell process.

---

# Task 12 - Basic Linux Commands

## Commands Practiced

```bash
uname -a
uname -r
lscpu
free -m
df -h
ip a
pwd
```

### Purpose

These commands display:

* Kernel information
* CPU details
* Memory usage
* Disk usage
* Network information
* Current directory

---

# Task 13 - Linux Help Commands

## Commands

```bash
uptime --help
man date
```

## What Does man Do?

The `man` command displays detailed documentation for Linux commands.

## Why Are Help Systems Important?

They provide built-in guidance and help users learn commands independently.

---

# Task 14 - Keyboard Shortcut Practice

| Shortcut | Function              |
| -------- | --------------------- |
| Ctrl + C | Interrupt process     |
| Ctrl + D | Exit shell            |
| Ctrl + L | Clear screen          |
| Ctrl + U | Clear line            |
| Ctrl + Z | Suspend process       |
| Tab      | Auto-complete command |

---

# Task 15 - Provisioning vs Configuration

## What is Provisioning?

Provisioning is the process of creating or deploying infrastructure resources.

### Example

Creating a new virtual machine.

## What is Configuration?

Configuration is the process of customizing or managing a system after it has been created.

### Example

Installing software and configuring services.

## Reboot vs Shutdown vs Poweroff

| Command  | Purpose                    |
| -------- | -------------------------- |
| Reboot   | Restart system             |
| Shutdown | Safely stop system         |
| Poweroff | Turn off system completely |

---

# Task 16 - Virtualization Concepts

## What is Virtualization?

Virtualization allows multiple operating systems to run on a single physical machine.

## Why Do Companies Use Virtualization?

* Reduce hardware costs
* Improve efficiency
* Simplify management
* Increase scalability

## Type 1 vs Type 2 Hypervisors

| Type 1                    | Type 2                        |
| ------------------------- | ----------------------------- |
| Runs directly on hardware | Runs on host operating system |
| Better performance        | Easier for beginners          |

## Why Use VirtualBox?

VirtualBox provides a simple platform for creating and managing virtual machines.

## Why Use Rocky Linux or Red Hat?

They are enterprise-focused Linux distributions widely used in production environments.

---

# Task 17 - Final Reflection

During Module 01, I gained a better understanding of Linux, networking, servers, virtualization, and system administration concepts.

The most interesting topics were virtualization and Linux history because they helped me understand how modern infrastructure operates.

The most challenging topic was networking because of the many concepts involved, including IP addressing, gateways, and routing.

Moving forward, I want to continue improving my Linux command-line skills, troubleshooting abilities, and system administration knowledge.

---

# Skills Learned

* Linux Fundamentals
* Networking Basics
* Server Concepts
* Linux Administration
* Virtualization
* Shell Usage
* Command-Line Operations
* IT Infrastructure Concepts

---

# Final Summary

Day 08 provided a strong foundation in Linux and Information Technology concepts.

Understanding servers, networking, virtualization, Linux history, and system administration principles will support future learning throughout the NIT Academy Linux and DevOps journey.

---

# Author

**Mehak Ubed**
NIT Academy – Linux, DevOps & SRE Learning Journey 🚀
