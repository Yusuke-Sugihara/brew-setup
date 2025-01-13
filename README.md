# Brew Setup

This repository helps you manage and back up your Homebrew installations using a `Brewfile`. It allows you to quickly restore your Homebrew setup on a new machine in case your current system is replaced or damaged.

## Features
- Backup installed Homebrew packages, casks, and taps.
- Quickly restore Homebrew environment on a new system.
- Keep your development setup portable and version-controlled.

## Requirements
- [Homebrew](https://brew.sh/) installed on your system.

## How to Use

### 1. Clone this repository
```bash
git clone https://github.com/Yusuke-Sugihara/brew-setup.git
cd brew-setup
```

### 2. Restore Homebrew environment
Run the following command to install all packages, casks, and taps listed in the `Brewfile`:
```bash
brew bundle --file=Brewfile
```

### 3. Update the `Brewfile`
If you install or remove packages, update the `Brewfile` and push the changes to this repository:

1. Generate an updated `Brewfile`:
   ```bash
   brew bundle dump --file=Brewfile --force --describe
   ```
2. Commit and push the changes:
   ```bash
   git add Brewfile
   git commit -m "Update Brewfile"
   git push origin main
   ```

## Notes
- **Backup scope**: The `Brewfile` includes Homebrew packages, casks (applications), and taps.
- **Privacy**: Ensure that the `Brewfile` does not contain any sensitive information before committing it to a public repository.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Author
- [Yusuke Sugihara](https://github.com/Yusuke-Sugihara)
