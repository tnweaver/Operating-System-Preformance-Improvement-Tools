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

Idk what else to add I am just going to add scripts or tools that others and I use making a huge collection of work for each operating system...



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


## Linux
### Description
This will be the Linux Section and it will very depending on the flavor of linux you are using as well as the kernal.
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
Now when you restart the ```powertop.service will autostart with the --auto-tune syntax 

### 2. TBC
### Description








## MacOS (Unix Variant)
### TLDR: Use my 'Perfect Mac Install Every Time' Github page I will mainly update it there.
### [https://github.com/tnweaver/PMIE]