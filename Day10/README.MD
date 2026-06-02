# Linux Practice Lab – Users, Directories & Files

## Hands-On Linux Filesystem Practice

> Day 10: Monday 18th May, 2026

---

# Table of Contents

| Task | Title                                                                                              |
| ---- | -------------------------------------------------------------------------------------------------- |
| 1    | [Verify Current Logged-in User](#task-1---verify-current-logged-in-user)                           |
| 2    | [Navigate to the /home Directory](#task-2---navigate-to-the-home-directory)                        |
| 3    | [List the Contents of /home](#task-3---list-the-contents-of-home)                                  |
| 4    | [Create Two Users](#task-4---create-two-users)                                                     |
| 5    | [Navigate to Alice's Home Directory](#task-5---navigate-to-alices-home-directory)                  |
| 6    | [Check the Contents of Alice's Directory](#task-6---check-the-contents-of-alices-directory)        |
| 7    | [Create Multiple Directories Using mkdir -p](#task-7---create-multiple-directories-using-mkdir--p) |
| 8    | [Navigate to the projects Directory](#task-8---navigate-to-the-projects-directory)                 |
| 9    | [Create a File](#task-9---create-a-file)                                                           |
| 10   | [Move One Level Up](#task-10---move-one-level-up)                                                  |
| 11   | [List the Contents Again](#task-11---list-the-contents-again)                                      |
| 12   | [Navigate to the images Directory](#task-12---navigate-to-the-images-directory)                    |
| 13   | [Create an Image File](#task-13---create-an-image-file)                                            |
| 14   | [Return to Your Home Directory](#task-14---return-to-your-home-directory)                          |
| 15   | [Verify Your User and Current Directory](#task-15---verify-your-user-and-current-directory)        |
| 16   | [Install the tree Package](#task-16---install-the-tree-package)                                    |
| 17   | [Install tree Again](#task-17---install-tree-again)                                                |
| 18   | [Display the Linux Directory Hierarchy](#task-18---display-the-linux-directory-hierarchy)          |
| 19   | [Final Questions](#task-19---final-questions)                                                      |
| 20   | [Final Reflection](#task-20---final-reflection)                                                    |

---

# Introduction

In today's hands-on lab, you will practice:

* Linux user management
* Directory navigation
* Creating files and folders
* Understanding home directories
* Using the `tree` command
* Exploring the Linux filesystem structure

This lab focuses on building confidence with essential Linux commands used daily by Linux Administrators.

---

# Task 1 - Verify Current Logged-in User

## Run

```bash
whoami
```

## Questions

* What username is displayed?
* Are you logged in as root or a normal user?

---

# Task 2 - Navigate to the /home Directory

## Run

```bash
cd /home
```

## Verify Your Current Location

```bash
pwd
```

Expected output:

```bash
/home
```

---

# Task 3 - List the Contents of /home

## Run

```bash
ls -l
```

## Observation

* What do you see?
* Are there any user directories already created?

> NOTE: On a fresh installation there should normally be no regular user directories unless users were already created earlier.

---

# Task 4 - Create Two Users

## Run

```bash
useradd student
useradd Alice
```

## Verify the Users Were Created

```bash
ls -l /home
```

Expected output should now include:

```bash
student
Alice
```

---

# Task 5 - Navigate to Alice's Home Directory

## Run

```bash
cd /home/Alice
```

## Verify Your Current Location

```bash
pwd
```

Expected output:

```bash
/home/Alice
```

---

# Task 6 - Check the Contents of Alice's Directory

## Run

```bash
ls -l
```

## Observation

* What do you see?
* There should be nothing inside Alice's home directory initially.

---

# Task 7 - Create Multiple Directories Using mkdir -p

## Run

```bash
mkdir -p projects docs images
```

## Verify the Directories

```bash
ls -l
```

Expected directories:

* projects
* docs
* images

---

# Task 8 - Navigate to the projects Directory

## Run

```bash
cd projects
```

## Verify the Contents

```bash
ls -l
```

OR

```bash
ll
```

## Observation

* Is the directory empty?

---

# Task 9 - Create a File

## Run

```bash
touch report.txt
```

## Verify the File Was Created

```bash
ls -l
```

Expected output should include:

```bash
report.txt
```

---

# Task 10 - Move One Level Up

## Run

```bash
cd ..
```

## Verify Your Current Location

```bash
pwd
```

Expected output:

```bash
/ home/Alice
```

---

# Task 11 - List the Contents Again

## Run

```bash
ls -l
```

## Observation

You should now see:

* projects
* docs
* images

---

# Task 12 - Navigate to the images Directory

## Run

```bash
cd images
```

## Verify the Directory Contents

```bash
ls -l
```

## Observation

* Is the images directory empty?

---

# Task 13 - Create an Image File

## Run

```bash
touch logo.png
```

## Verify the File

```bash
ls -l
```

Expected output:

```bash
logo.png
```

---

# Task 14 - Return to Your Home Directory

## Run

```bash
cd
```

## Questions

* Do you see the tilde symbol `~`?
* The tilde `~` means you are inside your home directory.

---

# Task 15 - Verify Your User and Current Directory

## Run

```bash
whoami
pwd
```

## Questions

* Which user are you logged in as?
* Which home directory are you currently inside?

---

# Task 16 - Install the tree Package

## Run

```bash
dnf install -y tree
```

## Important Practice

During installation press:

```bash
Ctrl + C
```

## Observation

* What happened?
* The installation should stop or interrupt.

---

# Task 17 - Install tree Again

## Run

```bash
dnf install -y tree
```

## This Time

Allow the installation to complete successfully.

---

# Task 18 - Display the Linux Directory Hierarchy

## Run

```bash
tree -d /home
```

## Observation

Can you identify:

* Alice
* projects
* docs
* images

---

# Task 19 - Final Questions

1. What does `whoami` do?
2. What does `pwd` display?
3. What does `cd ..` mean?
4. What does `cd` by itself do?
5. What is the purpose of `touch`?
6. Why is `tree` useful?
7. What does the tilde `~` represent?
8. What does `mkdir -p` do?

---

# Task 20 - Final Reflection

## Instructions

Write a short paragraph explaining:

* What you learned from this lab
* Which command was most useful
* Which command was difficult
* Why Linux filesystem navigation is important

---

# Final Summary

Today you practiced:

* Linux user management
* Directory navigation
* File creation
* Directory creation
* Home directory structure
* The `tree` command
* Basic filesystem visualization

These are fundamental Linux administration skills that every RHCSA and Linux Administrator must master.
