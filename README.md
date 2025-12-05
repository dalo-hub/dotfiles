# 🎨 Dotfiles

Minimal dotfiles setup for **Arch Linux** using the **Hyprland** window manager on Wayland.

This repository contains my personal setup and system configurations, focused on productivity and aesthetics with a cohesive **Andromeda color scheme** throughout. Whether you're new to Linux ricing or looking to enhance your current setup, these configurations provide a solid foundation.

## ✨ Features

- 🐧 Optimized Arch Linux base system
- 🪟 Hyprland window manager (Wayland native) with custom animations
- 📊 Waybar status bar with system monitoring
- 🚀 Wofi application launcher with custom styling
- 🖥️ Kitty terminal with GPU acceleration
- ⭐ Starship prompt with language detection
- 🎯 Fastfetch system info with Rayquaza theme
- 🌄 Hyprpaper wallpaper daemon
- 🎨 Unified Andromeda color palette across all components
- ⚙️ Modular and reusable configuration structure
- 📦 Easy to adapt and extend for your needs

## 📋 Requirements

- **Arch Linux** (or compatible derivative like Manjaro, EndeavourOS)
- **Hyprland** - Wayland compositor
- **Waybar** - Status bar
- **Wofi** - Application launcher
- **Kitty** - Terminal emulator
- **Hyprpaper** - Wallpaper daemon
- **Fastfetch** - System information tool
- **Starship** - Shell prompt
- **JetBrainsMono Nerd Font** - Icon and symbol support

## 📁 Structure

```
dotfiles/
├── README.md              # This file
├── config/
│   ├── fastfetch/
│   │   └── config.jsonc   # Fastfetch system info configuration
│   ├── hypr/
│   │   ├── hyprland.conf  # Hyprland window manager configuration
│   │   └── hyprpaper.conf # Hyprpaper wallpaper configuration
│   ├── kitty/
│   │   └── kitty.conf     # Kitty terminal emulator configuration
│   ├── starship/
│   │   └── starship.toml  # Starship prompt configuration
│   ├── waybar/
│   │   ├── config         # Waybar status bar configuration
│   │   └── style.css      # Waybar styling
│   └── wofi/
│       ├── config         # Wofi launcher configuration
│       └── style.css      # Wofi styling
└── wallpapers/
    └── rayquaza-graffiti.jpg  # Rayquaza wallpaper
```

## 🚀 Installation

### Prerequisites

Install required packages on Arch Linux:

```bash
sudo pacman -S hyprland waybar wofi kitty hyprpaper fastfetch starship ttf-jetbrains-mono-nerd
```

### Quick Setup

1. Clone the repository:

```bash
git clone https://github.com/dalo-hub/dotfiles.git ~/.dotfiles
cd ~/.dotfiles
```

2. Create necessary directories:

```bash
mkdir -p ~/.config/{fastfetch,hypr,kitty,starship,waybar,wofi,wallpapers}
```

3. Sync configuration files:

```bash
# Copy all configurations
cp config/fastfetch/config.jsonc ~/.config/fastfetch/
cp config/hypr/hyprland.conf ~/.config/hypr/
cp config/hypr/hyprpaper.conf ~/.config/hypr/
cp config/kitty/kitty.conf ~/.config/kitty/
cp config/starship/starship.toml ~/.config/starship/
cp config/waybar/config ~/.config/waybar/
cp config/waybar/style.css ~/.config/waybar/
cp config/wofi/config ~/.config/wofi/
cp config/wofi/style.css ~/.config/wofi/

# Copy wallpapers
cp wallpapers/rayquaza-graffiti.jpg ~/.config/wallpapers/
```

4. Enable Starship prompt (add to your `~/.bashrc` or `~/.zshrc`):

```bash
eval "$(starship init bash)"  # For Bash
# OR
eval "$(starship init zsh)"   # For Zsh
```

### Manual Linking (Recommended)

For easier updates, create symbolic links instead of copying:

```bash
ln -sf ~/.dotfiles/config/fastfetch/config.jsonc ~/.config/fastfetch/
ln -sf ~/.dotfiles/config/hypr/hyprland.conf ~/.config/hypr/
ln -sf ~/.dotfiles/config/hypr/hyprpaper.conf ~/.config/hypr/
ln -sf ~/.dotfiles/config/kitty/kitty.conf ~/.config/kitty/
ln -sf ~/.dotfiles/config/starship/starship.toml ~/.config/starship/
ln -sf ~/.dotfiles/config/waybar/config ~/.config/waybar/
ln -sf ~/.dotfiles/config/waybar/style.css ~/.config/waybar/
ln -sf ~/.dotfiles/config/wofi/config ~/.config/wofi/
ln -sf ~/.dotfiles/config/wofi/style.css ~/.config/wofi/
ln -sf ~/.dotfiles/wallpapers/rayquaza-graffiti.jpg ~/.config/wallpapers/
```

