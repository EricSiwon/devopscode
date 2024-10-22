
# Configuration de base

## Depuis une installation serveur avec Apache et SSH

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

### Mise à jour du system

```bash
apt-get update
apt-get dist-upgrade

dpkg --list
```

### Installation python

```bash
apt install python3.11-venv
 
python3 -m venv myvenv

source ./myvenv/bin/activate
```

### Confib .Bashrc

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