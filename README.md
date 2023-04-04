# hyprland-waayway

- **Window Manager** - [Hyprland](https://github.com/hyprwm/hyprland)
- **Display Manager** - [Ly](https://github.com/fairyglade/ly) Simple and works fine with hyprland
- **Shell** - Bash + Starship (might change later)
- **Terminal** - [Kitty](https://sw.kovidgoyal.net/kitty)
- **Panel** - Waybar using the aur package `waybar-hyprland-git`
- **Drawer** - [nwg-drawer](https://github.com/nwg-piotr/nwg-drawer) But using the colors from Kitty config of ChrisTitusTech
- **Notify Daemon** - [Dunst](https://github.com/dunst-project/dunst) Simple and functional
- **Launcher** - [Rofi](https://github.com/davatorium/rofi) 
- **File manager** - Thunar, simple and simple to theme
- **Config IDE** - Basic Neovim,
- **IDE** - VsCode

### Credits
These dotfiles are based on [hyprland-titus](https://github.com/ChrisTitusTech/hyprland-titus)

Ive also taken the waybar from [hyprland-dots](https://github.com/UnFunnyGuy/hyprland-dots)


## Setup
I would recommend using the archinstall command and setting up a simple sway desktop. Since it is closest to Hyprland

### We do Be Using yay

I recommend yay-bin since then it cannot break if your system has something wrong like settings
Run as user NOT ROOT!

```
# Before this you need base-devel and git installed
git clone https://aur.archlinux.org/yay-bin
cd yay-bin
makepkg -si
```

### Install le packages

``` bash
yay -S hyprland-bin polkit-gnome ffmpeg neovim viewnior       \
rofi pavucontrol thunar starship wl-clipboard wf-recorder     \
swaybg grimblast-git ffmpegthumbnailer tumbler playerctl      \
noise-suppression-for-voice thunar-archive-plugin kitty       \
waybar-hyprland wlogout swaylock-effects sddm-git pamixer     \
nwg-look-bin nordic-theme papirus-icon-theme dunst otf-sora   \
ttf-nerd-fonts-symbols-common otf-firamono-nerd inter-font    \
ttf-fantasque-nerd noto-fonts noto-fonts-emoji ttf-comfortaa  \
ttf-jetbrains-mono-nerd ttf-icomoon-feather ttf-iosevka-nerd  \
adobe-source-code-pro-fonts nwg-drawer
```

or execute the .install in this repo // Same command

to install ly just execute
```bash
yay -S ly
# and to enable ly
sudo systemctl enable ly
```

### Install the dotfiles...

Madness.ttf is the fonts package for all the icons in the top bar.
Copy the Madness.ttf to a fonts folder so on Arch
```bash
mkdir -p /usr/local/share/fonts/ttf/Madness
cp Madness.ttf /usr/local/share/fonts/ttf/Madness 
# And refresh the fonts cache
fc-cache
```

Copy the .config & .wallpapers & .bashrc to ~ or $HOME