This way, changes in the dotfiles repository automatically reflect in your config.

**Note:** This repository intentionally does not provide an automated install script. Configuration files live under `config/` — use the copy commands or the symbolic link examples above to install them to `~/.config`.

## 🔧 Included Configurations

### Hyprland (`config/hypr/hyprland.conf`)

Dynamic tiling Wayland compositor with smooth animations and custom keybindings:

**Features:**

- **Custom animations** - Smooth bezier curves for windows, workspaces, and layers
- **Dwindle layout** - Efficient window tiling with pseudotile support
- **10px gaps** between windows and 5px inner gaps
- **10px rounded corners** for modern aesthetic
- **Blur and shadows** - Elegant window decorations
- **Snap windows** - 10px gap spacing when snapping
- **Monitor support** - Primary eDP-1 at 1920x1080@60Hz, auto-detection for external monitors

**Key Bindings:**

- `SUPER + RETURN` - Launch Kitty terminal
- `SUPER + D` - Open Wofi application launcher
- `SUPER + E` - Open Dolphin file manager
- `SUPER + Q` - Close active window
- `SUPER + M` - Exit Hyprland
- `SUPER + F` - Toggle fullscreen
- `SUPER + SHIFT + SPACE` - Toggle floating mode
- `SUPER + SHIFT + C` - Reload Hyprland configuration
- `SUPER + [1-9]` - Switch to workspace
- `SUPER + SHIFT + [1-9]` - Move window to workspace
- `SUPER + S` - Toggle scratchpad
- `SUPER + Arrow keys` - Move focus between windows
- `SUPER + Mouse left/right` - Move/resize windows

**Media Keys:**

- Volume control (XF86AudioRaiseVolume/Lower/Mute)
- Brightness control (XF86MonBrightnessUp/Down)
- Media playback (requires playerctl)
- Microphone mute toggle

**Autostart:**

- Hyprpaper (wallpaper daemon)
- Waybar (status bar)

### Hyprpaper (`config/hypr/hyprpaper.conf`)

Wallpaper daemon for Hyprland:

- Preloads and displays `~/.config/wallpapers/rayquaza-graffiti.jpg`
- Fast wallpaper loading on startup
- Applies to all monitors

### Waybar (`config/waybar/`)

Highly customizable status bar for Wayland:

**Modules Left:**

- **CPU** - Current usage percentage with icon
- **Memory** - Used RAM in GB with icon
- **Disk** - Free disk space in GB with icon

**Modules Center:**

- **Workspaces** - Hyprland workspace indicators (6 persistent workspaces)
  - Default icon: 󰐝
  - Active workspace highlighted in red (`#ee5d43`)

**Modules Right:**

- **System Tray** - Application tray icons
- **PulseAudio** - Volume control (click to open pavucontrol)
- **Battery** - Battery percentage with status icons
- **Clock** - Time in HH:MM format (click for full date)

**Styling:**

- Dark background (`#23262e`) with yellow borders (`#ffe66d`)
- Rounded corners (0.5-0.6rem)
- Top position with 10px margins
- JetBrainsMono Nerd Font, 14px bold
- Red accent color for icons and active states

### Wofi (`config/wofi/`)

Application launcher for Wayland:

**Features:**

- **Centered window** - 500px wide, 8 lines visible
- **drun mode** - Application launcher
- **Dark theme** enabled
- **Case-insensitive search**
- **Image support** - Shows application icons
- **Custom prompt** - " Search"

**Styling:**

- Dark background (`#23262e`) with yellow border (`#ffe66d`)
- Rounded corners (14px window, 12px entries)
- Selection highlight in gray (`#3d4352`)
- Focus indication with yellow border
- JetBrainsMono Nerd Font

### Kitty (`config/kitty/kitty.conf`)

GPU-accelerated terminal emulator:

**Features:**

- **JetBrainsMono Nerd Font** - 12pt size with icon support
- **Beam cursor** - Modern cursor style
- **7px horizontal, 10px vertical padding**
- **3000 lines scrollback**
- **Full opacity** (no transparency)
- **Font resizing** - `Ctrl+Shift+Plus/Minus`

**Andromeda Color Scheme:**

- Background: `#23262E`
- Foreground: `#D5CED9`
- Cursor: `#FFE66D` (yellow)
- Selection: `#3D4352` background
- URL: `#00e8c6` (cyan)
- Active border: `#00e8c6` (cyan)
- 16-color palette with bright variants

**Special Colors:**

- Red: `#ee5d43`
- Green: `#96E072`
- Yellow: `#FFE66D`
- Blue: `#7cb7ff`
- Magenta: `#ff00aa`
- Cyan: `#00e8c6`

