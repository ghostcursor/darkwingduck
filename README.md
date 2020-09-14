# darkwingduck
Give your Rubber Ducky Wings!

First of all huge thanks to Seytonic at seytonic.com. This project is largely based on his work on creating the "$3" USB Rubber Ducky. Head on over to https://seytonic.com to checkout his work. 

Also big thanks to Hak5 and their creation of the USB Rubbery Ducky. It's a game changer in pen testing. 

So I saw the Rubber Ducky and I saw the cheap way of making one and wanted to add my own touch to it and that's how I created the DARKWING DUCK (Such a cool show!). I wanted to expand the versatility of the device and give a pen tester relative remote control of the device. So I decided to add bluetooth functionality to it. This has some great advantages, and disadvantages. 

Skip the boring reading and watch the video:
https://www.youtube.com/watch?v=oh7TcU3XbuQ&

Advantages

1) You can run multiple scripts with a single device (Seytonic solved this problem with a dip switch). 

2) You can run multiple scripts in sequence. Instead of being limited to one single script per plugin you can keep hacking and hacking forever and ever.

3) You can edit the script on the go. 

Disadvantages

1) Slower than the initial Rubber Ducky. This is because you have to connect the ducky to the computer. Connect to it via bluetooth, then send the script. Plus the interpreter has a small delay to allow for bluetooth reading. This speed problem will always be inherent to the bluetooth mode but cases where speed is critical this issue will be solved with a slider switch allowing for stand-alone mode, also because it's Arduino based, you can use Seytonic's Ducky Script converter and make it stand alone anyways. You just have to reprogram it between missions.

2) Not all commands work. You can't do anything that saves data back to the ducky, and some commands aren't interpreted due to limitations of the keyboard.h library that comes with arduino.

3) Some scripts are too long. Testing is still ongoing, but some scripts are longer than the bluetooth buffer on the arduino. This will be solved however with programming in the application to break down longer scripts into smaller discrete packets, as well as increasing the buffer in the ARDUINO.

WHAT YOU NEED

TO PERFORM SAID HACKING

1. Arduino Pro Micro (or chinesium equivalent)

2. HC06 Bluetooth Module

3. USB Cable/OTG

4. Android Phone

TO DEVELOP SAID HACKING

1. Arduino IDE

2. MIT APP Inventor 2

FILES IN THIS REPOSITORY:

darkwingduck.ino (arduino script)

HardwareSerial.H (replace original in core libraries of arduino)

darkwingduck.aia (App Inventor Project File)

darkwingduck.apk (Completed Android App you can install on your phone)

THINGS TO DO:

Get saving working in the app (this is easy, I just have to do it).

Run tests seeing what the max length of a script is for certain.

Add arduino code to look for programming button press/stand-alone vs. bluetooth mode.

Add SD Card code per Seytonic's work.

