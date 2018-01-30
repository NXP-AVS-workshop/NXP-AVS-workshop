---
title: '1. Set up your Hardware '


layout: nil
---


Let's begin by setting up the NXP Pico-Pi-IMX7D and Synaptics AudioSmart 2-Mic Development Kit. 

--- add some stuff here about how great the pico pi is (Resources etc) ---

{:.steps}
### Get your laptop ready for the workshop

1. You'll need a serial console (Putty, Tera Term etc) to access the PicoPi.  We recommend Tera Term, if you don't already have it you can access a direct download link [here](https://osdn.net/dl/ttssh2/teraterm-4.97.exe).  
2. VNC Viewer is also needed to open web browsers on the device remotely.  You can get VNC Viewer [here](https://www.realvnc.com/en/connect/download/viewer/).


{:.steps}
### Assembling Your Dev Kit

![BlockDiagram](/assets/SetupBlock.PNG)

1. Plug in the USB connections, mic/speaker, and ethernet (if not using wifi) connections as shown in the above picture.  
2. Next, connect +5V power to the 2Mic Synaptics kit.
3. Last step should be powering up your NXP Pico-Pi board by installing the USB type C connector into the board.  You can just use your computer as a power source. 

Your full setup should look something like this:

![FullSetup](/assets/FullSetup.jpg)


{:.steps}
### Booting Your Pico-Pi with Serial Console

1. Your Pico-Pi comes pre-loaded with a Yocto Linux image - as a user, you only need to run the setup scripts to build and launch the Alexa sample app.  On your laptop, open a serial console (Putty or Tera Term) and select the right COM port for your Pico-Pi (whichever new COM port appears in the drop-down when you plug in the USB connection from the Pico-Pi).  Configure your serial console with the settings as shown:
![ConsoleConfig](/assets/ConsoleConfig.PNG)
2. Once the terminal opens, you'll be presented with a login.  Type 'root' to continue.
![Root](/assets/Root.PNG)
3. Set the date by typing './home/root/Alexa_SDK/Scripts/setUTCTime.sh' into the console.
4. Type 'alsamixer' to pull up the controls for your sound card.  Use the up arrow keys to set PCM output level of the USB Mixer up to 100 as shown below:
![AlsaMixer](/assets/AlsaMixer.PNG)


{:.verify}
### Checkpoint 1
1. Make sure you are able to TeraTerm into your PicoPi and access the volume controls.

