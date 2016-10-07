# FlightDesk
A constantly evolving setup for controlling Elite Dangerous using DIY controllers for ultimate immersion.

# Software
 - Elite Dangerous (obviously)
 - Arduino
   - [Custom firmware](http://mitchtech.net/arduino-usb-hid-keyboard/) to allow it take act as a USB HID device
 - [OnTopReplica](https://ontopreplica.codeplex.com/) to allow mirroring of certain sections of screens and other screens
 - [PowerGrid](http://www.roccat.org/en-US/Products/Gaming-Software/Power-Grid/Home/) for Android App Control
 - [Google Play Music Desktop Player](https://www.googleplaymusicdesktopplayer.com/) for custom music
 - [SCP Toolkit](https://github.com/nefarius/ScpToolkit) for utilizing PS3 controller as Xbox Controller on PC
 
# Hardware
 - PS3 Controller
 - Arduino

# Inspiration
 - [Simpit](https://www.simplicate.info/tag/joystick/), just holy shit look at this!
 
# Overall Plan
 1.) I want to setup a custom built controller with switches and buttons with pretty LEDs and stuff that can be multi-pupose.
 2.) Would like to replicate the in-game cockpit as much as possible
 3.) Eventually probably replace the gamepad with a joystick and throttle control but I may not because I really like the gamepad.  Not sure if I would like a joystick as much.  Would be nice to have a spare hand.
 
 # Notes
  - the keypresses will be sent by the Arduino using the method described below:
    - [x] Test that [this](http://mitchtech.net/arduino-usb-hid-keyboard/) works
    - [ ] Make custom program for which buttons send which keypresses
    - [ ] Implement LEDs as well for indication
    - [ ] Figure out how to show status of current instruments with LEDs?
  - Setup second monitor to show status of things
    - This can be accomplished by mirroring in-game stuff (just for asthetics) with OnTopReplica
    - This can show stuff that's not in-game in smaller windows with OnTopReplica
    - Data on the second monitor should be maximized and resized automatically with button-pushes on the Arduino preferably
      - OnTopReplica(OTR) can be controlled via command-line (see ontopreplica.exe --help for details)
      - To get the Window ID & Title use this command in PowerShell:  
      `Get-Process |where {$_.mainWindowTItle} |format-table id,name,mainwindowtitle –AutoSize`
      - Still need to figure out how to close an OTR window after it's been opened so that button pushes can basically take small thumb-nails of windows and maximize them as needed.  (For example: have all of the different windows in small boxes across the screen but by pushing a button it brings up any of those windows in a full screen view on the second monitor.  While this could be done with a mouse right-click it'd be way cooler if the mouse wasn't necessary.
      
