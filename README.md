# makepkg-affinity
An Arch MakePKG to build Wine compatable with Affinity V2 suite

## On different distribution use toolbox and do the following:
Create Arch container
```
toolbox create --image quay.io/toolbx-images/archlinux-toolbox
```
Enter Arch container
```
toolbox enter archlinux-toolbox
```
Clone repository
```
git clone https://github.com/EnfrigFalco/makepkg-affinity.git
```
Enter folder
```
cd makepkg-affinity
```
Install nano
```
sudo pacman -Sy nano
```
Use nano to edit pacman configuration file
```
sudo nano /etc/pacman.conf
```
Paste the following in pacman.conf:
```
[multilib]
Include = /etc/pacman.d/mirrorlist
```
Build Wine with:
```
makepkg
```
