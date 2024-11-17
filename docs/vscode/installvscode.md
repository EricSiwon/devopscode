# Installing Visual Studio Code

## Installing package

### curl

```bash
$ su -
# apt-get install curl
```

## Installing VsCode via apt

> The proprietary repository and key can also be installed manually with the following script:

```bash
curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
sudo install -o root -g root -m 644 microsoft.gpg /etc/apt/keyrings/microsoft-archive-keyring.gpg
sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/microsoft-archive-keyring.gpg] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'
```

!!! note
    root@debiandesktop:~# curl https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg  
      % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current  
                                     Dload  Upload   Total   Spent    Left  Speed  
    100   983  100   983    0     0  18848      0 --:--:-- --:--:-- --:--:-- 19274  
    root@debiandesktop:~# sudo install -o root -g root -m 644 microsoft.gpg /etc/apt/keyrings/microsoft-archive-keyring.gpg  
    root@debiandesktop:~# sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/microsoft-archive-keyring.gpg] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/    vscode.list'


> Then update the package cache and install the package using:

```bash
sudo apt-get update
sudo apt-get install code # or code-insiders
```