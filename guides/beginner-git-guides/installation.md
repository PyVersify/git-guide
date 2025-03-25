# Git Installation Guide

Before you can use Git for version control, you will need to setup a GitHub Account and follow the relevant Git installation guide for your specific device.

## Step 1: Creating up a GitHub <samp>(If necessary)</samp> `optional`

> [!NOTE]
> I recommend setting up a GitHub account prior to downloading Git. This is not essential, as Git can be used for local version control as well as version control. However this guide details configuring your Git credentials, which needs to match your GitHub account credentials if your require working from GitHub repositories.
>
> See the [Creating a GitHub Account Guide](../github-guides/creating-a-github-account.md) for details on how to create a Github Account.

## Windows Installation

> [!NOTE]
> This guide will include installing Git Bash terminal to run Git Commands in Bash.

### 1. Download the installer
  - Visit the official Git for Windows website: _[https://git-scm.com/download/win](https://git-scm.com/download/win)_
  - Click on the **"Download"** button to get the latest version.
  - Choose the 64-bit or 32-bit version depending on your system.

### 2. Run the installer
  - Open the downloaded `.exe` file.
  - When prompted with "Do you want to allow this app to make changes to your device?", click **"Yes"**.
  - Click **"Next"** on the welcome screen.

### 3. Select Installation Location
  - Choose the destination folder <samp>(the default is recommended).</samp>
  - Click **"Next"**.

### 4. Select Components
  - The pre-selected settings are generally appropriate.
  - You can select "Additional icons" if you want desktop shortcuts.
  - Click **"Next"**.

### 5. Choose Default Editor
  - Select your preferred text editor to use with Git.
  - Click **"Next"**.

### 6. Adjust PATH Environment
  - Choose one of the following options:
    - "Use Git from Git Bash only." <samp>(Git commands will only work in Git Bash)</samp>
    - "Git from the command line and also from 3rd-party software." <samp>(recommended - allows Git to work in Command Prompt and PowerShell)
  - Click **"Next"**.

### 7. Complete Installation
  - Keep the default settings for the remaining options.
  - Click **"Install"** to begin installation.
  - Check **"Launch Git Bash"** and click **"Finish"** when installation completes.

### 8. Verify Installation
  - In the Git Bash terminal, Command Prompt, or PowerShell, type the following Git command:
    ```bash
    git --version
    ```
  - This will display the installed Git version.

## MacOS Installation <samp>[Homebrew]</samp> `recommended`

### 1. Install Homebrew <samp>(if not already installed)</samp>
  - Open Terminal
  - Run the following command:
      ```bash
      /text/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
      ```
  - Enter your password when prompted.

### 2. Install Git Using Homebrew
  - In Terminal, run:
      ```bash
      brew install git
      ```

### 3. Verify Installation
  - Run:
      ```bash
      git --version
      ```

## Linux Installation

> [!NOTE]
> Git is often pre-installed on many Linux distributions, but not always.

### 1. Determine if Git is pre-installed on your system
  - Open Terminal and run:
      ```bash
      git --version
      ```
  - You will see an error like: `-bash: git: command not found` if Git is not installed on the device already. Otherwise you won't need to worry about the installation <samp>(although I still recommend following step 2)</samp>

### 2. Update Package Index
  - Open Terminal.
  - Run:
    - <samp>Ubuntu/Debian</samp>
        ```bash
        sudo apt update
        ```
    - <samp>Fedora</samp>
        ```bash
        sudo dnf update
        ```

### 3. Install Git
  - For a **complete-install**, run:
    - <samp>For Ubuntu/Debian users:</samp>
        ```bash
        sudo apt install git-all
        ```
    - <samp>For Fedora users:</samp>
        ```bash
        sudo dnf install git-all
        ```
    - <samp> For Arch Linux users:</samp>
        ```bash
        sudo pacman -S git
        ```

### 4. Verify Installation
  - Run:
      ```bash
      git --version
      ```

## Initial Git Configuration

After installing Git, configure your identity:

### 1. Set Your Username
  - Run in your Bash Terminal:
      ```bash
      git config --global user.name "Your Name"

### 2. Set Your Email Address <samp>(use the email associated with your GitHub account)</samp>
  - Run:
      ```bash
      git config --global user.email "your.email@example.com"
      ```

### 3. Verify Your Configuration
  - Run:
      ```bash
      git config --list
      ```

> [!NOTE]
> You can find a more comprehensive guide on git configurations in our [Git Configuration Guide](../moderate-git-guides/git-config-guide.md).


