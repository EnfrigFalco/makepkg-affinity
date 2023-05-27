# makepkg-affinity
An Arch makepkg script to automate the building of a Wine prefix compatable to Serif Affinity V2 suite.

## If using a different distribution use Toolbox and enter the following prompts:
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
