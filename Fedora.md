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
- `sudo grub2-mkconfig -o /boot/efi/EFI/fedora/grub.cfg `
# App installs
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

### Sejda
**TODO**
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
