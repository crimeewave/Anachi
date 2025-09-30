
# Anachi Terminal

Advanced Linux terminal emulator for Windows with package management system.

## Features

- Linux-like commands: cd, ls, cat, mkdir, rm, cp, mv, and more
- Package management: Install and manage custom packages
- Tab completion: Smart autocomplete for commands and files
- Session management: Save and restore your working session
- Custom themes: Multiple color schemes for the terminal
- Command history: Searchable history with Ctrl+R
- System monitoring: Real-time CPU, memory, and disk usage
- Aliases support: Create custom command shortcuts
- Cross-platform: Works on Windows, Linux, and macOS

## Installation

1. Install Python 3.7 or higher
2. Install required dependencies:
   ```bash
   pip install requests
   ```
3. Download anachi.py and run:
   ```bash
   python anachi.py
   ```

## Quick Start

```bash
# Basic navigation
cd /path/to/directory
ls -la
pwd

# File operations
cat filename.txt
mkdir new_folder
cp file1.txt file2.txt
rm old_file.txt

# Package management
pkg list                    # Show available packages
pkg install aneofetch       # Install a package
pkg remove aneofetch        # Remove a package
pkg installed               # Show installed packages

# System information
system-info                 # Show system monitor
theme dark                  # Change to dark theme
alias ll='ls -la'          # Create alias
```

## Package System

Anachi features a powerful package system that allows extending terminal functionality.

### Available Packages

- aneofetch: System information display
- anachi-filemanager: Dual-pane file manager
- anachi-desktop: Graphical desktop environment
- anachi-chat: Global terminal chat
- anachi-lang: Scripting language for automation

### Creating Packages

Packages are simple Python applications with a main.py entry point. See the packages repository for examples.

## Configuration

### Themes

Change terminal appearance:
```bash
theme default    # Default green/blue theme
theme dark       # Orange/blue dark theme  
theme matrix     # Green matrix theme
```

### Aliases

Create command shortcuts:
```bash
alias ll='ls -la'
alias h='history'
alias c='clear'
```

Aliases are saved automatically in ~/.anachi/aliases.json

### System Monitor

Toggle system information display:
```bash
system-info on    # Enable system monitor
system-info off   # Disable system monitor
```

## Command Reference

### Built-in Commands

- cd [directory] - Change directory
- ls [options] - List files
- pwd - Show current directory
- cat [file] - Display file content
- mkdir [name] - Create directory
- rm [file] - Remove file
- cp [src] [dst] - Copy file
- mv [src] [dst] - Move file
- clear - Clear screen
- echo [text] - Print text
- history - Show command history
- help - Display help
- exit - Exit terminal

### Package Commands

- pkg list - List available packages
- pkg install [name] - Install package
- pkg remove [name] - Remove package
- pkg installed - Show installed packages

### System Commands

- theme [name] - Change color theme
- alias [name='command'] - Create alias
- system-info [on/off] - Toggle system monitor
- session-save - Force save session
- session-info - Show session information

## Architecture

Anachi Terminal is built with a modular architecture:

- Core Terminal: Command processing and execution
- Package Manager: Handles package installation and management
- Session Manager: Saves and restores working sessions
- Theme Manager: Manages color schemes and appearance
- System Monitor: Provides real-time system information

## File Structure

```
~/.anachi/
  packages/          # Installed packages
  bin/               # Package executables
  session.json       # Session data
  aliases.json       # User aliases
```

## Development

### Adding New Commands

Commands are implemented as methods in the AnachiTerminal class. To add a new command:

1. Add method to AnachiTerminal class
2. Add command to execute_command method
3. Update help text

### Package Development

Packages require:
- main.py with main() function
- package.json with metadata
- ZIP archive for distribution

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

MIT License - see LICENSE file for details

## Support

For issues and questions:
- Create GitHub issue
- Check documentation
- Review existing packages

## Changelog

### v3.0
- Added tab completion
- Session management
- Custom themes
- System monitoring
- Aliases support

### v2.0
- Package management system
- Improved command set
- Better error handling

### v1.0
- Basic terminal functionality
- Core commands
- Initial release
```
# iuseanachibtw
