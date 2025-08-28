# Overview

We will first set up all essential tools for the course:

1. **Discord** - Communication
2. **GitHub** - Version Control  
3. **VS Code** - Code Editor

<!-- Commented out for now:
4. **Python** - Programming Language
5. **Raspberry Pi Pico Extension** - Hardware
6. **AI Tools** - Development Assistance
-->

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

**ACM Discord Server:**

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
[VS Code Team Tutorial](https://www.youtube.com/watch?v=B-s71n0dHUk)

- Official tutorial from VS Code team
- Beginner-friendly
- Highly efficient for learning

## Opening the Integrated Terminal

Once VS Code is installed, you can access the terminal:

- **Windows/Linux:** `Ctrl + `` (backtick)
- **macOS:** `Cmd + `` (backtick)
- **Menu:** View → Terminal

This integrated terminal will be used for all command-line operations in the following sections.

## Set up your SSH Keys

SSH keys provide secure authentication for Git operations and server access. **Use VS Code's integrated terminal for all these commands.**

## Generate the SSH Key Pair:

1. **Open VS Code's integrated terminal** (`Ctrl/Cmd + `` backtick)
2. **Run the SSH key generation command:**

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

- Press Enter to accept the default file location
- Enter a passphrase when prompted (optional but recommended)

## Add the Public Key to GitHub:

1. **Copy your public key from VS Code's terminal:**
   ```bash
   # macOS/Linux:
   cat ~/.ssh/id_rsa.pub
   
   # Windows (Git Bash or PowerShell):
   cat ~/.ssh/id_rsa.pub
   ```

2. **Add to GitHub:**
   - Go to GitHub Settings → SSH and GPG keys
   - Click "New SSH key"
   - Paste your public key
   - Give it a descriptive title (e.g., "My Development Machine")

3. **Test the connection from VS Code's terminal:**
   ```bash
   ssh -T git@github.com
   ```
   
   You should see a message like: "Hi username! You've successfully authenticated..."

<!--
# 4. Python Installation

## Installation Requirements

Different methods for different operating systems!

**Helpful Resource:**  
[Real Python Installation Guide](https://realpython.com/installing-python/)

**Choose your OS:**

- Windows, macOS, or Linux guides available
- **Use the Official Installer method**

## Installation Tips

**Unsure about your OS?**

- Don't hesitate to ask!
- Department laptops generally use **Linux**

**Installation Options:**

- Default options are usually fine
- Ask questions if you're unsure!

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