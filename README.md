# My personal homeassistant configuration (no plugins needed)

## Heating

The flat is completly automated in terms of heating.

- Someone opened a window/door? -> Turn all heating off.
- No ones home? -> Turn all heating off.
- Just arrived at home? -> Wait some time (e.g. for ventilating after arrival) turn heating on.
- Cold? -> Trigger a heating boost for some minutes.
- Night reduction? -> Disable all heating automations between 23:00 and 07:00.

## Hardware

### Raspberry Pi 3B

Hosts homeassistant.

### Aeotec Z-Wave Stick

[Z-Wave Stick from Amazon](https://www.amazon.de/gp/product/B00YETCNOE/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)

In order to use them together with homeassistant, you need to have a compatible z-wave stick for your raspberry pi.
It plugs in via USB and has an easy to use pairing button.

[Manual](https://www.generationrobots.com/media/AeonLabsZwaveZstickS2/Aeon-Labs-Controleur-Z-wave-Z-stick-S2-user-manual.pdf)

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

### Aeotec WallMote Quad

[WallMote Quad from Amazon](https://www.amazon.de/gp/product/B017DV4C34/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)

The wallmote is used to trigger:

 - heating on/off
 - laundry timer
 - living room light on/off
 
### Aeotec Light Bulb

[Light Bulb from Amazon](https://www.amazon.de/gp/product/B07H9WBHJJ/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)

Extremly bright Z-Wave Plus compatible light bulb. 

