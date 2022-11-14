dnf group install base-x11
dnf group install base-x
dnf repolist
dnf -y install epel-release
dnf group install Xfce
vim /etc/gdm/custom.conf 
systemctl set-default graphical.target 
systemctl isolate graphical.target 
