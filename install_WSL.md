# WSL
In this document instructions are offered on how to install and use Windows Subsystem for Linux (WSL) on a Windows 10 machine. User is assumed to have administrative rights

## What is WSL
Windows Subsystem for Linux (WSL) is a feature of Microsoft Windows that allows developers to run a Linux environment without the need for a separate virtual machine or dual booting

## Why use WSL
It is often the case that software is either exclusively available on Linux platforms and not windows or that installing it on windows is difficult or imposible. 

## How to install WSL
You can start by following this online guide from Microsoft: https://learn.microsoft.com/en-us/windows/wsl/install In short, you need administrative rights on your windows machine and then run a couple of commands using Powershell.

First check whether WSL is installed. Run wsl --install. If WSL is not already installed, instalation process will start and Ubuntu, the default Linux distribution, will be installed. Otherwise you will see the help text of WSL command printed.

WSL2: https://learn.microsoft.com/en-us/windows/wsl/install-manual#step-3---enable-virtual-machine-feature

In the case WSL is already present, just intall Ubuntu with: 

wsl --install -d Ubuntu-24.04

wsl --set-default-version 2

### Fix possible internet connection issues

`sudo vim /etc/resolv.conf`

```
nameserver 10.14.4.44
nameserver 10.13.17.13
nameserver 1.1.1.1

search lumcnet.prod.intern prod.intern vpn.lumcnet.prod.intern
```

### Install pip
```
sudo apt-get update
```

```
sudo apt install python3-pip
```

### Install miniconda
Explain role of conda

#### Commands to intall conda
These four commands download the latest 64-bit version of the Linux installer, rename it to a shorter file name, silently install, and then delete the installer:
```
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm ~/miniconda3/miniconda.sh
```

After installing, initialize your newly-installed Miniconda. The following commands initialize for bash shell:
```
~/miniconda3/bin/conda init bash
``` 
From: https://docs.anaconda.com/miniconda/

### Install a more convenient terminal
[Windows terminal](https://learn.microsoft.com/en-us/windows/terminal/) is a host application for the command line shells, like Powershell and bash we have just install via WSL. You can install it using windows store, or through Powershell. Open Powershell and type: 
```
winget install --id Microsoft.WindowsTerminal -e
```

