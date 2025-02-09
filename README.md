# Operating-System-Preformance-Improvement-Tools
## Operating System Preformance Improvement Tools
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

## MacOS (Unix Variant)
### TLDR: Use my 'Perfect Mac Install Every Time' Github page
### [https://github.com/tnweaver/PMIE]