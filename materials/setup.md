# Overview

This guide was in part prepared by Allegheny's ACM student chapter and is designed to set up the essential tools for the course. It includes:

1. **Discord** - Communication
2. **GitHub** - Version Control  
3. **VS Code** - Code Editor (with SSH key setup)
4. **Git Configuration** - Version Control Identity Setup
5. **Python** - Programming Language

# 1. Discord Setup

## Download and Create Account

- Download Discord: [discord.com](https://discord.com/)
- Create your account for **free**
- Use personal or school email
  - **Note**: You'll lose Allegheny email access after graduation
- Make sure your display name is your full name

## Join Discord Servers

**CIS Department Discord:**

- Join here: [discord.gg/tWa2BwXqSp](https://discord.gg/tWa2BwXqSp)
- **Primary course communication channel**

**ACM Discord Server (optional):**

- Join here: [discord.gg/4gm2jumuEd](https://discord.gg/4gm2jumuEd)
- Get notified of events
- **Tip**: Attend 3 ACM events → eligible for membership!

# 2. GitHub Setup

## Create Your Free Account

- Sign up: [github.com/signup](https://github.com/signup)
- **Essential for:**
  - Accessing class repositories
  - Submitting your work for grading
  - Version control

## Set Up Your GitHub Profile

**Complete your profile for better collaboration:**

1. **Add a profile picture**
   - Click on your avatar in the top-right corner
   - Select "Settings"
   - Upload a clear photo of yourself

2. **Add your name and bio**
   - Go to "Public profile" section
   - Add your full name (first and last)
   - Write a brief bio (e.g., "Computer Science student at Allegheny College")

3. **Add your location and email**
   - Location: "Meadville, PA" (or your hometown)
   - Email: Use your preferred contact email

4. **Set up your README**
   - Consider creating a profile README to showcase your work
   - Optional but recommended for building your professional presence

# 3. VS Code Setup

## Download VS Code

**All Platforms:** [code.visualstudio.com/download](https://code.visualstudio.com/download)

**Beginner Setup Guide:**  
For Reference: [VS Code Team Tutorial](https://www.youtube.com/watch?v=B-s71n0dHUk)
- Official tutorial from VS Code team
- Beginner-friendly
- Highly efficient for learning

## Opening the Integrated Terminal

Once VS Code is installed, you can access the terminal:

- **Windows/Linux:** `Ctrl + ` (backtick)`
- **macOS:** `control + ` (backtick)`
- **Menu:** View → Terminal

This integrated terminal will be used for all command-line operations in the following sections.

## Set up your SSH Keys

SSH keys provide secure authentication for Git operations and server access. **Use VS Code's integrated terminal for all these commands.**

## Generate the SSH Key Pair:

1. **Open VS Code's integrated terminal**
2. **Run the SSH key generation command:**

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

- Press Enter to accept the default file location
- Enter a passphrase when prompted (you will need to enter it each time you send your work to GitHub, press Enter twice if you don't want to create passphrase)

## Add the Public Key to GitHub:

1. **Copy your public key from VS Code's terminal:**
   ```bash
   cat ~/.ssh/id_rsa.pub
   ```

2. **Add to GitHub:**
   - Go to GitHub Settings → SSH and GPG keys
   - Click "New SSH key"
   - Paste your public key
   - Give it a descriptive title (e.g., "HP Machine")

3. **Test the connection from VS Code's terminal:**
   ```bash
   ssh -T git@github.com
   ```
   
   You should see a message similar to: "You've successfully authenticated..."

# 4. Git Configuration

## Verify Git is Working

First, let's confirm Git is installed:

```bash
git --version
```

You should see something like `git version 2.x.x`

## Configure Git Identity (Required for Commits)

**Before you can make any commits, Git needs to know who you are:**

```bash
git config --global user.name "Your Full Name"
git config --global user.email "your.email@example.com"
```

**Example:**
```bash
git config --global user.name "Jane Smith"
git config --global user.email "jane.smith@allegheny.edu"
```

**Verify your configuration:**
```bash
git config --global --list
```

You should see your name and email listed.

## Why This Configuration Matters

- **Every commit** includes author information
- **GitHub needs this** to link commits to your profile
- **Required for grading** - we need to identify your work
- **Professional practice** - proper attribution in team projects

**Your Git setup is now complete for making commits!**

# 5. Python Installation

Mac and Linux Users: check if you have the correct version of Python installed already on your machine. 

Open VS Code's integrated terminal and run:
```bash
python3 --version
```

OR 
```bash
python --version
```
**We will be using Python 3.12.** If you have Python 2.x, please install the Python 3 version by following instructions below.

## Installation by Operating System

Choose the instructions for your operating system. Since you already have VS Code installed, we will focus on getting Python set up and working with your editor.

### macOS Installation

**Option 1: Official Python Installer (Recommended)**
1. Go to [python.org/downloads](https://python.org/downloads)
2. Download the latest Python 3.x version for macOS
3. Run the downloaded `.pkg` file
4. Follow the installation wizard (default options are fine)
5. **Important**: Check "Add Python to PATH" if prompted

**Option 2: Using Homebrew (if you have it installed)**
```bash
brew install python
```

**Verify Installation:**
Open VS Code's integrated terminal and run:
```bash
python3 --version
```
You should see something like `Python 3.x.x`

### Windows Installation

**Official Python Installer**
1. Go to [python.org/downloads](https://python.org/downloads)
2. Click "Download Python 3.x.x" (latest version)
3. Run the downloaded `.exe` file
4. **IMPORTANT**: Check "Add Python to PATH" checkbox at the bottom
5. Click "Install Now"
6. If prompted, allow the installer to disable path length limit

**Verify Installation:**
Open VS Code's integrated terminal and run:
```bash
python --version
```
or
```bash
python3 --version
```
You should see something like `Python 3.x.x`

**If Python is not recognized on Windows:**

If you get an error like "'python' is not recognized as an internal or external command", you need to add Python to your PATH:

1. **Find your Python installation path:**
   - Usually located at: `C:\Users\YourUsername\AppData\Local\Programs\Python\Python3X\`
   - Or: `C:\Python3X\`

2. **Add Python to PATH:**
   - Press `Windows + R`, type `sysdm.cpl`, press Enter
   - Click "Environment Variables" button
   - Under "System Variables", find and select "Path", click "Edit"
   - Click "New" and add your Python path (e.g., `C:\Users\YourUsername\AppData\Local\Programs\Python\Python312\`)
   - Also add the Scripts folder: `C:\Users\YourUsername\AppData\Local\Programs\Python\Python312\Scripts\`
   - Click "OK" on all windows
   - **Restart VS Code** and try again

3. **Alternative method using VS Code terminal:**
   ```bash
   # Check if Python is installed but not in PATH
   where python
   # or
   py --version
   ```

### Linux Installation

**Ubuntu/Debian:**
```bash
sudo apt update
sudo apt install python3 python3-pip
```

**Verify Installation:**
Open VS Code's integrated terminal and run:
```bash
python3 --version
```
You should see something like `Python 3.x.x`

<!--
## Test Your Python Installation

Let's make sure Python is working correctly with a simple "Hello World" program.

### Create Your First Python Program

1. **In VS Code, create a new file:**
   - Press `Ctrl+N` (Windows/Linux) or `Cmd+N` (macOS) or go to File -> New File
   - Save it as `hello.py` in a folder of your choice

2. **Copy and paste this code:**
   ```python
   print("Hello, World!")
   print("Python is working correctly!")
   
   # Let's also check the Python version
   import sys
   print(f"You are running Python {sys.version}")
   ```

3. **Run your program:**
   - Open VS Code's integrated terminal
   - Navigate to where you saved `hello.py`
   - Run the program:
     
     **macOS/Linux:**
     ```bash
     python3 hello.py
     ```
     
     **Windows:**
     ```bash
     python hello.py
     ```

4. **Expected output:**
   ```
   Hello, World!
   Python is working correctly!
   You are running Python 3.x.x
   ```

### Troubleshooting

**If you get "command not found" or "not recognized":**
- Make sure Python was added to your system PATH during installation
- Try using `python3` instead of `python` (especially on macOS/Linux)
- Restart VS Code and your terminal

**Still having issues?**
- Ask for help!
- Check if Python is installed: look for Python in your Applications (macOS) or Programs (Windows)
-->

<!--
# 5. Raspberry Pi Pico Extension

## Installing the Extension

1. **Open VS Code**
2. **Go to Extensions Marketplace**
3. **Search:** "Raspberry Pi Pico"
4. **Install** with a simple click!

## Important Note

**Ensure** the extension is published by **Raspberry Pi**

- Look for the official publisher name
- Avoid unofficial extensions
  

# 6. AI Tools Setup

## Overview

Essential AI tools for enhanced coding experience:

- GitHub Copilot
- GPT-4.1 & Premium Models
- Gemini CLI
- OpenCode CLI
- VS Code Integration

## 6a. GitHub Copilot

**Enable GitHub Copilot:**

- Go to [github.com/features/copilot](https://github.com/features/copilot)
- Sign up with your GitHub account
- **Students**: Eligible for GitHub Student Developer Pack (includes free Copilot!)

## Install Copilot Extension

1. Open **VS Code**
2. Go to **Extensions**
3. Search **"GitHub Copilot"**
4. Click **Install**
5. Sign into GitHub when prompted

## 6b. GPT-4.1 & Premium Models

**Access Requirements:**

- Log into ChatGPT with GitHub or personal account
- **GPT-4.1**: Unlimited usage under student plan
- **Premium Models**: 300 requests/month
  - Claude Sonnet 3.5
  - GPT-5

**💡 Pro Tip:** CLI uses fewer premium requests than VS Code extension!

## 6c. Gemini CLI

**Google's AI CLI Tool**

Install using npx:

```bash
npx https://github.com/google-gemini/gemini-cli
```

Perfect for AI-powered coding tasks directly from terminal!

## 6d. OpenCode CLI

**AI Coding Agent Tool**

Install and launch:

```bash
npx opencode-ai@latest
```

Another powerful tool for our coding workflow.

## 6e. VS Code AI Integration

**Optional but Recommended**

Install VS Code extensions for better integration:

1. **Gemini CLI**
2. **OpenCode AI**

**VS Code → Extensions → Search for each tool**


# Setup Complete! ✅

## You now have:

- ✅ Discord for communication  
- ✅ GitHub account ready  
- ✅ VS Code configured with SSH keys


- ✅ Python installed  
- ✅ Raspberry Pi Pico extension  
- ✅ AI tools ready

## Questions?

Ready to start coding with our complete development environment!

## Let's begin our coding journey! 🚀
-->
