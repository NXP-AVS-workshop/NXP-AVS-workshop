---
title: '6. Launch the Client'

layout: nil
---


The sample application is in the folder */Alexa_SDK/avs-sdk-client/SampleApp/src/*. In order to start it, just input the following command:

'cd ~/Alexa_SDK/avs-sdk-client/SampleApp/src/
TZ=UTC ./SampleApp ../../Integration/AlexaClientSDKConfig.json 
../../Integration/inputs/SensoryModels/ DEBUG9'

You can see that it is starting with the highest debug level, **DEBUG9**.  This will display status messages in the console as you communicate with Alexa.  If you want to reduce output, simply change that to a lower number or remove it altogether. For starters, try it at the highest level so you can see what is going on behind the scenes.

You should see the following screen indicating that the Sample App is ready for interaction:

![app launched](../assets/app_launched.png)  **UPDATE**

{:.verify}
### Checkpoint 9

Say "Alexa" into the microphone array on your Synaptics 2-Mic dev kit to trigger the **Wake Word Engine**.   You should see the console status change to **Listening**, indicating the wake word was recognized.  Then say "tell me a joke." If Alexa responds with **Thinking...**, then **Speaking**, congratulations!  You have a working prototype.  

![app running](../assets/app_running.png)

As you interact with your prototype, you should see a series of status changes annotated by your level of DEBUG set (DEBUG9 in this picture).  If you cannot hear Alexa's response, ensure your speaker/earbuds are turned on and plugged in to your Synaptics kit 3.5mm audio jack.  

If Alexa isn't responding or your Sample App appears stuck at a certain step (displaying error messages when you try to speak), just type "**s**" and hit return to stop that interaction.  You can also type "**q**" and hit return to exit from the Sample App.
