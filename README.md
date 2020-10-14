# Melopero_BME280_Arduino_Library

## How to use

First ypu need to include the library in your script and create a Melopero_BME280 object:

```C++
#include "Melopero_BME280.h"

Melopero_BME280 sensor;

void setup(){
    ...
```

### Settings

You can select one of three settings presets: weather monitoring, indoor navigation and gaming.

```C++
sensor.set_weather_monitoring_configuration();
sensor.set_indoor_navigation_configuration();
sensor.set_gaming_configuration();
```

Or you can specify your own settings:

```C++
// Set the Oversampling:
// To turn off a sensor (and not take measurements from that sensor)
// set the oversampling to BME280_NO_OVERSAMPLING
# The possible oversampling values are :
# BME280.OVERSAMPLING_1X
# BME280.OVERSAMPLING_2X
# BME280.OVERSAMPLING_4X
# BME280.OVERSAMPLING_8X
# BME280.OVERSAMPLING_16X
bme.set_oversampling(pressure_os, temperature_os, humidity_os):
