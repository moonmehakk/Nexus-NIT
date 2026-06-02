# Practice Lab – Understanding Linux Inodes

> NIT Academy Linux Practice Lab
> Date: 21st May, 2026 - Day 13

## Objective

Understand Linux inodes, metadata, directory structures, and filesystem inode management through practical exercises.

---

# Task 1 - Understanding Inodes

## What is an Inode?

An inode is a special data structure in Linux that stores metadata about a file or directory.

### Inode Stores:

* File permissions
* Owner information
* Group information
* File size
* Timestamps
* Data block locations

### Inode Does Not Store:

* Filename

The filename is stored inside the directory entry and points to the inode number.

### Example

```text
report.txt → inode 3470012
```

Linux reads the inode to locate the file metadata and actual data blocks.

---

# Task 2 - Check Inode Numbers

Run:

```bash
ls -li /var
```

### Observation

Notice that each file and directory has a unique inode number displayed in the first column.

### Questions

1. What is an inode number?
2. Why does each file have a different inode?

---

# Task 3 - View Directory Metadata

Run:

```bash
ls -ld /
```

### Observation

This command displays metadata about the root directory itself rather than its contents.

### Questions

1. What information is displayed?
2. What does the directory size represent?

---

# Task 4 - Compare ls Commands

Run:

```bash
ls -l /
ls -ld /
ls -li /
ls -ild /
```

### Learning Points

* `ls -l /` shows contents of `/`
* `ls -ld /` shows metadata of `/`
* `ls -li /` shows inode numbers of contents
* `ls -ild /` shows inode number of root directory itself

### Questions

1. What is the difference between `ls -l` and `ls -ld`?
2. What additional information does `-i` provide?

---

# Task 5 - Check Filesystem Inode Usage

Run:

```bash
df -i
```

### Observation

This command displays:

* Total inodes
* Used inodes
* Free inodes
* Inode usage percentage

### Questions

1. What does inode usage mean?
2. Why are free inodes important?

---

# Task 6 - Understanding Inode Exhaustion

## Scenario

A filesystem may show free disk space:

```bash
df -h
```

Example:

```text
20G Available
```

But file creation fails.

### Root Cause

All available inodes have been consumed.

### Important Concept

A filesystem requires:

* Free disk blocks
* Free inodes

Both resources must be available to create new files.

### Interview Question

Why can `df -h` show free space while users cannot create new files?

**Answer:** Because all inodes are exhausted even though disk blocks are still available.

---

# Task 7 - Create Files and Observe Inodes

Create a practice directory:

```bash
mkdir ~/inode_lab
cd ~/inode_lab
```

Create files:

```bash
touch file1
touch file2
touch file3
```

Check inode numbers:

```bash
ls -li
```

### Observation

Each file receives a unique inode number.

---

# Task 8 - Delete and Recreate Files

Delete a file:

```bash
rm file2
```

Create another file:

```bash
touch newfile
```

Check again:

```bash
ls -li
```

### Observation

Linux may reuse a previously freed inode number.

---

# Task 9 - Explore File Metadata

Run:

```bash
stat /etc/passwd
```

Identify:

* Inode number
* File size
* Permissions
* Owner
* Access time
* Modify time
* Change time

### Questions

1. What information does `stat` provide?
2. How is it different from `ls -l`?

---

# Key Commands Summary

| Command               | Purpose                 |
| --------------------- | ----------------------- |
| `ls -li`              | Show inode numbers      |
| `ls -ld`              | Show directory metadata |
| `df -i`               | Display inode usage     |
| `df -h`               | Display disk usage      |
| `stat file`           | Detailed file metadata  |
| `find / -inum NUMBER` | Search by inode         |

---

# Practice Questions

1. What does an inode store?
2. Does an inode store filenames?
3. What is the difference between `ls -l /` and `ls -ld /`?
4. Why can a system run out of inodes?
5. What command displays inode usage?
6. Why can file creation fail even when free disk space exists?

---

# Final Reflection

Today I learned how Linux filesystems use inodes to store file metadata and how filenames are linked to inode numbers through directory entries. I practiced viewing inode information, checking inode usage, and understanding why filesystems can run out of inodes even when free disk space remains available. Understanding inodes is important for Linux system administration and troubleshooting storage-related issues.
