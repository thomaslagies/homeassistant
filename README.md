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

### Aeotec WallMote Quad

[WallMote Quad from Amazon](https://www.amazon.de/gp/product/B017DV4C34/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)

The wallmote is used to trigger:

 - heating on/off
 - laundry timer
 - living room light on/off
 
### Aeotec Light Bulb

[Light Bulb from Amazon](https://www.amazon.de/gp/product/B07H9WBHJJ/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1)

Extremly bright Z-Wave Plus compatible light bulb. 

