### These are the steps to install Docker on Windows 10 Home ###

- I noticed that when I installed Docker, it did not run as it said I needed to run 
virtualization in the BIOS. Here are the steps I took to allow it to run on my computer.
This solution may not work for everyone but it helped solve mine ane may be helpful for you too.

### Steps to get Docker on Windows 10 home: ###

1. Go to the Microsoft store and install Ubuntu 20.04 and set a username and password.
2. Install WSL x 64 (windows subsystem for Linux)
3. Go to “Turn windows features on or off” and check off Windows Hypervisor platform, Virtual machine platform, and Windows subsystem for Linux (enable them)
(Enabling virtualization through BIOS): Go to settings > update & security > recovery > Advanced startup > restart now > (when restarted) > go to troubleshoot > (using up, down, right, left keys and enter to confirm) > advanced options > UEFI firmware settings (restart) > (when booted) > press f10 > system configuration > virtualization technology >  (default: disabled) > enable it (enabled)> f10 to save & exit (virtualization is now enabled!)
4. Open Ubuntu 20.04 and set wsl2 as default with these following commands (wsl -l -v: to check which version wsl is running, if 1, change to 2)(to change, use: wsl —set-version Ubuntu-20.04 2 or wsl —set-default-version 2) 
5. Download and install docker desktop 
Run it and it should work! (Also make sure when you run the app, go to general > resources > wsl integration > make sure enable integration with my default wsl distribution is checked (then you should be all set to use Docker on Window 10 Home!)


** Jenkins: cmd or ubuntu terminal: docker pull jenkins** (to get Jenkins container)


### Enabled virtualization through BIOS (Basic Input Output System) 

(Go to settings) > go to update and security > go to recovery settings > advanced tab and select restart > select f10 to open bios settings and go to system config)

Credits: 
https://2nwiki.2n.cz/pages/viewpage.action?pageId=75202968
Docker on HP: https://thewebspark.com/2019/04/02/how-to-enable-virtualization-in-bios-of-windows-10-home-hp-systems-solved/amp/
WSL & Docker: https://youtu.be/5RQbdMn04Oc

