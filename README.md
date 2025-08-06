# i3 Window Manager Configuration

A clean and minimal i3 configuration with custom status bar using i3blocks.

## Features

- **Clean Layout**: Organized configuration with minimal comments
- **Custom Workspaces**: Named workspaces for different applications
- **Status Bar**: Custom i3blocks configuration with system monitoring
- **Application Assignments**: Automatic workspace assignments for specific apps
- **Floating Dialogs**: Enhanced dialog window handling
- **Dark Theme**: Black color scheme with accent colors

## Installation

1. Install required dependencies:
   ```bash
   sudo pacman -S i3-wm i3blocks alacritty dmenu feh compton flameshot
   ```

2. Copy configuration files:
   ```bash
   mkdir -p ~/.config/i3
   cp config ~/.config/i3/
   cp i3blocks.conf ~/.config/i3/
   ```

3. Add wallpaper:
   ```bash
   # Place your wallpaper at ~/Downloads/wallpaper.jpg
   # Or modify the path in the config file
   ```

4. Restart i3 or reload configuration: `Mod+Shift+r`

## Key Bindings

| Key Combination | Action |
|-----------------|--------|
| `Mod + Return` | Open terminal (alacritty) |
| `Mod + d` | Application launcher (dmenu) |
| `Mod + q` | Kill focused window |
| `Mod + Shift + s` | Screenshot (flameshot) |
| `Mod + Shift + x` | Lock screen |
| `Mod + f` | Fullscreen toggle |
| `Mod + h/v` | Split horizontal/vertical |
| `Mod + s/w/e` | Stacking/Tabbed/Split layout |
| `Mod + r` | Resize mode |
| `Mod + Shift + c` | Reload configuration |
| `Mod + Shift + r` | Restart i3 |

## Workspaces

- **1: terminal** - Terminal applications
- **2: neovim** - Code editor (VS Code assigned here)
- **3: firefox** - Firefox browser
- **4: brave** - Brave browser
- **5-10** - General purpose workspaces

## Status Bar Modules

The i3blocks configuration includes:
-  Volume control
-  Memory usage
-  Disk usage
-  WiFi status
-  Bandwidth monitor
-  CPU usage
-  Battery status
-  Date and time (with seconds)

## Hardware Support

- **Audio**: PulseAudio volume controls
- **Brightness**: xbacklight controls
- **Mouse**: Logitech Wireless Mouse configuration
- **Display**: Dual monitor setup (eDP-1 + HDMI-1)
- **Touchpad**: Toggle functionality

## Customization

### Colors
Modify the color variables in the config:
```bash
set $bg-color          #000000  # Background
set $inactive-bg-color #2f343f  # Inactive windows
set $text-color        #f3f4f5  # Text
set $urgent-bg-color   #E53935  # Urgent windows
```

### Wallpaper
Change wallpaper path:
```bash
exec_always feh --bg-scale ~/path/to/your/wallpaper.jpg
```

### Applications
Modify application assignments:
```bash
assign [class="YourApp"] $ws1
```

## Dependencies

- **i3-wm**: Window manager
- **i3blocks**: Status bar
- **alacritty**: Terminal emulator
- **dmenu**: Application launcher
- **feh**: Wallpaper setter
- **compton**: Compositor
- **flameshot**: Screenshot tool
- **xbacklight**: Brightness control
- **pulseaudio**: Audio system

## File Structure

```
~/.config/i3/
├── config          # Main i3 configuration
└── i3blocks.conf   # Status bar configuration
```

