# Git and GitHub Connection

## 1. Connect Git to GitHub

To use Git with GitHub, first make sure Git is installed on your computer and you have a GitHub account.

### Step 1: Set your Git identity
Run these commands in the terminal:

```bash
git config --global user.name "Your Name"
git config --global user.email "your_email@example.com"
```

This tells Git who you are when you commit changes.

### Step 2: Connect Git to GitHub
You can connect Git to GitHub using either HTTPS or SSH.

#### Option A: HTTPS
This is simple and works well for beginners.

```bash
git clone https://github.com/username/repository.git
```

#### Option B: SSH (recommended)
SSH is more secure and often used for regular development.

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

Then add the generated public key to your GitHub account under Settings > SSH and GPG keys.

### Step 3: Verify the connection
```bash
ssh -T git@github.com
```

If everything is correct, GitHub will confirm that your connection is successful.

---

## 2. How to Clone a Repository Using Git

Cloning means downloading a repository from GitHub to your computer.

### Command
```bash
git clone <repository-url>
```

### Example
```bash
git clone https://github.com/username/repository.git
```

After cloning, you can enter the folder:

```bash
cd repository
```

Now you can view files, edit them, and commit changes.

---

## 3. How to Fork a Git Repository

Forking means making your own copy of someone else’s repository on GitHub.

This is useful when you want to work on a project without changing the original repository directly.

### Steps to fork a repository
1. Open the repository on GitHub.
2. Click the Fork button.
3. Choose your GitHub account as the destination.
4. GitHub will create your own copy of the project.

### Clone your fork to your computer
```bash
git clone https://github.com/your-username/repository.git
```

### Add the original repository as upstream
This helps you keep your fork updated with the original project.

```bash
git remote add upstream https://github.com/original-owner/repository.git
```

---

## 4. Common GitHub Commands

```bash
git push
```
Uploads your local commits to GitHub.

```bash
git fetch
```
Downloads changes from the remote repository without merging them.

```bash
git merge
```
Combines changes from one branch into another.

```bash
git pull
```
This does both fetch and merge together.

---

## Summary

- Connect Git to GitHub by setting your name and email.
- Use git clone to download a repository from GitHub.
- Use Fork to create your own copy of someone else’s project.
- Use git push, git pull, git fetch, and git merge to manage your work online.