### Starship (`config/starship/starship.toml`)

Fast, customizable shell prompt written in Rust:

**Features:**

- **Andromeda color palette** - Matches system theme
- **Multi-segment layout** - OS, user, directory, git, languages, docker, time
- **OS detection** - Custom symbols for 20+ distributions
- **Username display** - Always visible with style
- **Directory truncation** - 3 levels with custom folder icons
- **Git integration** - Branch and status indicators
- **Language detection** - Python, Node.js, C, C++, Rust, Go, PHP, Java, Kotlin, Haskell
- **Environment support** - Docker, Conda, Pixi
- **Time module** - HH:MM format display
- **Status character** - Visual success/error indication

**Module Stack:**

```
[OS][User][Directory][Git Branch][Git Status][Languages][Docker/Conda/Pixi][Time]
[❯ Prompt]
```

**Color Segments:**

- Yellow background: OS and user
- Red background: Directory
- Gray background: Git, languages, and time
- Red/Yellow prompt character based on exit status

### Fastfetch (`config/fastfetch/config.jsonc`)

Modern system information tool:

**Features:**

- **Rayquaza PNG logo** - Kitty graphics protocol display
- **Custom layout** - Boxed design with borders
- **Yellow key color** with red title accents
- **Comprehensive info** - User, hostname, uptime, OS, kernel, DE, terminal, shell, CPU, disk, memory, network
- **Color palette display** - Terminal colors with circle symbols

**Modules Displayed:**

- User and hostname
- System uptime
- Distribution and kernel
- Desktop environment (Hyprland)
- Terminal (Kitty) and shell
- CPU with P/E core count
- Disk usage for root partition
- Memory usage
- Local IPv4 address with interface name
- Terminal color preview

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

## 📝 Current Setup

✅ **Complete configurations for:**

- ✅ Hyprland window manager with animations and keybindings
- ✅ Hyprpaper wallpaper daemon
- ✅ Waybar status bar with system monitoring
- ✅ Wofi application launcher
- ✅ Kitty terminal with Andromeda theme
- ✅ Starship prompt with language detection
- ✅ Fastfetch system info with Rayquaza theme
- ✅ Unified Andromeda color scheme
- ✅ Rayquaza graffiti wallpaper

## 🎯 Upcoming Improvements

- [ ] Shell configuration (Bash/Zsh with aliases and functions)
- [ ] Notification daemon (Dunst/Mako) configuration
- [ ] Screenshot tool (Grim/Slurp) integration with keybindings
- [ ] Screen recording setup
- [ ] Neovim configuration
- [ ] GTK/Qt theme files
- [ ] Additional wallpapers
- [ ] Automated installation script with backup
- [ ] Lock screen (Swaylock) configuration

## 📄 License

Free to use, modify, and distribute. No restrictions applied.

## 🤝 Contributing

Found an issue or have suggestions? Feel free to:

- Report bugs and improvements
- Fork and adapt for your needs
- Share your enhancements

## 🖼️ Screenshots

The setup features a cohesive Andromeda-themed environment with:

- Rayquaza graffiti wallpaper
- Yellow (`#FFE66D`) and red (`#ee5d43`) accent colors
- Dark background (`#23262E`) throughout
- Consistent styling across all components

## 🔗 Resources

- [Hyprland Documentation](https://wiki.hyprland.org)
- [Waybar Documentation](https://github.com/Alexays/Waybar)
- [Wofi Documentation](https://hg.sr.ht/~scoopta/wofi)
- [Kitty Documentation](https://sw.kovidgoyal.net/kitty/)
- [Starship Documentation](https://starship.rs)
- [Fastfetch Documentation](https://github.com/fastfetch-cli/fastfetch)
- [Arch Wiki](https://wiki.archlinux.org)
- [Wayland Project](https://wayland.freedesktop.org)

## 💡 Tips

**After installation:**

1. Log out and select Hyprland from your display manager
2. Press `SUPER + D` to open Wofi and launch applications
3. Use `SUPER + RETURN` to open Kitty terminal
4. Run `fastfetch` to see the system info display
5. Check Waybar at the top for system monitoring

**Customization:**

- Modify colors in each config file to match your preferences
- The Andromeda palette variables are defined in each configuration
- Adjust gaps, borders, and animations in `hyprland.conf`
- Change wallpaper path in `hyprpaper.conf`
- Customize Waybar modules in `config/waybar/config`

## 💬 Notes

This is a personal project in continuous evolution. Feel free to adapt any configuration to your specific needs and preferences. No single setup fits everyone—use this as inspiration and customize liberally!

The Andromeda color scheme provides excellent readability and visual consistency. All components are designed to work together seamlessly while maintaining performance and simplicity.
