# 🎨 Dotfiles

Minimal dotfiles setup for **Arch Linux** using the **Hyprland** window manager on Wayland.

This repository contains my personal setup and system configurations, focused on productivity and aesthetics. Whether you're new to Linux ricing or looking to enhance your current setup, these configurations provide a solid foundation.

## ✨ Features

- 🐧 Optimized Arch Linux base system
- 🪟 Hyprland window manager (Wayland native)
- ⚙️ Modular and reusable configuration structure
- 🎯 Minimalist and efficient approach
- 📦 Easy to adapt and extend for your needs
- 🚀 Performance-focused setup

## 📋 Requirements

- **Arch Linux** (or compatible derivative like Manjaro, EndeavourOS)
- **Hyprland** installed and functioning on Wayland
- Basic familiarity with terminal and configuration files
- User permissions (no root/sudo required for installation)

## 📁 Structure

```
dotfiles/
├── README.md              # This file
└── config/
    ├── fastfetch/
    │   └── config.jsonc   # Fastfetch system info configuration
    ├── hypr/
    │   └── hyprland.conf  # Hyprland configuration
    ├── kitty/
    │   └── kitty.conf     # Kitty terminal emulator configuration
    └── starship/
        └── starship.toml  # Starship prompt configuration
```

## 🚀 Installation

### Quick Setup

1. Clone the repository:

```bash
git clone https://github.com/dalo-hub/dotfiles.git ~/.dotfiles
cd ~/.dotfiles
```

2. Create necessary directories:

```bash
mkdir -p ~/.config/fastfetch
mkdir -p ~/.config/hypr
mkdir -p ~/.config/kitty
mkdir -p ~/.config/starship
```

3. Sync configuration files:

```bash
# Copy Fastfetch configuration
cp config/fastfetch/config.jsonc ~/.config/fastfetch/

# Copy Hyprland configuration
cp config/hypr/hyprland.conf ~/.config/hypr/

# Copy Kitty configuration
cp config/kitty/kitty.conf ~/.config/kitty/

# Copy Starship configuration
cp config/starship/starship.toml ~/.config/starship/
```

### Manual Linking (Optional)

For easier updates, create symbolic links instead of copying:

```bash
ln -sf ~/.dotfiles/config/fastfetch/config.jsonc ~/.config/fastfetch/
ln -sf ~/.dotfiles/config/hypr/hyprland.conf ~/.config/hypr/
ln -sf ~/.dotfiles/config/kitty/kitty.conf ~/.config/kitty/
ln -sf ~/.dotfiles/config/starship/starship.toml ~/.config/starship/
```

This way, changes in the dotfiles repository automatically reflect in your config.
This repository intentionally does not provide an automated install script.

Configuration files live under `config/` — use the copy commands or the symbolic link examples above to install them to `~/.config`.

Recommendation: prefer creating symbolic links (as shown in the "Manual Linking" section) so updates to this repository automatically propagate to your active configuration.

## 🔧 Included Configurations

### Fastfetch (`config/fastfetch/config.jsonc`)

A minimalist system information display tool featuring:

- **Custom Rayquaza logo** - Displays Pokémon art as system header
- **System monitoring** - Shows user, hostname, uptime, OS, kernel, desktop environment
- **Hardware details** - CPU (with P/E core count), disk usage, and memory information
- **Network information** - Displays local IP address and network interface
- **Shell detection** - Shows currently active shell and terminal
- **Color scheme** - Matches the Andromeda color palette for aesthetic consistency
- **Color indicators** - Terminal color palette visualization at bottom

**Key modules displayed:**

- User and hostname
- System uptime
- Distribution info
- Kernel version
- Desktop environment (Hyprland)
- Terminal emulator (Kitty)
- Active shell
- CPU and disk statistics
- Memory usage
- Local IP address and network interface
- Terminal colors

### Hyprland (`config/hypr/hyprland.conf`)

A dynamic tiling window manager with:

- **Custom keyboard shortcuts** - Optimized for productivity
- **Animations and visual effects** - Smooth and modern UI transitions
- **Configurable workspaces** - Multiple desktops for organization
- **Multi-monitor support** - Seamless experience across displays
- **Customizable gaps and layouts** - Master-stack, dwindle, and more

**Key bindings:**

