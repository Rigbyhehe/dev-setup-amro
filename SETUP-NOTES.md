# Development Environment Setup

This file documents the tools, settings, extensions, and commands used to configure my development environment.

## Tools and Technologies

- Visual Studio Code – Code editor
- Git – Version control system
- WSL 2 – Runs Linux on Windows
- Ubuntu 24.04 – Linux distribution
- Python 3.11 – Programming language
- uv – Python version and environment manager

## Installation and Verification

### 1. VS Code

VS Code was already installed and configured with the required extensions and workspace settings.

### 2. Git

Git for Windows was installed using the official Windows installer.

Git was installed inside Ubuntu using:

```
sudo apt install git
```

Installation was verified on Windows and Ubuntu using:

```
git --version
```

### 3. WSL 2 and Ubuntu 24.04

installed Ubuntu using:

```
wsl --install -d Ubuntu-24.04
```
### 4. Python 3.11 and uv

Ubuntu 24.04 comes with Python 3.12.3 by default. Since the project required Python 3.11, uv was installed to manage Python versions without replacing the system Python.

Python 3.11.18 was installed using uv and its version was verified successfully.

### 5. Virtual Environments

A virtual environment was created using uv to isolate project dependencies from the system Python and other projects.

The environment was activated before installing packages and deactivated when finished.

### 6. VS Code and WSL Integration

The Microsoft WSL extension was installed to connect VS Code with Ubuntu.

The project was opened from the WSL terminal using the code command. The integrated terminal was configured to use Bash instead of PowerShell.

### 7. GitHub Authentication

A public GitHub repository was created and cloned into the Ubuntu environment using HTTPS.

The local repository was connected to the remote GitHub repository through the origin remote.

GitHub authentication was configured using HTTPS with a fine-grained Personal Access Token (PAT).

Git credential caching was enabled to temporarily store credentials in memory.