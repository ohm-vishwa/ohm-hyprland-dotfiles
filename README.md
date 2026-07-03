# Arch Linux Hyprland Project

![Alt Text](Screenshot_03-Mar_18-16-28_11039.png)

## ✨ Auto clone and install

> [!CAUTION]
> If you are using FISH SHELL, DO NOT use this function. Clone and ran install.sh instead

- you can use this command to automatically clone the installer and ran the script for you
- NOTE: `curl` package is required before running this command

```bash
sh <(curl -L https://raw.githubusercontent.com/ohm-vishwa/ohm-hyprland-dotfiles/refs/heads/main/install.sh)
```

#### then

```sh
cd ~/
mkdir -p src
cd src
git clone https://github.com/ohm-vishwa/ohm-hyprland-dotfiles
cd ohm-hyprland-dotfiles
mv ~/.config/hypr ~/.config/hypr.bak
mv ~/.config/waybar ~/.config/waybar.bak
cp -r hypr waybar ~/.config/
```

### my config dependency

[Hyprland Plugins](https://hypr.land/plugins/)

- [Hypr Dynamic Cursor](https://github.com/VirtCode/hypr-dynamic-cursors)

- [Hypr Expo](https://github.com/hyprwm/hyprland-plugins/tree/main/hyprexpo)

```sh
sudo pacman -S hyprpm
```

```sh
hyprpm add https://github.com/hyprwm/hyprland-plugins
hyprpm add https://github.com/virtcode/hypr-dynamic-cursors
hyprpm update
hyprpm enable dynamic-cursors
hyprpm enable hyprexpo
```

check plugins

```sh
hyprpm list
```

## Keybinding related to waybar

```sh
bindd = $mainMod CTRL ALT, B, toggle waybar on/off, exec, pkill -SIGUSR1 waybar
bindd = $mainMod CTRL, B, waybar styles menu, exec, $scriptsDir/WaybarStyles.sh
bindd = $mainMod ALT, B, waybar layout menu, exec, $scriptsDir/WaybarLayout.sh
```
