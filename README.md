# Welcome to WindowsOTK-Steam-Deck

A big problem I had when using Windows on the Steam Deck was the steamOS on-screen-keyboard (OSK) as this keyboard can be covered by windows start menu and some other programs. Steam does not allow you to change guide button chord config (It allows you to change but it doesn't save)

After trying to find a work around I found no answers and decided to make a work around myself and show you how to use it.

This tutorial will teach you how to change the on-screen-keyboard brought up by pressing the "steam" + "x" buttons

### NEW FEATURES
-Added "steam" + "Y" which will press f11, This can help with getting some apps in and out of fullscreen mode.

-Added "steam" + "A" which will press Alt + f4, as steams "exit application" does not work in some cases.

-Added "steam" + "menu" (pause button) which will press Windows + D. an easy way to access Desktop if you are stuck in an app for any reason.

## Using custom config

### Step 1
First I would recommend changing your OSK to the touch keyboard, you can find a quick guide (and guides to many other tweaks for Steam Deck Windows) over at [baldsealion's Steamdeck Ultimate Windows11 Guide](https://github.com/baldsealion/Steamdeck-Ultimate-Windows11-Guide/wiki/1.2-Windows-OS-Tweaks#replace-on-screen-keyboard-with-touch-keyboard)

### Step 2
[Download my custom config from this repo](https://github.com/prey-io/WindowsOTK-Steam-Deck/archive/refs/heads/main.zip)

### Step 3
Open Steam go to "Settings" -> "Interface" and turn off "Run steam when my computer starts" don't worry, it will still launch when you boot after following this guide

### Step 4
Close Steam and Open your Steam Directory,

(If you cant find it type "Steam" in Windows Search, Right Click and "Open File Location" this should bring you to a Shortcut for steam in Start Menu folder, Right click this shortcut and again click "Open File Location")

### Step 5
Open the folder named "controller_base" and drag "chord_neptune.vdf" from [my custom config](https://github.com/prey-io/WindowsOTK-Steam-Deck/archive/refs/heads/main.zip) in.

### Step 6
Steam will revert your changes on launch, but we can work around this

Type "Steam" in Windows Search and "Open file location", This should bring you to your Start Menu Programs, Right click the steam shortcut and click "Properties", In the "target" box you want to add `-noverifyfiles` after so it should look like `"C:\Program Files (x86)\Steam\steam.exe" -noverifyfiles`

(Steam has a tendency to revert this change also, you can prevent this by changing the file to "Read-only" in the "General" tab

### Step 7
Now to boot steam on launch,
Press Windows + R to open "Run" and type 

`shell:startup` for steam to start **only** on your **current user**

`shell:common startup` for steam to start on **all users**

Copy the shortcut you just made in the Start Menu folder into this folder and there you go!

You can now Re-Launch steam and pressing "steam" + "x" on your deck should open windows touch keyboard instead of steams keyboard.


_Note: If your Steam Keyboard still appears sometimes, it is part of your desktop controller configuration which can be changed easily with no tweaks_
