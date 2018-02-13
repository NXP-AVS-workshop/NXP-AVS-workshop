---
title: '5. Run Unit Test'


layout: nil
---
This assumes the build on your device is located in the directory /avs-sdk-client.

#### Unit Tests

Go to the terminal window, and run the following steps to execute the series of Unit tests on your prototype.  

`cd /Alexa_SDK/avs-sdk-client
make all test`

![test_start](/assets/teststart.PNG)

For this workshop, tests have been pre-built to save time.  If you have your earbuds or speakers in, you'll hear Alexa run through a series of audio tests as well as functional tests.

![test_pass](/assets/testPassed.PNG)

Your test status should show success, with 100% of tests passed.  As a developer, any time you modify your client's on-device software, you should run **Unit Test** to ensure nothing was unintentionally broken.  Now you're ready to launch your client!


