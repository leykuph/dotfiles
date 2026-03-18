<div align="center">

# ✦ dotfiles

**leykuph's Arch Linux configuration — OC Palette**

![Arch Linux]
![Hyprland]
![Waybar]

</div>

---

## ✦ Screenshots

![desktop](./.screenshots/1.png)
![desktop2](./.screenshots/2.png)

---

## ✦ Setup

| Component | App |
|-----------|-----|
| **WM** | [Hyprland](https://hyprland.org) |
| **Bar** | [Waybar](https://github.com/Alexays/Waybar) |
| **Launcher** | [Wofi](https://hg.sr.ht/~scoopta/wofi) |
| **Terminal** | [Kitty](https://sw.kovidgoyal.net/kitty) |
| **Shell** | [Fish](https://fishshell.com) |
| **Prompt** | [Starship](https://starship.rs) |
| **Notifications** | [Swaync](https://github.com/ErikReider/SwayNotificationCenter) |
| **File Manager** | [Yazi](https://github.com/sxyazi/yazi) |
| **System Monitor** | [Btop](https://github.com/aristocratos/btop) |
| **Idle Daemon** | [Hypridle](https://github.com/hyprwm/hypridle) |
| **Wallpaper** | [Hyprpaper](https://github.com/hyprwm/hyprpaper) |
| **Cursor** | [Bibata Modern Classic](https://github.com/ful1e5/Bibata_Cursor) |
| **Font** | JetBrainsMono Nerd Font |

---

## ✦ OC Palette

> Dark nocturnal aesthetic — purple structural, orange for attention, no neon.

| Role | Hex |
|------|-----|
| Background | `#1A1626` |
| Card | `#221C34` |
| Input | `#2A2342` |
| Purple Accent | `#AF87D7` |
| Orange Accent | `#E19B5A` |
| Text | `#F5F0FA` |
| Muted Text | `#C7BDD9` |
| Inactive | `#8F84A6` |
| Shadow/Border | `#5E4A7F` |
| Error/Red | `#E85A6A` |
| Green | `#7BC8A4` |
| Gold | `#F2C86A` |

---

## ✦ Installation

> Uses a bare git repo to manage dotfiles in place.

```bash
# Clone the repo
git clone --bare https://github.com/leykuph/dotfiles.git $HOME/.dotfiles

# Set up the alias (fish)
echo "alias dotfiles='git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'" >> ~/.config/fish/config.fish
source ~/.config/fish/config.fish

# Hide untracked files
dotfiles config --local status.showUntrackedFiles no

# Checkout files
dotfiles checkout
```

> **Note:** If there are conflicts with existing configs, back them up first.

---

## ✦ Dependencies

```bash
# Core
sudo pacman -S hyprland waybar wofi kitty fish starship \
  swaync yazi btop hypridle hyprpaper grim brightnessctl \
  wl-clipboard jq

# AUR
yay -S bibata-cursor-theme
```

---

## ✦ Structure

```
~/.config/
├── hypr/
│   ├── hyprland.conf
│   └── hypridle.conf
├── waybar/
│   ├── config.jsonc
│   └── style.css
├── kitty/
│   └── kitty.conf
├── wofi/
│   └── style.css
├── swaync/
│   └── style.css
├── yazi/
│   ├── yazi.toml
│   └── theme.toml
├── btop/
│   └── themes/oc-palette.theme
└── starship.toml
.nanorc
```

---

<div align="center">

*built with 🎵 and too many hours of ricing*

</div>
