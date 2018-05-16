---
title: '3. Install the Alexa Voice Service SDK'


layout: nil
---

On your laptop's TeraTerm console, navigate to the Alexa_SDK/Scripts directory to run the **setCredentials.sh** script:

`
cd Alexa_SDK/Scripts
./setCredentials.sh`


You'll be prompted for your AVS Credentials next - this includes your Product ID (no spaces!) and Client ID.  Copy and paste these numbers from your Developer Portal Product Profile that you created in the previous step.  Ensure you don't accidentally copy an extra space, or miss a character!

**Important note:**  you need to pick the Client ID you created in the Security Profile tab - don't use the one at the top of the product page!

![WrongClientID](assets/ClientIDfail.png)

You need to pick the ClientID you created for Code-Based Linking, in the Other Devices and Platforms section.

![CBL_ID](assets/NXPCBL.png)


You'll be prompted for your choice of locale, then you should be ready to build.

![AppBuilt](assets/AppBuilt.PNG)

{:.verify}
### Checkpoint 5

1. Sample app shows 100% Built success message
  
