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
├── config/
│   └── hypr/
│       └── hyprland.conf  # Hyprland configuration
├── kitty/
│   └── kitty.conf         # Kitty terminal emulator configuration
└── starship/
    └── starship.toml      # Starship prompt configuration
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
mkdir -p ~/.config/hypr
mkdir -p ~/.config/kitty
mkdir -p ~/.config/starship
```

3. Sync configuration files:

```bash
# Copy Hyprland configuration
cp config/hypr/hyprland.conf ~/.config/hypr/

# Copy Kitty configuration
cp kitty/kitty.conf ~/.config/kitty/

# Copy Starship configuration
cp starship/starship.toml ~/.config/starship/
```

### Manual Linking (Optional)

For easier updates, create symbolic links instead of copying:

```bash
ln -sf ~/.dotfiles/config/hypr/hyprland.conf ~/.config/hypr/
ln -sf ~/.dotfiles/kitty/kitty.conf ~/.config/kitty/
ln -sf ~/.dotfiles/starship/starship.toml ~/.config/starship/
```

This way, changes in the dotfiles repository automatically reflect in your config.

## 🔧 Included Configurations

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

### Kitty (`kitty/kitty.conf`)

A GPU-accelerated terminal emulator featuring:

- **Custom color scheme** - Optimized for readability and aesthetics
- **Performance optimized** - Faster than traditional terminal emulators
- **Font configuration** - Nerd Font support for icons and symbols
- **Productive shortcuts** - Quick actions and window management
- **True color support** - Full RGB color capabilities

## 🎯 Shell & Prompt

### Starship (`starship/starship.toml`)

A cross-platform, minimal prompt built in Rust featuring:

- **Fast and lightweight** - Written in Rust for optimal performance
- **Language indicators** - Shows active programming languages and versions
- **Git integration** - Real-time repository status and branch information
- **Custom modules** - Directory, command duration, exit status, and more
- **Starry theme** - Beautiful and minimalist visual design
- **Environment awareness** - Displays active virtual environments (Python, Node.js, etc.)

**Installation:**

```bash
# Install Starship (if not already installed)
curl -sS https://starship.rs/install.sh | sh

# Add to your shell config (~/.bashrc or ~/.zshrc)
eval "$(starship init bash)"  # For Bash
eval "$(starship init zsh)"   # For Zsh
```

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
