# SmartPID

## What is SmartPID?

**SmartPID** is a powerful and flexible controller for complete **brewing process automation** and recipe management as well **fermentation temperature control**. SmartPID is wifi connected for data logging and remote process control via web and mobile

## Get SmartPID

SmartPID can be bought [directly here](http://smartpid.com/store/). After integration is released, a one year pre-paid code of Brewfather Premium is included with new sales.

## Integration features

**Smart Hombrewing Application**

* Remote monitor of process parameters \(set point, current temperature, PID out, pump status, timers
* Process events notification and alarms
* Remote actions \(process start/stop pause/resume, set point change, power change, pump start/auto/stop
* Recipe definition and upload for execution

**Smart Thermostat**

* Remote monitor of process parameters \(set point, current temperature, PID out, timers\)
* Process events notification and alarms
* Remote actions \(process start/stop pause/resume, set point change,\)
* Fermentation profile definition and upload

## Firmware Pre-Requirements

In order to use the integration a specific firwmare level is needed on SmartPID 

Both classic DIN box controller \(STC version\) and the new CUBE version are fully compatible.

**Smart Homebrewing ⇒ version 1.3-010 +**

**Smart Thermostat ⇒ version 0.5-014 +**

Download the FW from the [SmartPID wiki page](http://smartpid.com/wiki/doku.php?id=sw_release) on the web site and upgrade. Click here for [upgrade instructions on video](https://youtu.be/RnQzNxVUHeo).

#### Upgrade mini guide

1. [Download ](http://smartpid.com/wiki/doku.php?id=sw_release)firmware from SmartPID
2. Unzip the .bin file
3. Rename .bin file to **flash.bin** before copying it to SmartPID
4. Attach SmartPID to computer via USB **while** holding the **RED** button
5. Delete **FLASH.BIN** from the SmartPID storage device that has now appeared
6. **Copy** new **flash.bin** to SmartPID storage device
7. Safetly detach device after copy has finished
8. Verify that upgrade is ok by checking firmware version in the info menu

## Enable SmartPID integration

![Enable SmartPID in the Settings page in the Power-ups Section](../.gitbook/assets/image%20%2849%29.png)

## Configure SmartPID

![Open the Devices page in the new menu option that appears](../.gitbook/assets/image%20%2862%29.png)

## Register/Login to SmartPID account

In the devices page there will now be a **Configure** button next to the SmartPID section. Click it to set up SmartPID.

![Enter your e-mail and password, then login or register](../.gitbook/assets/image%20%2839%29.png)

### Register new SmartPID account \(new SmartPID users\)

Enter your wanted e-mail and password then click Register. If registration is successful you will be logged in to the new account automatically. _**Warning: SmartPID Password is not encrypted and is stored in plain text**._

You can also register a new account in the SmartPID android app.

### Login to existing SmartPID account \(existing SmartPID users\)

If you already have a SmartPID account. Enter your e-mail and password then click Register. If registration is successful you will be logged in to the new account automatically. _**Warning: SmartPID Password is not encrypted and is stored in plain text**._

## SmartPID device setup

Your SmartPID needs to be set up with wifi connection and the login for your SmartPID account.

For instructions on how to set up your SmartPID device for Wifi and MQTT server connection please check the [guide here](http://smartpid.com/wiki/doku.php?id=demo_tutorials).

## Register SmartPID device



![Configure SmartPID device](../.gitbook/assets/image%20%2836%29.png)

1. From the SmartPID configuration window click **Add device**
2. Insert a name for your smartPID controller
3. Select the proper application \(homebrewing / thermostat\). This must be compatible with the firmware on your SmartPID
4. Enter the 12 characters serial number found in the SmartPID info menu
5. Enable **Channel 1** and/or **Channel 2**, optionally name the Channel\(s\).
6. **Save** to add to your device list
7. When you click Save the device will appear, and Brewfather will communicate with your SmartPID via MQTT messages

## Mode: Homebrewing

![Homebrewing Panel](../.gitbook/assets/image%20%2828%29.png)

### Recipe upload and process start

1. Go to **Batches page** - **Brewing** tab
2. Click on the **Start** button in the **Brew Controller** section
3. Select your homebrewing controller from the list
4. Flag the proper options and press start to push the recipe to SmartPID controller and eventually start the recipe execution.

{% hint style="info" %}
Recipe is saved always in **position 1** in the controller and will override any recipe entered manually in that position
{% endhint %}

![Start a recipe from the batch page](../.gitbook/assets/image%20%2875%29.png)

![Start Homebrewing SmartPID](../.gitbook/assets/image%20%2820%29.png)

### 

#### Optional Mash Steps Template

If you want one to one mapping of the mahing steps to the recipe format of the SmartPID you can utilize the **Mash steps template** mashing profile.

![](../.gitbook/assets/image%20%2840%29.png)

1. Select profile in recipe

![](../.gitbook/assets/image%20%2858%29.png)

2. Alter the profile by adjusting time and temperature on the steps with time greater than 0. Leave the rest as is.

## Mode: Thermostat

![Thermostat Panel](../.gitbook/assets/image%20%2837%29.png)

### Start fermentation profile from recipe



1. Go to **Batches page** - **Fermentation** tab
2. Click on the **Start** button in the **Fermentation Controller** section
3. Select your thermostat controller from the list
4. Click **Start** to start the profile

Optionally you can also start a fermentation profile from the devices page.

{% hint style="info" %}
Profile is saved always in **position 1** in the controller and will override any profile entered manually in that position
{% endhint %}

![](../.gitbook/assets/image%20%2876%29.png)

![](../.gitbook/assets/image%20%2855%29.png)
