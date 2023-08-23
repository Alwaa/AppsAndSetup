# Dual Booting with Windows
- Set time to local time: `timedatectl set-local-rtc 1 --adjust-system-clock`
  OR
- Set windows time to UTC (more finiky)

# App installs
### Chrome (as of 38)
```
sudo dnf install fedora-workstation-repositories
sudo dnf config-manager --set-enabled google-chrome
sudo dnf install google-chrome-stable
```

# NeoVim
