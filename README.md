# My personal homeassistant configuration

## Hardware

### Raspberry Pi 4

Hosts homeassistant.

### Aeotec Z-Wave Stick

Note!

This stick does not work properly when it is connect directly to the pi 4.
You need to bridge in any kind of USB hub, otherwise you run into voltage issues while detecting the stick in `z-wave js`

![Z-Wave Stick](https://github.com/thomaslagies/homeassistant/blob/main/images/zwave_stick.jpg)

[Z-Wave Stick from Amazon](https://www.amazon.de/gp/product/B00YETCNOE/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)

In order to use them together with homeassistant, you need to have a compatible z-wave stick for your raspberry pi.
It plugs in via USB and has an easy to use pairing button.

[Manual](https://www.generationrobots.com/media/AeonLabsZwaveZstickS2/Aeon-Labs-Controleur-Z-wave-Z-stick-S2-user-manual.pdf)

[Factory Reset](https://aeotec.freshdesk.com/support/solutions/articles/6000121947-how-to-manually-factory-reset-z-stick-gen5-)

The Z-Stick operates in three distinct modes: Inclusion-Mode, Removal-Mode and SerialAPIMode. Both Inclusion-Mode and Removal-Mode require the Z-Stick to be unplugged from the
USB connector of the host, while SerialAPI-Mode requires that the Z-Stick to be plugged into
the USB connector of the host.
• Inclusion-Mode : Adding/Including Z-Wave Devices into the Z-Wave Network
1. To initiate Inclusion-Mode, unplug the Z-Stick from the USB connector and then tap the
button. (The LED will blink slowly.)
Note: While in Inclusion-Mode, the Z-Stick is in perpetual add/inclusion. There is no
need to press the button on the Z-Stick again to include each new device.
2. To include a new Z-Wave device into the network, simply go to the device with the ZStick and press the button on the device you wish to include. (The LED on the Z-Stick
will blink fast during a network neighbor discovery and stay solid for 3 seconds to
indicate successful inclusion of the device into the network.)
3. The LED will then return to blinking slowly, indicating readiness for further device
inclusions. Repeat step 2 for each device as you wish to include.
4. Tap the Z-Stick button to turn it off.
• Removal-Mode : Deleting/Removing/Excluding Z-Wave Devices from the Z-Wave Network
1. To initiate Removal-Mode, unplug the Z-Stick from the USB connector. Then press and
hold down the button for approximately 3 seconds. (The LED will transition from
blinking slowly to blinking fast.)
Note: While in Removal-Mode, the Z-Stick is in perpetual removal/exclusion where it
will remove Z-Wave devices from the networks they are currently paired to. There is no
need to press the button on the Z-Stick again to exclude each device.
2. To remove a Z-Wave device from the network, simply go to the device with the Z-Stick
and press the button on the device you wish to remove. (The LED on the Z-Stick will
immediately stay solid for 3 seconds to indicate successful removal from the network.)
3. The LED will then return to blinking fast, indicating readiness for further device
exclusions. Repeat step 2 for each device as you wish to exclude.
4. Tap the Z-Stick button to turn off. 

### Aeotec WallMote Quad (4 Button - 8 Inputs tap/hold)

![Z-Wave WallMote](https://github.com/thomaslagies/homeassistant/blob/main/images/zwave_wallmote.jpg)

[WallMote Quad from Amazon](https://www.amazon.de/gp/product/B017DV4C34/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)

The wallmote is used to trigger:

 - heating on/off
 - laundry timer
 - living room light on/off
 
 It is mounted to the wall via a magnetic plate. 
 Im looking for additional button actions, but currently 95% of my automations, well, run automaticly.
 
### Aeotec Light Bulb

![Z-Wave Light Bulb](https://github.com/thomaslagies/homeassistant/blob/main/images/zwave_led_bulb.jpg)

[Light Bulb from Amazon](https://www.amazon.de/gp/product/B07H9WBHJJ/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)

Extremly bright Z-Wave Plus compatible light bulb. 
Wide range of nice looking colors

#### How to reset?

To reset to factory settings, power the light on 6 times with 0.5-2.0s delay.

### Devolo Thermostat

![Z-Wave Thermostat](https://github.com/thomaslagies/homeassistant/blob/main/images/zwave_thermostat.jpg)

#### Own Experience

- How to install?
  There are two extensions for different valve types included. You may install them by sticking a flat head screwdriver into the slit in the battery compartment. 
  Then turn the thermostat until you can feel resistance.
  Now you are able to screw/unscrew the extensions from the thermostat
- How to mount/unmount to heater?
  Once the correct extension is in place, you may screw the whole thing with good pressure against the heaters thread.
  Again, make sure you have that 'click' so the internals wont turn instead.
  Now press the middle button for some seconds. 'M' will show on the display. Press the middle button again an the thermostat will press itself against the heater threads. It should not be lose afterwards.
  To unmount, repeat the same process. In the end the firm grip will losen and you are able to unscrew the thermostat.
- How to reset ZWAVE?
  Since this is not documented anywhere, this is what kinda worked for me.
  Remove one battery. Press and hold the middle button for 10 seconds while inserting the battery again. The thermostat will flash wildy, meaning the reset worked.

[Devolo Thermostat from Amazon](https://www.amazon.de/gp/product/B00M2JKABQ/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)

[Manual](http://manuals-backend.z-wave.info/make.php?lang=DE&sku=DEVE9356&cert=ZC08-15020003)

I use these thermostats since they are able to read current temperature. 
If the given threshold is reached, the thermostat will throttle itself until it holds the target temperature.

The thermostats are only used in automatic mode. 
Triggers are:
- presence of one of our smartphones in our network
- time schedules
- open/closed windows (see door sensors)

### Smart Things Door Sensor

![Z-Wave Door Sensor](https://github.com/thomaslagies/homeassistant/blob/main/images/zwave_door_sensor.jpg)

[Door Sensor from Amazon](https://www.amazon.de/gp/product/B07FMDR286/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)

[Manual](https://fccid.io/2AKXA-IM20ZWAVEUSA/Users-Manual/User-Manual-3307318)

Our flat has 5 windows/doors (Entrance Door has no sensor)
I currently only use 4 of these sensors, since one sensor is used at a double window.
Stick the "smart" part on the left window pane, and the "dumb" side on the right one.

Theses sensors worked a 100% of the time for me and control our heating scenes.
As soon as a window/door opens, the termostats will be throttled.
If all windows/doors are closed again, the heating scene is triggered.

Since the thermostats only pull every minute or so, there is a small delay in between an open window and a throtteling thermostat.
This might not be 100% efficient (you want to throttle it immediatly) but in our use case its okay.
We normaly air our flat for around 10-20 minutes, several times a day.

