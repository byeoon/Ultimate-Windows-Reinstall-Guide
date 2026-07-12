# Proper Windows Reinstallation Guide <a href='https://ko-fi.com/O5O6VWWOH' target='_blank'><img height='36' style='border:0px;height:36px;' src='https://storage.ko-fi.com/cdn/kofi5.png?v=6' alt='Buy Me a Coffee at ko-fi.com' /></a>
**This guide is still being updated! Please be patient. It was last updated on 6/10/25**

## Intro
This guide helps power users reconfigure a fresh system to squeeze out as much performance and user safety as possible. This is a guide made for Windows 11 but most parts are backwards comaptible. I personally do not use modded installations as they will always have random side effects such as not being able to use certain game launchers, core features being missing, and other things too. You can get the same, if not better performance just from following this guide. There was also [a video made by Eric Parker](https://www.youtube.com/watch?v=nyMHBKlNk9c&pp=ygUVZXJpYyBwYXJrZXIgbW9kZGVkIG9z) which talks about the usage & risks of modded installs more in detail.

### Index
Here is a short outline of the things that will be covered in this guide.
- 1. Pre-Installation
  - LTSC Edition
  - World Region (Not Recommended)
- 2. OOBE
    - Bypass Microsoft Account Requirements
    - Force Local Account
- 3. Post-OOBE
   - Tools to run
   - Optional QoL Software

## Pre-Installation
There are two different ways to install Windows, it depends on personal preference. Before installing anything new, make sure to backup all your files on an external drive. It is reccomended to install Windows onto an NVME for the best performance. I use [this NVME](https://sabrent.com/products/sb-rocket-nvme4-1tb) but it's up to personal preference. <sub>This NVME in particular went on sale on Amazon for $49.</sub>


### Enterprise LTSC
The direct downloads for LTSC versions can be found on [Massgrave's Website](https://massgrave.dev/windows_ltsc_links). Select the version and language that you prefer. The direct links are no longer available as they aren't hosted on the website, but instead direct you to a download link. Since these are ISO files, you will need to burn it to a flash drive. I recommend using [Rufus](https://rufus.com) to do that. Enterprise LTSC is the best way to install as it removes additional bloat from your system and is overall more stable. LTSC does not get as many updates because it is meant for businesses who need a reliable version of Windows (think of IoT devices).

### English (World) (Not Reccomended!)
Before installing Windows (10/11) while you are still in the media creation tool, set your region to American (World). If you do not see the option in the media tool, you will have to do that in the setup itself (image below).  This removes any 3rd party applications and bloat that Windows tries to install on start such as Candy Crush, TikTok, and Solitare. **Some services like the Microsoft Store, the clock, and other core functions have been reported to be broken on some installations**. If you don't care about those potential risks you can continue using World.

<img src="https://github.com/user-attachments/assets/13342b8b-4fa7-439f-aa45-d8b067c760b8" height="480px" width="480px">

## OOBE

### Local Account Setup
In recent Windows feature updates, Microsoft forces you to have an online account and setup the computer strictly online, despite that people have found ways around it. Currently, the easiest way as of Windows 11 24H2 is to run a bypass command in the developer console. **Press <kbd>CTRL</kbd> + <kbd>SHIFT</kbd> + <kbd>J</kbd> to open the developer console** and then run `WinJS.Application.restart("ms-chx://LOCALONLY")`. You will now skip to the local account dialogue. Enter your desired username and password and proceed with the setup like normal. Microsoft may also patch this at anytime, and I have not tested it in a while. Feel free to make an issue on the GitHub page if this no long erworks.

Make sure to turn off all of the boxes for Microsoft to collect your data, or switch them to minimal data collection. Don't worry as once we reach the desktop we can completely get rid of telemetry. Once all of that is done, you should finally be at the desktop!

## Post-OOBE
There are a few tools and commands that you should run and install first. This part is where everyone might forget to do or get stuck on. The first thing that I made sure to download was [O&O ShutUp 10++](https://www.oo-software.com/en/shutup10), [Remove MS Edge](https://github.com/ShadowWhisperer/Remove-MS-Edge), [Microsoft Activation Scripts](https://massgrave.dev/) (optional), and [Chris Titus Winutils](https://github.com/ChrisTitusTech/winutil). All of these play a crucial role in fine tuning your new Windows experience. If you want to tweak these yourself, skip to the next category. 

### O&O ShutUp 10++
If you want to use my configuration file, it's in the repository and [you can download it here](https://github.com/byeoon/Proper-Windows-Reinstall/blob/master/Byeoon%20OOSU10%20Config.cfg). To apply the changes, go to `File > Import Settings` and then select the config file you just downloaded. This removes all telemetry and additional system tracking. Feel free to adjust it to your own liking. 

### Optional Quality of Life Software
There are some other tools that may help you adjust Windows to your liking. [Winaero Tweaker](https://winaero.com) is one that I personally use on every reinstall because it has a bunch of customizable features and useful settings such as verbose logon messages and adding custom items to the context menu. Another nice quality of life customization tool that I use is *Temp*

#### Customization / Themes

##### StartAllBack
Personally, I like this tool as it brings back the old taskbar and start menu. [You can download it here](https://www.startallback.com/) and configure it to your liking. Keep in mind it has a 90 day trial period, but it works similar to WinRar as it won't stop you from using the tool but remind you to get a license key and replace the background of the start menu with a frowny face. It's only $4 for one PC so I would recommend buying it and supporting the devs.





