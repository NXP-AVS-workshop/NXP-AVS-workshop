---
title: '3. Install the Alexa Voice Service SDK'


layout: nil
---

On your laptop's TeraTerm console, navigate to the Alexa_SDK directory to run the **SetupAVS.sh** script:

`
cd Alexa_SDK
./setupAVS.sh`

![SetupAVS](assets/SetupAVS.PNG)

You'll be prompted to proceed through the Sensory Wake Word license agreement.  Hit enter to scroll through the EULA and type "yes" to accept the agreement.

After accepting, you should see the Sample App build.  This can take some time - for purposes of this workshop, portions have been prebuilt to get you up and running faster.

Once the Sample App finishes, you should be prompted for your AVS Credentials next - this includes your Product ID (no spaces!), Client ID, and Client Secret.  Copy and paste these numbers from your Developer Portal Product Profile that you created in the previous step.  Ensure you don't accidentally copy an extra space, or miss a character!

You'll be prompted for your choice of locale, then you should be ready to build.

![AppBuilt](assets/AppBuilt.PNG)

{:.verify}
### Checkpoint 5

1. Sample app shows 100% Built success message
2. ProductID is entered as NXP-Prototype, and Client ID/Client Secret are entered and confirmed  
