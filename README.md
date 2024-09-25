# WSL
How to install and use Windows Subsystem for Linux (WSL)

## Why use WSL
...

## How to install WSL
You can start by following this online guide from Microsoft: https://learn.microsoft.com/en-us/windows/wsl/install In short, you need administrative rights on your windows machine and then run a couple of commands using Powershell.

First check whether WSL is installed. Run wsl --install. If WSL is not already installed, instalation process will start and Ubuntu, the default Linux distribution, will be installed. Otherwise you will see the help text of WSL command printed.

WSL2: https://learn.microsoft.com/en-us/windows/wsl/install-manual#step-3---enable-virtual-machine-feature

In the case WSL is already present, just intall Ubuntu with: 

wsl --install -d Ubuntu-24.04

wsl --set-default-version 2

ø
