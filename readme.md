# WSL Ubuntu 20.04 Setup

This script will completely configure Ubuntu 20.04 in [WSL](https://docs.microsoft.com/en-us/windows/wsl/). It has only been tested on Ubuntu 20.04!

### Instructions

From Ubuntu, just clone and run `setup.sh`

```bash
cd ~
git clone https://github.com/kevinchatham/wsl-ubuntu-setup
chmod +x ~/wsl-ubuntu-setup/setup.sh
~/wsl-ubuntu-setup/setup.sh
```

### Resetting Ubuntu

Ubuntu can be reset with one of these commands.

For WSL v1: 
```batch
wslconfig /unregister Ubuntu && ubuntu
```

For WSL v2: 
```batch
wsl --unregister Ubuntu && ubuntu
```

### Install Ubuntu Without Microsoft Store

If you do not have access to the Microsoft Store, don't worry, Ubuntu can be manually installed. Please see [this documentation](https://docs.microsoft.com/en-us/windows/wsl/install-manual) (at Downloading Distributions) for more details. Note that you will need to install WSL first.

Manually Install Ubuntu 20.04 (using PowerShell):
```powershell
Invoke-WebRequest -Uri https://aka.ms/wslubuntu2004 -OutFile Ubuntu.appx -UseBasicParsing | Add-AppxPackage .\Ubuntu.appx
```