- `SUPER + [1-9]` - Switch workspaces
- `SUPER + [H/J/K/L]` - Navigate windows
- `SUPER + [T/V/S/F]` - Change layouts
- `SUPER + Enter` - Launch terminal (Kitty)
- `SUPER + Alt + Q` - Close window

### Kitty (`config/kitty/kitty.conf`)

A GPU-accelerated terminal emulator featuring:

- **Custom color scheme** - Andromeda-inspired palette optimized for readability
- **Performance optimized** - Faster than traditional terminal emulators
- **Font configuration** - JetBrainsMono Nerd Font for icons and symbols
- **Productive shortcuts** - Quick actions for font resizing
- **True color support** - Full RGB color capabilities
- **Beam cursor** - Modern cursor style with shell integration disabled

**Color Scheme:**

- Primary background: `#23262E`
- Primary foreground: `#D5CED9`
- Accent colors: Cyan (`#00e8c6`), Yellow (`#FFE66D`), Red (`#ee5d43`), Green (`#96E072`)

## 🎯 Shell & Prompt

### Starship (`config/starship/starship.toml`)

A cross-platform, minimal prompt built in Rust featuring:

- **Fast and lightweight** - Written in Rust for optimal performance
- **Language indicators** - Shows active programming languages (Python, Node.js, C, C++, Rust, Go, PHP, Java, Kotlin, Haskell)
- **Git integration** - Real-time repository status, branch information, and change indicators
- **Custom modules** - Directory with truncation, command duration, exit status, and time display
- **Andromeda theme** - Color palette matching the system's aesthetic
- **Environment awareness** - Displays Docker context, Conda, and Pixi environments
- **Dynamic format** - Organized prompt segments with smooth color transitions

**Module Stack:**

- OS indicator (with custom symbols for each distribution)
- Username and authentication status
- Current directory (with custom folder icons)
- Git branch and status
- Programming language versions
- Docker context
- Time display with HH:MM format
- Visual prompt character with status indication

**Installation:**

```bash
# Install Starship (if not already installed)
curl -sS https://starship.rs/install.sh | sh

# Add to your shell config (~/.bashrc or ~/.zshrc)
eval "$(starship init bash)"  # For Bash
eval "$(starship init zsh)"   # For Zsh
```

## 🎨 Color Palette

All configurations use the **Andromeda color palette** for visual consistency:

| Color        | Hex       | Usage                        |
| ------------ | --------- | ---------------------------- |
| Background   | `#23262E` | Primary background           |
| Foreground   | `#D5CED9` | Primary text                 |
| Yellow/Gold  | `#FFE66D` | Accents, highlights          |
| Red          | `#ee5d43` | Errors, active borders       |
| Cyan/Teal    | `#00e8c6` | Secondary accents            |
| Green        | `#96E072` | Success, positive indicators |
| Purple       | `#ff00aa` | Additional accent            |
| Blue         | `#7cb7ff` | Secondary highlight          |
| Neutral Gray | `#746F77` | Inactive/muted elements      |
| Surface      | `#3D4352` | UI surface color             |

## 📝 Status

🔨 **Actively in development.** More configurations and documentation will be added progressively.

Current focus areas:

- Core Hyprland and Kitty configurations ✅
- Documentation improvements 🔄
- Additional application configs (coming soon)

## 🎯 Upcoming Improvements

- [ ] Shell configuration (Bash/Zsh with custom prompts)
- [ ] Automated dotfiles manager script
- [ ] Quick installation script with validation
- [ ] Custom GTK/Qt theme integration
- [ ] Configuration for additional applications (Neovim, Dunst, etc.)
- [ ] Wallpaper management
- [ ] System-wide keyboard shortcuts documentation
- [ ] Video/screenshot configuration

## 📄 License

Free to use, modify, and distribute. No restrictions applied.

## 🤝 Contributing

Found an issue or have suggestions? Feel free to:

- Report bugs and improvements
- Fork and adapt for your needs
- Share your enhancements

## 🔗 Resources

- [Hyprland Documentation](https://wiki.hyprland.org)
- [Kitty Documentation](https://sw.kovidgoyal.net/kitty/)
- [Arch Wiki](https://wiki.archlinux.org)
- [Wayland Project](https://wayland.freedesktop.org)

## 💬 Notes

This is a personal project in continuous evolution. Feel free to adapt any configuration to your specific needs and preferences. No single setup fits everyone—use this as inspiration and customize liberally!
