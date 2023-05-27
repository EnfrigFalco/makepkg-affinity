# makepkg-affinity
An Arch MakePKG to build Wine compatable with Affinity V2 suite

## On different distribution use toolbox and do the following:

### Prepare container
```
toolbox create --image quay.io/toolbx-images/archlinux-toolbox
toolbox enter archlinux-toolbox
git clone https://github.com/EnfrigFalco/makepkg-affinity.git
cd makepkg-affinity
```
#### Enable multilib in pacman configuration file
```
sudo pacman -Sy nano
sudo nano /etc/pacman.conf
```
Paste the following:
```
[multilib]
Include = /etc/pacman.d/mirrorlist
```
### Build
makepkg
```
