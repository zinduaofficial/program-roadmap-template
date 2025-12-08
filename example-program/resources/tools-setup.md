# Development Tools Setup

> **Program:** Software Engineering Program

This guide will help you set up your development environment for the Software Engineering Program. Follow these instructions carefully to ensure you have all necessary tools installed and configured.

## Overview

You'll need to install several tools and configure your development environment. This process typically takes 1-2 hours. Complete this setup **before** the program starts.

## Table of Contents

1. [Operating System Setup](#operating-system-setup)
2. [Python Installation](#python-installation)
3. [Code Editor (VS Code)](#code-editor-vs-code)
4. [Git and GitHub](#git-and-github)
5. [Node.js and npm](#nodejs-and-npm)
6. [Database Tools](#database-tools)
7. [Additional Tools](#additional-tools)
8. [Verification](#verification)
9. [Troubleshooting](#troubleshooting)

## Operating System Setup

### Windows Users

**Install Windows Terminal (Recommended):**
1. Open Microsoft Store
2. Search for "Windows Terminal"
3. Click Install

**Enable Windows Subsystem for Linux (WSL) - Optional but Recommended:**
```powershell
wsl --install
```

### macOS Users

**Install Homebrew (Package Manager):**
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

**Install Xcode Command Line Tools:**
```bash
xcode-select --install
```

### Linux Users

Ensure your system is up to date:
```bash
sudo apt update && sudo apt upgrade -y
```

## Python Installation

### Version Required: Python 3.10 or later

#### Windows
1. Download Python from [python.org](https://www.python.org/downloads/)
2. Run the installer
3. **Important:** Check "Add Python to PATH"
4. Click "Install Now"

#### macOS
```bash
brew install python@3.11
```

#### Linux (Ubuntu/Debian)
```bash
sudo apt install python3.11 python3.11-venv python3-pip
```

### Verify Installation
```bash
python --version
# or
python3 --version
```
Should show Python 3.10 or later.

## Code Editor (VS Code)

### Installation

Download and install from [code.visualstudio.com](https://code.visualstudio.com/)

### Essential Extensions

Install these extensions in VS Code:

1. **Python** (Microsoft)
   - Syntax highlighting, debugging, IntelliSense
   
2. **Pylance** (Microsoft)
   - Enhanced Python language support
   
3. **GitLens** (GitKraken)
   - Advanced Git integration
   
4. **Prettier** (Prettier)
   - Code formatter
   
5. **Live Server** (Ritwick Dey)
   - Local development server for web projects
   
6. **ESLint** (Microsoft)
   - JavaScript linting

7. **Thunder Client** (Thunder Client)
   - API testing tool

### VS Code Configuration

Create a settings.json with these recommended settings:
```json
{
  "editor.formatOnSave": true,
  "editor.tabSize": 4,
  "python.linting.enabled": true,
  "python.linting.pylintEnabled": true,
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 1000
}
```

## Git and GitHub

### Install Git

#### Windows
Download from [git-scm.com](https://git-scm.com/download/win)

#### macOS
```bash
brew install git
```

#### Linux
```bash
sudo apt install git
```

### Configure Git

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Set Up GitHub Account

1. Create account at [github.com](https://github.com)
2. Set up SSH keys (recommended):

```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "your.email@example.com"

# Start ssh-agent
eval "$(ssh-agent -s)"

# Add SSH key
ssh-add ~/.ssh/id_ed25519

# Copy public key (macOS/Linux)
cat ~/.ssh/id_ed25519.pub
# Copy this output and add to GitHub Settings > SSH Keys
```

### Verify Git Installation
```bash
git --version
```

## Node.js and npm

### Version Required: Node.js 18 LTS or later

#### Windows
Download from [nodejs.org](https://nodejs.org/) (LTS version)

#### macOS
```bash
brew install node@18
```

#### Linux
```bash
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs
```

### Verify Installation
```bash
node --version
npm --version
```

## Database Tools

### PostgreSQL

#### Windows
Download installer from [postgresql.org](https://www.postgresql.org/download/windows/)

#### macOS
```bash
brew install postgresql@15
brew services start postgresql@15
```

#### Linux
```bash
sudo apt install postgresql postgresql-contrib
sudo systemctl start postgresql
```

### Database GUI (Optional)

**pgAdmin** - PostgreSQL management tool
- Download from [pgadmin.org](https://www.pgadmin.org/)

**DBeaver** - Universal database tool
- Download from [dbeaver.io](https://dbeaver.io/)

## Additional Tools

### Postman or Insomnia

For API testing and development:
- **Postman:** [postman.com](https://www.postman.com/downloads/)
- **Insomnia:** [insomnia.rest](https://insomnia.rest/download)

### Docker (Optional - needed in later courses)

- Download from [docker.com](https://www.docker.com/get-started)
- Windows: Docker Desktop
- macOS: Docker Desktop
- Linux: Docker Engine

### Browser DevTools

Install these browsers with developer tools:
- **Chrome** or **Chromium** (recommended)
- **Firefox Developer Edition** (alternative)

Install browser extensions:
- React Developer Tools
- Redux DevTools (later in program)

## Verification

After installation, verify all tools:

```bash
# Python
python --version

# Git
git --version

# Node.js
node --version
npm --version

# PostgreSQL
psql --version
```

### Test Your Setup

Create a test project:

```bash
# Create directory
mkdir test-setup
cd test-setup

# Test Python
python -c "print('Python works!')"

# Test Git
git init
git status

# Test Node
npm init -y
node -e "console.log('Node works!')"

# Test Python virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install requests
python -c "import requests; print('Python packages work!')"
deactivate
```

## Troubleshooting

### Python not found

**Issue:** Command not found or wrong version

**Solution:**
- Ensure Python is added to PATH
- Try `python3` instead of `python`
- Restart terminal/computer after installation

### Git permission errors

**Issue:** Permission denied when using Git

**Solution:**
- Check SSH key setup
- Verify GitHub account connection: `ssh -T git@github.com`
- Use HTTPS instead of SSH temporarily

### npm permissions errors

**Issue:** Permission denied when installing packages

**Solution (macOS/Linux):**
```bash
sudo chown -R $(whoami) ~/.npm
sudo chown -R $(whoami) /usr/local/lib/node_modules
```

### PostgreSQL connection issues

**Issue:** Can't connect to PostgreSQL

**Solution:**
- Verify PostgreSQL is running
- Check port 5432 is not blocked
- Verify password and username
- Try: `sudo systemctl status postgresql` (Linux)

### VS Code Python extension issues

**Issue:** Python not detected in VS Code

**Solution:**
1. Open Command Palette (Ctrl+Shift+P / Cmd+Shift+P)
2. Type "Python: Select Interpreter"
3. Choose your Python installation

## Getting Help

If you encounter issues:

1. **Search the error message** - Most setup issues have been solved before
2. **Check program Slack/Discord** - Ask fellow students or instructors
3. **Post in troubleshooting channel** - Include:
   - Operating system and version
   - Complete error message
   - What you've already tried
4. **Schedule office hours** - For persistent issues

## Pre-Program Checklist

Before the program starts, verify:

- [ ] Python 3.10+ installed and verified
- [ ] VS Code installed with all essential extensions
- [ ] Git installed and configured
- [ ] GitHub account created and SSH keys set up
- [ ] Node.js and npm installed
- [ ] PostgreSQL installed
- [ ] Created and tested a virtual environment
- [ ] Postman or Insomnia installed
- [ ] Browser with DevTools installed
- [ ] All tools verified with test commands

## Optional Setup

### Terminal Customization

Make your terminal more productive:

**Oh My Zsh (macOS/Linux):**
```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

**PowerShell Customization (Windows):**
- Install Windows Terminal
- Customize with [Oh My Posh](https://ohmyposh.dev/)

### Productivity Tools

- **Notion** or **Obsidian** - Note-taking
- **Todoist** or **Trello** - Task management
- **Pomodoro Timer** - Time management
- **f.lux** or **Night Shift** - Reduce eye strain

## Resources

- [Python Documentation](https://docs.python.org/3/)
- [Git Documentation](https://git-scm.com/doc)
- [VS Code Documentation](https://code.visualstudio.com/docs)
- [Node.js Documentation](https://nodejs.org/docs/)
- [PostgreSQL Documentation](https://www.postgresql.org/docs/)

---

**Last Updated:** December 2025

**Questions?** Post in the #tech-setup channel or email support@zinduaschool.com
