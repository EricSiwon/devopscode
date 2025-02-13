# Xcfe Xrdp

cat /etc/os-release

For CentOS 8:
sudo yum install -y epel-release

For RHEL 8:
sudo yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm

Installing the Gnome Desktop:
xrdp requires a desktop environment to connect to. Install the Gnome desktop using the following command:
sudo yum groupinstall -y “Server with GUI” ....

sudo yum install -y tigervnc-server xrdp ....

Starting xrdp Service: Start the xrdp server service using:

sudo systemctl start xrdp

Verify that xrdp is listening on port 3389:

sudo netstat -antup | grep xrdp

Enabling xrdp Service on Boot:

sudo systemctl enable xrdp

Firewall Configuration:
sudo firewall-cmd --permanent --add-port=3389/tcp && sudo firewall-cmd --reload

sudo firewall-cmd --list-all

-----
sudo dnf group list | grep -i xfce

sudo dnf groupinstall "Xfce" "base-x"

sudo echo "exec /usr/bin/xfce4-session" >> ~/.xinitrc

-----
