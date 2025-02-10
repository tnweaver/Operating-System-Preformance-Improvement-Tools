# Operating-System-Preformance-Improvement-Tools
## Project Overview
This will be a collection of Different operating system preformance tools (Some created by me and others not) that I reccomend to use for post OS installation.


**Disclamer!!!** This is just a personal project page that if it is of use to others than good! If not than thats fine too! I will really only update this when I get the chance to as I have a full time job and this is just one of many passion projects.
- If you like this one you can check out the other simple project that I make and post on Github!

### Main features:
Support for the main different types of OS

Types of operating systems:
- Mac 
- Windows
- Linux

Idk what else to add I am just going to add scripts or tools that others and I use making a huge collection of work for each operating system... (mainly just windows)


## Windows
### Description
This is the Best support tools I have found for preformance improvement when it comes to Windows 10/11+ (Depending on support)
### [Discalmer] I will try my best to link/refrence the origional creator, so if you see errors or issues please let me know I am willing to change anything on this page. 
- There is no order to this (best to worst) this is just a list of tools in no certian order. 
### 1. UnattendedWinstall by Memory
### Description:
This is a creation tool that can make personalized unattened answer files that help automatically debloading windows and is created and supported by Memory. 
### You can find the Github install here:
### [https://github.com/memstechtips/UnattendedWinstall]


### 2. Winhance by Memory
### Description:
This is a new one that I personally think is the best polished when it comes to long term support of the windows 10/11 OS. I really like the UI Design and the ease of use and that it is made by Memory
### You can find the Github install here:
### [https://github.com/memstechtips/Winhance]

### 3. The Ultimate Windows Utility by Chris Titus
### Description:
This Is a tool that Chris Titus has been working on for years, and I personally first started using it for windows 10 and now its mainly expanded to windows 11+. A very good tool and really you only need one command line to download and run the tool as long as you launch a powershell as an administrator.
### You can find the Website Guide here:
### [https://christitus.com/windows-tool/]
### The command is here if you dont want to go check out his website:
```bash
iwr -useb https://christitus.com/win | iex
```


## Linux
### Description
This will be the Linux Section and it will very depending on the flavor of linux you are using as well as the kernal. For the most part most good linux distros come pretty well tuned. for the most part if you have many problems most of them dont really apply to any kernel. The main reason for this section is for power preformance as the most popular software to run on servers is linux. This includes hypervisors (VMware ESXI/Proxmox/Red Hat Virtualization).
- **Warning!!!** All of the commands are shown from a Ubuntu Flavors/Kernel Example.


### 1. Powertop
### Description:


Install Process:

First Install Powertop onto the device.

```Bash
sudo apt install powertop -y 
```
To run the service you can use:
```bash
powertop
```
or 
```bash
sudo powertop
```

My perfered way of using powertop is to use it with the ```--auto-tune``` syntax added allowing the service to automaticly tune the parts of the computer making it more power efficient. 

Currently everytime that the OS starts the powertop service wont auto start so we will need to create a new service that makes it autostart.

First You will need to create and edit the ```powertop.service``` 
```bash
nano /etc/systemd/system/powertop.service
```
Then once you have used the command and editing the ```powertop.service``` with nano copy this over, save and exit.
```bash
[Unit]
Description=PowerTOP auto-tuning

[Service]
Type=oneshot
ExecStart=/usr/sbin/powertop --auto-tune

[Install]
WantedBy=multi-user.target
```

Then Enable the ```powertop.service```
```bash
systemctl enable powertop.service
```
Now when you restart the ```powertop.service``` will autostart with the --auto-tune syntax 







## MacOS (Unix Variant)
### TLDR: Use my 'Perfect Mac Install Every Time' Github page I will mainly update it there.
### [https://github.com/tnweaver/PMIE]