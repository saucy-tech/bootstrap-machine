# Mac Mini Sync Instructions

Follow these steps to sync your Mac Mini with your MacBook Pro setup using the bootstrap-machine repository.

## 1. Accessing the Repository

First, navigate to your working directory and clone/pull the repository:

```bash
# Navigate to your preferred directory
cd ~/Developer  # or your preferred location

# Clone if you haven't already
git clone git@github.com:bsauceda/bootstrap-machine.git

# Or pull if you already have it
cd bootstrap-machine
git pull origin main
```

## 2. Brewfile Setup

Copy and use the Brewfile:

```bash
# Copy Brewfile to home directory
cp Brewfile ~/Brewfile

# Navigate to home directory
cd ~

# Check what packages are missing (this won't install anything)
brew bundle check

# Install any missing packages
brew bundle install
```

## 3. Verification

After installation, verify that everything is properly installed:

```bash
# Check for any issues with Homebrew
brew doctor

# List all installed packages to verify
brew list
```

## 4. Cleanup

Optional cleanup after successful sync:

```bash
# Remove old versions of installed formulae
brew cleanup

# Optional: remove the Brewfile if you don't want to keep it in home directory
rm ~/Brewfile
```

## Troubleshooting

If you encounter any issues:
1. Run `brew doctor` to check for system issues
2. Ensure you have proper permissions: `sudo chown -R $(whoami) /usr/local/*`
3. Check the Homebrew logs: `brew config`

