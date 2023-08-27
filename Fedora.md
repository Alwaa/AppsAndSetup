# Setup Script


# Dual Booting with Windows
- Set time to local time: `timedatectl set-local-rtc 1 --adjust-system-clock`
  OR
- Set windows time to UTC (more finicky)

```
sudo dnf install grub-customizer
```
[Link to commands for displaying fedora (35, but worked with 38)](https://youtu.be/VaIgbTOvAd0?si=tuTmIvhpZAOa1L6t&t=1083)
- /etc/default/grub
- GRUB_ENABLE_BLSCFG -> false
- ``sudo grub2-mkconfig -o /boot/grub2/grub.cfg`
	> (maybe) Instead of: `sudo grub2-mkconfig -o /boot/efi/EFI/fedora/grub.cfg `
	> It seems to boot wight into fedora with the "efi/EFI" one
- (Still not working :((( ) Add background image to root folder
# App installs
FIRST?
```
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
```
### Chrome (as of 38)
```
sudo dnf install fedora-workstation-repositories
sudo dnf config-manager --set-enabled google-chrome
sudo dnf install google-chrome-stable
```

### Obsidian
```
flatpak install flathub md.obsidian.Obsidian
```

> Setup Minimal Theme
> Fetch git repositories
> setup vaults (one for each repo) in the folder `~Documents/obsidian/`
### Discord
```
flatpak install flathub com.discordapp.Discord
```

### Steam
```
flatpak install flathub com.valvesoftware.Steam
```
> Turn off run in background in app settings
> Maybe steam-devices needed for controller support

### Sejda
- Only as a .deb for the moment... Use web version


# SETUP

git:
```
git config --global user.name "Alwaa"
git config --global user.email "74717334+Alwaa@users.noreply.github.com"
sudo dnf install gh
```
> Login with github cli `gh auth login`

htop:
```
sudo dnf update -y && sudo dnf upgrade -y
sudo dnf install htop
```


# NeoVim
```
sudo dnf install neovim
git clone https://github.com/NvChad/NvChad ~/.config/nvim --depth 1 && nvim
```
> No to custom config
Then:
```
mv ~/.config/nvim/lua/custom ~/.config/nvim/lua/custom-backup
git clone https://github.com/Alwaa/nvchad-custom.git ~/.config/nvim/lua/custom
nvim
```
 And setup a [NerdFont](https://www.nerdfonts.com/font-downloads)
 ```
 mkdir -p ~/.local/share/fonts/HackMono
 unzip ~/Downloads/Hack.zip -d ~/.local/share/fonts/HackMono/
 fc-cache -v
 ```
 