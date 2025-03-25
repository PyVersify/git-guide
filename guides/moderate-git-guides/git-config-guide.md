# Git Configuration Guide

Git configuration is essential for properly identifying your commits and connecting your local repositories to GitHub. This guide will walk you through the process of configuring Git for use with GitHub.

## Basic Git Configuration <samp>[Setting Your Identity]</samp>

Before using Git with GitHub, you need to configure your identity:

### Step 1: **Set your username**:
```bash
git config --global user.name "Your Name"
```

### Step 2: **Set your email address** <samp>(use the email associated with your GitHub account)</samp>:
```bash
git config --global user.email "your.email@example.com"
```

### Step 3: **Verify your configuration**:

```bash
git config --list
```

## Configuration Levels

Git configuration can be set at three different levels:

- **System level [`--system`]**: Applies to every user on the system

    ```bash
    git config --system user.name "Your Name"
    ```

- **Global level [`--global`]**: Applies to all your repositories

    ```bash
    git config --global user.name "Your Name"
    ```

- **Local level [`--local`]**: Specific to a single repository

    ```bash
    git config user.name "Your Name"
    ```

Each level overrides the previous one, with local settings taking precedence over global, and global over system.

## Editing Configuration Files Directly
You can also edit configuration files directly:

### 1. Edit system configuration:
```bash
git config --system --edit
```

### 2. Edit global configuration:

```bash
git config --global --edit
```

### 3. Edit local repository configuration:

```bash
git config --edit
```

## Configuration File Locations

### - Global Configuration:

- **Linux/Mac**: `~/.gitconfig`

- **Windows**: `C:\Users\USERNAME\.gitconfig`

### System Configuration:

- **Linux/Mac**: `/etc/gitconfig`

- **Windows**: `C:\ProgramData\Git\config`

### Local configuration:

- **Inside the repository**: `.git/config`

## Configuring for Multiple GitHub Accounts

If you need to use different GitHub accounts for different repositories

### Set global configuration for your primary GitHub account

```bash
git config --global user.name "Primary Name"
git config --global user.email "primary@example.com"
```

### For specific repositories

- Navigate to the repository folder and set local configuration:

    ```bash
    cd /path/to/repository
    git config user.name "Secondary Name"
    git config user.email "secondary@example.com"
    ```

### Add a remote to connect your local repository to GitHub

```bash
git remote add origin git@github.com:username/repository.git
```

### Push your local repository to GitHub

```bash
git push -u origin master
```

> [!NOTE]
> If you're using the newer default branch name, use main instead of master.

## Set default editor <samp>(e.g., nano)</samp>

```bash
git config --global core.editor nano
```

## Enable colorful output

```bash
git config --global color.ui true
```

## Set default branch name for new repositories

```bash
git config --global init.defaultBranch main
```

## Configure line ending behavior

```bash
# For Windows
git config --global core.autocrlf true

# For Mac/Linux
git config --global core.autocrlf input
By properly configuring Git, you'll ensure that your commits are correctly attributed and that your local repositories connect seamlessly with GitHub.
```