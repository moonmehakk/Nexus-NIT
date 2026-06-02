# Day 17 - GitHub Repositories & Git Workflow

**Name:** Mehak Ubed

> 25th May, 2026

---

## Overview

Today we learned how to:

* Create and manage GitHub repositories
* Understand Local and Remote Repositories
* Fork repositories on GitHub
* Configure Git username and email
* Initialize a Git repository
* Stage, commit, and push code
* Generate and configure SSH keys
* Connect a local machine to GitHub securely

---

## Topics Covered

### 1. GitHub Basics

Learned:

* What GitHub is
* Why developers use GitHub
* Importance of Remote Repositories
* Benefits of collaboration using GitHub

---

### 2. Forking a Repository

Learned how to:

* Fork an existing repository
* Create a personal copy of a project
* Practice safely without affecting the original repository

---

### 3. Creating a Remote Repository

Learned how to:

* Create a new repository on GitHub
* Configure repository settings
* Understand the difference between Local and Remote Repositories

---

### 4. Git Configuration

Commands practiced:

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

### 5. Git Repository Initialization

Commands practiced:

```bash
git init
git status
```

---

### 6. Staging and Committing Files

Commands practiced:

```bash
git add .
git commit -m "Initial Commit"
```

---

### 7. SSH Key Configuration

Commands practiced:

```bash
ssh-keygen -t rsa -b 4096 -C "your@email.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
```

Learned how to:

* Generate SSH keys
* Add SSH keys to GitHub
* Authenticate securely with GitHub

---

### 8. Connecting Local Repository to GitHub

Command practiced:

```bash
git remote add origin git@github.com:username/repository.git
```

---

### 9. Pushing Code to GitHub

Commands practiced:

```bash
git push -u origin main
```

Learned how to:

* Upload code to GitHub
* Verify uploaded files
* Track project changes professionally

---

## Key Git Commands

```bash
git status
git add .
git commit -m "message"
git push
```

---

## Final Reflection

Today I learned how Git and GitHub work together to manage source code. I practiced creating repositories, configuring Git, generating SSH keys, committing changes, and pushing files to GitHub. Understanding the difference between Local and Remote Repositories was one of the most important concepts learned today.

---