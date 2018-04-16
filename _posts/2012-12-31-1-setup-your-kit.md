---
title: '1. Set up your Hardware '


layout: nil
---

### Introduction to your Workshop Hardware

The **Synaptics NXP 2Mic AVS Dev Kit** is the complete solution to expedite development of Alexa Home Products.  The kit consists of a **Synaptics AudioSmart™ 2-Mic Development Kit** for Amazon Alexa Voice Service (AVS) and a **PICO-PI-IMX7** development board with the **NXP i.MX 7D** processor.  The kit outputs a fully functioning Amazon AVS prototype that uses the Synaptics Kit as an audio front end, and the PICO-PI-IMX7 i.MX 7D development board as the processor handling wake word recognition and interface to Amazon’s AVS service. 

Let's begin by setting up the NXP Pico-Pi-IMX7D and Synaptics AudioSmart 2-Mic Development Kit. 


### Get Required Software

For this tutorial, you'll use your personal computer (PC/Mac/Linux) to configure and start the Alexa Voice Service client running on the Pico-Pi.

You'll need to use a serial console (Putty, Tera Term etc) to access the PicoPi.  We recommend **Tera Term**, you can access a direct download link [here](https://osdn.net/dl/ttssh2/teraterm-4.97.exe).  

**VNC Viewer** is also needed to open web browsers on the device remotely.  You can get VNC Viewer [here](https://www.realvnc.com/en/connect/download/viewer/).



### Assembling Your Dev Kit

![BlockDiagram](/assets/SetupBlock.PNG)

Plug in the USB connections, mic/speaker, and ethernet (if not using wifi) connections as shown in the above picture.  Next, connect +5V power to the 2Mic Synaptics kit.
Last step should be powering up your NXP Pico-Pi board by installing the USB type C connector into the board.  You can just use your computer as a power source. 

Your full setup should look something like this:

![FullSetup](/assets/FullSetup.jpg)



### Booting Your Pico-Pi with Serial Console

Your Pico-Pi comes pre-loaded with a Yocto Linux image - you only need to run the setup scripts to build and launch the Alexa sample app.  On your laptop, open a serial console (Putty or Tera Term) and select the right COM port for your Pico-Pi (whichever new COM port appears in the drop-down when you plug in the USB connection from the Pico-Pi).  Configure your serial console with the settings as shown:  (change baud rate to 115200)

![ConsoleConfig](/assets/ConsoleConfig.PNG)

Once the terminal opens, you'll be presented with a login.  Type "root" to continue.  If you don't see a prompt come up, try hitting "return" or power cycling the Pico-Pi by unplugging the USB-C cable.

![Root](/assets/Root.PNG)

Set the date by entering the following command into the console:  (if this doesn't work, you may need to load the workshop image onto your Pico-Pi)
`sudo bash /home/root/Alexa_SDK/Scripts/setUTCTime.sh` 

Type "alsamixer" into the terminal and hit return to pull up the controls for your sound card.  Make sure the I2S sound card is selected (Not audio-sgt15000). Use the up arrow keys to set PCM output level of the USB Mixer up to 100 and hit esc to exit.
![AlsaMixer](/assets/mixerv3.PNG)

Plug in ethernet or activate wi-fi by clicking in an antenna onto the micro-SMB connector on your NXP module and typing

`wifi_setup.sh "<SSID>" "<PW>"`

You can leave the password field blank if the connection is open.

Test your connection by typing `ping 4.2.2.2` and see if you're online!

### Load the AVS Tutorial Image onto your Pico-Pi - For Windows PC

**Your Pico-Pi should have the workshop's required image already loaded onto it.**  

Make sure the jumper J2 on your Pico-Pi is set to normal running position as shown below:

![JumperNormal](/assets/JumperNormal.PNG)


{:.verify}
### Checkpoint 1
1. Make sure you are able to TeraTerm into your PicoPi and access the I2S volume controls.
2. Crank it up to 100!
3. Check that you have the latest image by confirming Alexa-SDK folder is on your /root path.


