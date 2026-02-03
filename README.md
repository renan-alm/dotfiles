# Dotfiles

Personal dotfiles configuration for macOS with Zsh.

## Overview

A collection of shell configuration files to set up a consistent development environment across machines. Designed for use with [Oh My Zsh](https://ohmyz.sh/) and [Powerlevel10k](https://github.com/romkatv/powerlevel10k).

## Contents

```
dotfiles/
├── .my_zshrc              # Main Zsh configuration
└── config/
    ├── renan-aliases      # Shell aliases
    ├── renan-envvars      # Environment variables
    ├── renan-functions    # Bash/Zsh functions
    └── eof-config         # End-of-file configs (loaded last)
```

### Configuration Files

| File | Description |
|------|-------------|
| `.my_zshrc` | Main Zsh config with Oh My Zsh, Powerlevel10k, kubectl completion, and plugin loading |
| `renan-aliases` | Shortcuts for navigation, git, docker, terraform, and kubernetes |
| `renan-envvars` | PATH exports and tool configurations (Terraform, Go, Ansible) |
| `renan-functions` | Helper functions for Python venv, Docker, Git, and more |
| `eof-config` | Configurations that must be sourced at the end of shell init |

## Prerequisites

- macOS with [Homebrew](https://brew.sh/)
- [Oh My Zsh](https://ohmyz.sh/)
- [Powerlevel10k](https://github.com/romkatv/powerlevel10k) (`brew install powerlevel10k`)
- Recommended plugins: `zsh-autosuggestions`, `zsh-syntax-highlighting`, `fzf`, `asdf`

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/<username>/dotfiles.git ~/dotfiles
   ```

2. Create symlinks:
   ```bash
   ln -s ~/dotfiles/.my_zshrc ~/.zshrc
   ```

3. Update the source paths in `.my_zshrc` to point to your dotfiles location.

4. Reload your shell:
   ```bash
   source ~/.zshrc
   ```


## License

MIT
