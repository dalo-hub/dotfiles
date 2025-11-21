# 🎨 Dotfiles

Minimal dotfiles setup for **Arch Linux** using the **Hyprland** window manager on Wayland.

This repository contains my personal setup and system configurations, focused on productivity and aesthetics.

## ✨ Features

- 🐧 Optimized Arch Linux base
- 🪟 Hyprland window manager (Wayland)
- ⚙️ Modular and reusable structure
- 🎯 Minimalist and efficient configurations
- 📦 Easy to adapt and extend

## 📋 Requirements

- **Arch Linux** (or compatible derivative)
- **Hyprland** installed and functioning on Wayland
- User permissions (no root required)

## 📁 Structure

```
dotfiles/
├── README.md              # This file
├── config/
│   └── hypr/
│       └── hyprland.conf  # Hyprland configuration
└── kitty/
    └── kitty.conf         # Kitty terminal emulator configuration
```

## 🚀 Installation

1. Clone the repository:

```bash
git clone https://github.com/dalo-hub/dotfiles.git ~/.dotfiles
```

2. Sync configuration files:

```bash
# Copy Hyprland configuration
cp ~/.dotfiles/config/hypr/hyprland.conf ~/.config/hypr/

# Copy Kitty configuration
cp ~/.dotfiles/kitty/kitty.conf ~/.config/kitty/
```

## 🔧 Included Configurations

### Hyprland (`config/hypr/hyprland.conf`)

Dynamic window manager based on Wayland with:

- Custom keyboard shortcuts
- Animations and visual effects
- Configurable workspaces

### Kitty (`kitty/kitty.conf`)

Fast and modern terminal emulator with:

- Custom color scheme
- Optimized fonts
- Productive shortcuts

## 📝 Status

🔨 Actively in development. More configurations and documentation will be added progressively.

## 🎯 Upcoming Improvements

- [ ] Shell configuration (Bash/Zsh)
- [ ] Automated dotfiles manager
- [ ] Quick installation script
- [ ] Custom theme
- [ ] Configuration for additional applications

## 📄 License

Free to use, modify, and distribute.

## 💬 Notes

This is a personal project in evolution. Feel free to adapt any configuration to your needs.
