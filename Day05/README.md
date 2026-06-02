# Welcome to NIT Academy - Day 05

> **Student:** Mehak Ubed  
> **Day-05:** Wednesday 13th May, 2026

---

# Table of Contents

| Task | Title | Summary |
|------|------|------|
| 1 | Installation for Windows | Install Visual Studio Code on Windows |
| 2 | Installation for Chromebook | Install Visual Studio Code on Chromebook |
| 3 | Installation for Mac | Install Visual Studio Code on macOS |

---

# Introduction

Visual Studio Code (VS Code) is one of the most popular code editors used by developers, Linux administrators, DevOps engineers, and cloud professionals.

For Day 05, the objective was to install Visual Studio Code based on the operating system being used.

---

# Learning Objectives

By completing Day 05, I learned how to:

- Download Visual Studio Code
- Install VS Code on my operating system
- Launch VS Code successfully
- Prepare my development environment
- Understand the importance of a modern code editor

---

# Task 1 - Installation for Windows

## Objective

Install Visual Studio Code on a Windows system.

### Step 1 - Open the VS Code Website

Visit:

```text
https://code.visualstudio.com/
```

### Step 2 - Download VS Code

Click:

```text
Download for Windows
```

This downloads the Windows installer (.exe file).

### Step 3 - Install VS Code

Installation Steps:

1. Open downloaded installer
2. Click Next
3. Accept License Agreement
4. Continue through setup
5. Click Install

### Recommended Installation Options

- Add VS Code to PATH
- Create Desktop Icon

### Step 4 - Launch VS Code

Open from:

```text
Start Menu → Visual Studio Code
```

### Outcome

Successfully installed Visual Studio Code on Windows.

---

# Task 2 - Installation for Chromebook

## Objective

Understand how VS Code can be installed on Chromebook.

### Step 1 - Enable Linux

Navigate to:

```text
Settings → Developer → Linux Development Environment
```

Enable Linux support.

### Step 2 - Open Linux Terminal

Open:

```text
Launcher → Terminal
```

### Step 3 - Install VS Code

Run:

```bash
sudo apt update
sudo apt install wget gpg -y

wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg

sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg

echo "deb [arch=amd64 signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" | sudo tee /etc/apt/sources.list.d/vscode.list

sudo apt update

sudo apt install code -y
```

### Outcome

Successfully installed Visual Studio Code on Chromebook.

---

# Task 3 - Installation for Mac

## Objective

Understand how VS Code can be installed on macOS.

### Step 1 - Download VS Code

Visit:

```text
https://code.visualstudio.com/download
```

Choose:

- Apple Silicon
- Intel Chip

### Step 2 - Extract Download

1. Open Downloads
2. Double-click ZIP file
3. Extract Visual Studio Code

### Step 3 - Move to Applications

Move:

```text
Visual Studio Code.app
```

to:

```text
Applications
```

### Step 4 - Launch VS Code

Open:

```text
Applications → Visual Studio Code
```

If prompted:

```text
Click Open
```

### Outcome

Successfully installed Visual Studio Code on macOS.

---

# Skills Learned

During Day 05, I gained experience in:

- Installing development tools
- Configuring a code editor
- Preparing a Linux/DevOps workspace
- Understanding platform-specific installations

---

# Final Summary

Today I learned how to:

- Download Visual Studio Code
- Install VS Code on Windows, Chromebook, or Mac
- Launch and verify installation
- Prepare a professional development environment

Visual Studio Code is now ready for future Linux, DevOps, Git, and programming tasks.

---

# Author

**Mehak Ubed**  
NIT Academy – Linux, DevOps & SRE Learning Journey 🚀