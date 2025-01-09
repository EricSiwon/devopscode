
# Configuration de base

## Depuis une installation serveur avec Apache et SSH

> iso : debian-12.5.0-amd64-netinstall.iso
> Install Serveur iniquement + SSH + Apache


### Ip address

> Execution sous root `su -`

```bash
ip -4 addr
```

```console
(myvenv) siwone@debiandetest:~$ ip -4 addr

1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
2: ens18: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    altname enp0s18
    inet 192.168.1.124/24 brd 192.168.1.255 scope global dynamic ens18
       valid_lft 26705sec preferred_lft 26705sec
```

### Changer IP Address

> Sur une install Desktop Xcfe

```console
# ip route show

default via 192.168.1.254 dev ens18 proto dhcp src 192.168.1.45 metric 100
192.168.1.0/24 dev ens18 proto kernel scope link src 192.168.1.45 metric 100

# ls /sys/class/net

ens18  lo


# vi /etc/network/interfaces

allow-hotplug ens18
iface ens18 inet static
   address 192.168.1.179/24
   gateway 192.168.1.254
   dns-nameservers 8.8.8.8 8.8.4.4

: Redémarrer le service réseau

# systemctl restart networking.service
# ou REBOOT

: Vérification de la configuration

ip addr show ens18

ip a

# ip route show

default via 192.168.1.254 dev ens18 onlink
192.168.1.0/24 dev ens18 proto kernel scope link src 192.168.1.179

# ip -4 addr

1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
2: ens18: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    altname enp0s18
    inet 192.168.1.179/24 brd 192.168.1.255 scope global ens18
       valid_lft forever preferred_lft forever

ls /sys/class/net

ens18  lo

cat /etc/network/interfaces

# This file describes the network interfaces available on your system
# and how to activate them. For more information, see interfaces(5).

source /etc/network/interfaces.d/*

# The loopback network interface
auto lo
iface lo inet loopback

allow-hotplug ens18
iface ens18 inet static
   address 192.168.1.179/24
   gateway 192.168.1.254
   dns-nameservers 8.8.8.8 8.8.4.4

```

### Mise à jour du system

```bash
apt-get update
apt-get dist-upgrade

dpkg --list
```

### Config Remote Session Xclient

> L'utilisateur ne doit pas étre déjà connecté dans une autre session : logoff !

```bash
apt update && sudo apt upgrade -y
# apt install xfce4 xfce4-goodies xorg dbus-x11 x11-xserver-utils -y
apt install xrdp -y
systemctl status xrdp
adduser xrdp ssl-cert
systemctl restart xrdp

? echo "startxfce4" > ~/.Xclients
? chmod +x ~/.Xclients

sudo apt-get install ufw
ufw allow 3389
```

### Installation python

```bash
su -
apt install python3.11-venv
exit
python3 -m venv myvenv

source ./myvenv/bin/activate
```

### Config .Bashrc (Setting windows title)

```bash
set-window-title() {
  #echo -en "\033]0;$(pwd | sed -e "s;^$HOME;~;")\a"
  echo -en "\033]0;$(pwd | sed -e "s;^/home/tsan2/appli/;~;")\a"
}

if [[ "$PROMPT_COMMAND" ]]; then
  export PROMPT_COMMAND="$PROMPT_COMMAND;set-window-title"
else
  export PROMPT_COMMAND=set-window-title
fi
```

### Le fichier bashrc

```bash
--8<-- "docs/files/bashrc"
```

### Accès au NAS

```bash
apt-get install gvfs-backends
apt-get install gvfs-fuse
apt-get install gigolo
```

> Thunar: GO -> Browse Network

### 'apt-get update' failed: exit code 100

root@proxmox:~# apt-get update
Get:1 http://security.debian.org bookworm-security InRelease [48.0 kB]
Hit:2 http://ftp.fr.debian.org/debian bookworm InRelease                             
Get:3 http://ftp.fr.debian.org/debian bookworm-updates InRelease [55.4 kB]           
Get:4 http://security.debian.org bookworm-security/main amd64 Packages [190 kB]
Get:5 http://security.debian.org bookworm-security/main Translation-en [116 kB]      
Err:6 https://enterprise.proxmox.com/debian/ceph-quincy bookworm InRelease           
  401  Unauthorized [IP: 51.91.38.34 443]
Err:7 https://enterprise.proxmox.com/debian/pve bookworm InRelease
  401  Unauthorized [IP: 51.91.38.34 443]
Reading package lists... Done
E: Failed to fetch https://enterprise.proxmox.com/debian/ceph-quincy/dists/bookworm/InRelease  401  Unauthorized [IP: 51.91.38.34 443]
E: The repository 'https://enterprise.proxmox.com/debian/ceph-quincy bookworm InRelease' is not signed.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
E: Failed to fetch https://enterprise.proxmox.com/debian/pve/dists/bookworm/InRelease  401  Unauthorized [IP: 51.91.38.34 443]
E: The repository 'https://enterprise.proxmox.com/debian/pve bookworm InRelease' is not signed.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
root@proxmox:~#

sudo nano /etc/apt/sources.list.d/pve-enterprise.list
vi /etc/apt/sources.list.d/ceph.list

as directed in this document. in order to comment out the enterprise repository deb https://enterprise.proxmox.com/debian/pve bullseye pve-enterprise
Saving the file and running sudo apt-get update solved the problems.