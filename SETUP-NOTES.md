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

VS Code was downloaded and installed from the official Visual Studio Code website.

### 1.1 Workspace Settings

The following workspace settings were configured in `.vscode/settings.json`:

`files.autoSave: afterDelay`  Automatically saves files after a short delay 
`editor.formatOnSave: true`  Formats files whenever they are saved 
 `editor.renderWhitespace: all` Displays whitespace characters to make formatting easier to inspect

### 1.2 Recommended Extensions

The following extensions were added to `.vscode/extensions.json`:
 Python : Provides Python language support, debugging, and interpreter selection 
 Pylance : Provides code completion, type checking, and error detection 
 GitLens : Provides Git history, commit information, and line blame 

These recommendations allow the same development tools to be suggested when the repository is opened in VS Code.

### 2. Git

Git for Windows was installed using the official Windows installer.

Git was installed inside Ubuntu using:

sudo apt install git

Installation was verified on Windows and Ubuntu using:

git --version

### 3. WSL 2 and Ubuntu 24.04

installed Ubuntu using:

wsl --install -d Ubuntu-24.04

### 4. Python 3.11 and uv

Ubuntu 24.04 comes with Python 3.12.3 by default. Since the project required Python 3.11, uv was installed to manage Python versions without replacing the system Python.

uv was installed using its official installation script:

curl -LsSf https://astral.sh/uv/install.sh | sh


Python 3.11.18 was installed using uv and its version was verified successfully.
The command:
uv python install 3.11

### 5. Virtual Environments

A virtual environment was created using uv to isolate project dependencies from the system Python and other projects.

The environment was activated before installing packages and deactivated when finished.
The commands:
uv venv --python 3.11
source .venv/bin/activate
python -m pip install requests
python -m pip show requests
deactivate

### 6. VS Code and WSL Integration

The Microsoft WSL extension was installed to connect VS Code with Ubuntu.

The project was opened from the WSL terminal using the code command. The integrated terminal was configured to use Bash instead of PowerShell.

### 7. GitHub Authentication

A public GitHub repository was created and cloned into the Ubuntu environment using HTTPS.

The local repository was connected to the remote GitHub repository through the origin remote.

GitHub authentication was configured using HTTPS with a fine-grained Personal Access Token (PAT).

Git credential caching was enabled to temporarily store credentials in memory.