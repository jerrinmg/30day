# Day 3: ReInstallation Nightmare!

As Kali Linux OS that I had installed earlier was not functioning properly ( No wifi detetction of onboard Laptop WiFi card, No sound and some other issues ) so I decided to reinstall the OS. 

## A. Installing the OS on the system 

1) Download the OS, flash it using Rufus.
2) Load the OS onto a pendrive, boot it from the pendrive using BIOS bootloader order movement to put the USB at the top. 
3)Follow the installation guide or steps in the installer, 
4) Disk allocation: note as Ubuntu was already installed, you can share the home directory. But I still need the root ( / ) and ____ ( I forgot ). Swap area with a memory allocation = your current Ram Memory should be created.  I also allocated space as well as for Eifi?  I think it only needs 100 mb, I think I have done this by installing Ubuntu. This block of instruction is a bit unclear as I dont remember the exact steps I had done.
5) In the installation step, I was getting the error that I was not able to install the extra tools. ( later on I found out that this was one of the main reasons to install Kali, ie the preinstalled or to be preinstalled tools).
6) So to avoid the error, I had to opt to not install any of the tools. Later on I found out ( thanks to reddit ) the reason why the tools could not be installed was because of Windows Defender fiddling with the OS during the flashing stage using Rufus. Pesky Windows Defender! Next time Ill have to disable it for flashing.
7) So as a result, I had nothing but CLI as a result of the installation. Then I thought ah , I can just install a GUI, but unfortunately there was no internet. Kali was not detecting my laptop’s inbuilt wifi card.
8) Thankfully I had a wireless adapter, using that I was able to connect to the internet and download the various shenanigans, the GUI etc.
9) After nights of running command line commands by dredge typing, ( could not copy paste anything as there was no browser, no internet , no interface no nothing )I managed to get it working somehow.  
10) The inbuilt WiFi of the laptop is still not working by the way. Have to figure out a way to make it work. It works fine on Ubuntu though. [1]
11) Make Kali Look cool: This is discouraged by many people, as Kali is a tool and not a way to show off. But I did it anyway. Hyperland + Kali Linux
  ![image](https://github.com/jerrinmg/30day/assets/166682032/3acd2b8d-7cec-483b-8d95-a5799af16807)

## B.Fidning the tools 
1) First find out the tools you want, / the most used tools in Kali Linux

![image](https://github.com/jerrinmg/30day/assets/166682032/74ae71d6-7fa1-4554-98e6-a47e3078dcb1)
![image](https://github.com/jerrinmg/30day/assets/166682032/26023758-1a2d-4fe7-9508-747053ebed3f)
2) Precatuions ! Step 2) Okay before doing that  Ill have to find out if installing packages and tools reveals my ip and whether I need to proxychain or hide my steps before doing this. I was thinking of doing that as the next step, but I guess It  cant wait.
