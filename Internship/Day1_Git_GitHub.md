# Day 1 - Git & GitHub

## 1. Development Environment Setup & VS Code Basics
Before we dive into coding, we need to set up our development tools.

### Installation
Please refer to the installation PPT for details:
* 📥 [Installation.pptx](https://github.com/user-attachments/files/21192967/Installation.pptx)

Ensure the following tools are installed:
1. **VS Code:** The primary editor we will use.
2. **Git:** The version control system.
3. **Postman:** For testing API requests.

---

## 2. Command Line Interface (CLI) Basics

### What is a Terminal?
A **terminal** (or command-line interface, CLI) is a text-based interface that allows users to interact with the operating system using commands instead of graphical user interfaces (GUIs). It's especially useful for developers.

> In Windows, the terminal is commonly accessed via **Command Prompt** or **Windows Terminal** (recommended).

### Important CLI Commands (Windows)

| Command | Description |
|--------|-------------|
| `cd` | Change directory |
| `dir` | List files and folders in the current directory (Windows alternative to `ls`) |
| `cls` | Clear the terminal screen |
| `echo` | Print a message |
| `mkdir` | Make a new directory |
| `rmdir` or `del` | Remove a directory or file |
| `exit` | Exit the terminal |

#### Examples:
```bash
cd Documents        # Go to the Documents folder
mkdir projects      # Create a folder named 'projects'
cd projects         # Navigate into 'projects'
echo Hello World!   # Print Hello World!
cls                 # Clear the screen
```

> Note: On Linux/macOS, `ls` is used instead of `dir`, and `clear` instead of `cls`.

---

## 3. Git & GitHub Basics

### What is Git?
**Git** is a free and open-source **version control system**. It helps developers track changes in code, collaborate with others, and roll back to previous versions if needed.

Git lets you:
* Track the history of changes in files.
* Work on new features in **branches**.
* Merge changes safely with others.
* Collaborate via platforms like **GitHub**, **GitLab**, etc.

<div style="text-align: center;">
  <img src="https://github.com/so-sc/HackHarbor-3.0/blob/main/Tech/assets/Git_workflow.jpg" alt="Git Workflow" width="500">
</div>

---

### Getting Started with Git
Before using Git, configure your identity in your terminal:
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

---

### Setting Up Authentication (SSH Setup)
It's recommended to use **SSH instead of HTTPS**, as it avoids repeated login prompts and simplifies authentication.

* 📘 [Setting up Git (The Odin Project)](https://www.theodinproject.com/lessons/foundations-setting-up-git)
* 🎥 [Video Guide](https://youtu.be/snCP3c7wXw0?si=Bw8ulNhQBEVxC2yc)

#### Step 1: Generate an SSH Key (Git Bash or Terminal)
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```
* Press **Enter** to accept the default file location.
* Press **Enter** again to skip setting a passphrase.

#### Step 2: Start the SSH Agent and Add Your Key
* **In Git Bash:**
  ```bash
  eval "$(ssh-agent -s)"
  ssh-add ~/.ssh/id_ed25519
  ```
* **In PowerShell (Run as Administrator the first time):**
  ```powershell
  Set-Service ssh-agent -StartupType Automatic
  Start-Service ssh-agent
  ssh-add $env:USERPROFILE\.ssh\id_ed25519
  ```

#### Step 3: Add the SSH key to GitHub
1. Display your public key:
   ```bash
   cat ~/.ssh/id_ed25519.pub
   ```
2. Copy the entire output.
3. Go to [https://github.com/settings/keys](https://github.com/settings/keys)
4. Click **"New SSH key"**, paste the key, and give it a descriptive title (e.g., *"Windows laptop"*).

---

### Initialize Git in Your Project
Navigate to your project folder and run:
```bash
cd your-project-folder
git init
```
This creates a `.git` directory that allows Git to track changes in your project.

### Git Basic Commands Reference

| Command                       | Description                                      |
| ----------------------------- | ------------------------------------------------ |
| `git init`                    | Initializes a new Git repository                 |
| `git status`                  | Shows current changes (staged/unstaged)          |
| `git add <file>`              | Stages a file for commit                         |
| `git commit -m "message"`     | Saves staged changes with a message              |
| `git log`                     | Shows commit history                             |
| `git remote add origin <url>` | Links your local repo to a remote (like GitHub)  |
| `git push -u origin main`     | Pushes commits to the remote repo                |
| `git pull`                    | Gets latest changes from the remote repo         |
| `git clone <url>`             | Copies a remote repository to your local machine |

#### Example Git Workflow:
```bash
git init
git add index.html
git commit -m "Add homepage"
git remote add origin https://github.com/username/repo.git
git push -u origin main
```

---

## 4. Hands-on Follow-Along Task

### Goal: Initialize and Push Your First Git Repository
1. Open Windows Terminal and go to your desktop:
   ```bash
   cd Desktop
   ```
2. Create a new folder and move into it:
   ```bash
   mkdir my-first-git-project
   cd my-first-git-project
   ```
3. Create a sample file:
   ```bash
   echo Hello Git! > readme.txt
   ```
4. Initialize Git:
   ```bash
   git init
   ```
5. Add and commit the file:
   ```bash
   git add readme.txt
   git commit -m "Initial commit with readme"
   ```
6. Create a repository on GitHub (without README, gitignore, or license), link it and push:
   ```bash
   git remote add origin https://github.com/yourusername/my-first-git-project.git
   git branch -M main
   git push -u origin main
   ```
