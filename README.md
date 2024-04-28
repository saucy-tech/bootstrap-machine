# Computer Setup Configurations

This repository contains configuration files and scripts for quickly setting up new computers with necessary software using different package managers like Homebrew, Chocolatey, and Nix.

## Requirements

- **Git**: Required for cloning this repository.
- **Package Managers**: Ensure the appropriate package managers are installed on the machine:
  - Chocolatey for Windows
  - Homebrew for macOS
  - Nix for Unix-like systems

## Usage Instructions

### Install Package Managers

```bash
# Choclatey for Windows
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

# Homebrew for macOS
```

### Cloning the Repository

To use the configurations and scripts, start by cloning the repository to your new machine:

```bash
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name
```

### Running Configurations

Navigate to the appropriate directory for your OS/package manager and execute the installation commands:

#### Homebrew (macOS)

```bash
cd brew/
brew bundle
```

#### Chocolatey (Windows)

```powershell
cd choco/
choco install --packages.config="packages.config.json" -y
```

#### Nix (Unix-like Systems)

```bash
cd nix/
nix-env -i all -f ./default.nix
```

## Workflow and Maintenance

To ensure that your configurations are always up-to-date and allow for easy updating of the setup scripts, consider the following practices:

1. **Regular Updates**: Regularly push updates to the repository as you modify or add configurations.
2. **Pre-Installation Updates**: Always pull from the repository before running the scripts on a new machine to ensure you are using the latest versions.

## Conclusion

By organizing your repository in this manner, you provide clear instructions and a streamlined system that can be easily used and maintained. This setup not only helps in automating and simplifying the setup process but also facilitates easy updates and modifications as your software needs evolve.
