ESPHome component to monitor a Jikong Battery Management System (JK-BMS) via UART-TTL, display the data on the OLED display and send it via mqtt.
Heavily inspired by the https://github.com/syssi/esphome-jk-bms.

Uses "TTGO T-Display ESP32 CP2104" which is powered up from the step down dc-dc converter XL7015A. This allows the module to be powered up directly from the battery (up to 80V dc).
Connects to the JKBMS RS485 port via Micro JST 1.25 4 Pin female plug.

I assembled both modules on the universal PCB with two terminal blocks for ease of connecting it to the bms and battery (power).
My setup:

![20231028_203130](https://github.com/ostry81k/JKBMS_TTGO_mqtt/assets/139721177/ce402db5-0991-4ed7-8742-9e2d918d635d)

The built in UP and DOWN buttons allow for scrolling between the displayed pages.

I display the received data in the Home Assistant screen:
![homeassistant](https://github.com/ostry81k/JKBMS_TTGO_mqtt/assets/139721177/4dd631a7-fb0e-41c5-a7c1-dfb6dcf178f8)

From there can be exported to InfluxDB and passed to Grafana:
<dashboard TBD>
