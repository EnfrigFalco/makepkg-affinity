# makepkg-affinity
An Arch makepkg script to automate the building of a Wine prefix compatable to Serif Affinity V2 suite. Made possible by the efforts of to Wanesty and Grunt. More information at https://forum.affinity.serif.com/index.php?/topic/182758-affinity-suite-v204-on-linux-wine/

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
git clone https://github.com/EnfrigFalco/makepkg-affinity-v2.git
```
Enter folder
```
cd makepkg-affinity-v2
```
Install build packages
```
chmod +x arch-wine-dependencies.sh
```
```
sudo ./arch-wine-dependencies.sh
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
