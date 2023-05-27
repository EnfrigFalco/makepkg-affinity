# makepkg-affinity
An Arch MakePKG to build Wine compatable with Affinity V2 suite

If on different distribution build with the following:

```
toolbox create --image quay.io/toolbx-images/archlinux-toolbox
toolbox enter archlinux-toolbox
sudo pacman -Sy nano

# Enable multilib
sudo nano /etc/pacman.conf
    [multilib]
    Include = /etc/pacman.d/mirrorlist

# Download Wine Affinity AUR package: 
makepkg
```
