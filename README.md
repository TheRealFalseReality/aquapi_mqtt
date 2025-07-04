# [AquaPi for ESPHome - MQTT](./)
<img src="/assets/image/AquaPi Logo Blue.png" alt="drawing" align="left" width="120"/>

The Aquarium meets the Smart Home!

**[Setup Guide](https://github.com/TheRealFalseReality/aquapi/wiki/Setup-AquaPi)**  
**[Build It Yourself](https://github.com/TheRealFalseReality/aquapi/wiki/Build-It-Yourself)**  
**[Wiki](https://github.com/TheRealFalseReality/aquapi/wiki)**  

**[Join the conversation on Reef2Reef!](https://www.reef2reef.com/threads/aquapi-an-open-souce-aquarium-controller.1033171/)**  

AquaPi for ESPHome is a project that helps you build a powerful aquarium monitoring and automation system using affordable [ESPHome](https://esphome.io/) devices and [Home Assistant](https://www.home-assistant.io/installation/).
Make endless automations and monitor temperature, water level, and upgrade for advanced aquarium monitoring: pH, salinity, dissolved oxygen, and more (using EZO circuits and probes).  

**# TODO:** 
* Make MQTT `is_connected` sensor
* Create `restart` automation when not connected to MQTT Server

Why use AquaPi?

- **Open-source**: Freely available for anyone to access, modify, and contribute to.
- **Modular**: Designed to be easily expanded and customized based on your specific needs.
- **Modernized**: Utilizes the latest technologies and tools for a seamless user experience.
- **Customizable**: Adapt the system to fit your unique aquarium setup and monitoring preferences.
- **Versatile**: Expand the system's capabilities with your own compatible sensors and equipment.
- **Affordable**: Offers a cost-effective alternative to many high-end monitoring solutions.
- **Powerful**: Provides comprehensive monitoring capabilities for various water parameters.

### **[Buy Now!](https://www.capitalcityaquatics.com/store/aquapi)**

## Demo
[**Try out the AquaPi Demo!**](https://www.capitalcityaquatics.com/store#storelivedemo)

<table>
  <tr>
    <td>
      <img src="assets/image/AquaPi+-+Transp.png" alt="aquapi"/>
    </td>
    <td>
      <img src="https://github.com/TheRealFalseReality/aquapi/assets/106857076/db50c972-2bbd-4c9f-9f62-fa6e62f41cf3" alt="PXL_20240224_022516268~2" width="1080"/>
    </td>
  </tr>
</table>

UI
| <img src="assets/image/Screenshot 2024-10-15 120850.png" alt="dashboard"/> | ![Screenshot 2024-02-22 001408](https://github.com/TheRealFalseReality/aquapi/assets/106857076/a430aabc-2c28-43e7-9779-3c5c04c4b7db)  |
| ------------- | ------------- |

## Hardware Used
**ESP32 devkit**  
**HomeAssistant** using a Raspberry Pi 3 or above. The more RAM, the better.  
**Prerequisite!!** A Raspberry Pi (or something similar) running HomeAssistant to communicate and interact with the ESP32 via `homeassistant.local:8123`.
Get [Raspberry Pi Imager](https://www.raspberrypi.com/software/)

### Sensors
***Temperature*** 
  - DS18B20 Waterproof Thermistor  
  
***Water Level - Optical*** 
  - 2 Food Grade Optical Infrared Water Liquid Sensors w/Magnetic Mount
    
***Water Leak Sensor***
  - Liquid Detection Sensor, 6ft Cable, 2 Mounting Screws w/Magnetic Mount
  
**pH:** *Atlas Scientific pH: [EZO-pH](https://files.atlas-scientific.com/pH_EZO_Datasheet.pdf) & [Lab Grade pH Probe](https://files.atlas-scientific.com/pH_probe.pdf)*  
  - EZO™ pH Circuit, ISO 10523 Compliant  
  - Double junction silver / silver chloride Lab Grade pH Probe with Vanadium III, Gen 3
  - Electrically Isolated EZO™ Carrier Board
  - Range: 0 - 14
  - Time Before Recalibration: 1 Year
  - Life Expectancy: ~2.5+ Years

**Salinity:** *Atlas Scientific Conductivity: [EZO-EC](https://files.atlas-scientific.com/EC_EZO_Datasheet.pdf) & [Conductivity Probe K 1.0](https://files.atlas-scientific.com/EC_K_1.0_probe.pdf)*  
  - EZO™ EC Circuit, ISO 7888 Compliant  
  - Conductivity Probe K 1.0, Graphite, Gen 3
  - Electrically Isolated EZO™ Carrier Board
  - Range: 0.07 − 500,000+ μS/cm
  - Time Before Recalibration: ~10 Years
  - Life Expectancy: ~10 Years
    
**Dissolved Oxygen:** *Atlas Scientific DO: [EZO-DO](https://files.atlas-scientific.com/DO_EZO_Datasheet.pdf) & [Dissolved Oxygen Probe](https://files.atlas-scientific.com/LG_DO_probe.pdf)*  
  - EZO™ DO Embedded Circuit  
  - Range: 0.00 - 100 mg/L (0 - 350% saturation)
  - Life Expectancy: ~4 Years
    
**ORP:** *Atlas Scientific ORP: [EZO-ORP](https://files.atlas-scientific.com/ORP_EZO_Datasheet.pdf) & [ORP Probe](https://files.atlas-scientific.com/orp_probe.pdf)*  
  - EZO™ ORP Embedded Circuit  
  - Range: -2000mV - 2000 mV
  - Life Expectancy: ~2 Years

**Peristaltic Dosing Pump:** *Atlas Scientific Pump: [EZO-PMP](https://files.atlas-scientific.com/EZO_PMP_Datasheet.pdf)*  
  - EZO™ Pump Embedded Circuit  
  - Flow Rate: 0.5ml to 105ml/min
  - Tube Size: 5mm
  - Head Height: 8.1m(26.5')

**Carbon Dioxide Air:** *Atlas Scientific CO2: [EZO-CO2](https://files.atlas-scientific.com/EZO_CO2_Datasheet.pdf)*  
  - EZO™ CO2 Embedded Circuit, Gaseous  
  - Range: 0 − 10,000 ppm
  - Life Expectancy: ~5.5 Years

**Other EZO probes that should work but not yet tested:**  
[Humidity](https://files.atlas-scientific.com/EZO-HUM-Datasheet.pdf), 
[Temperature](https://files.atlas-scientific.com/EZO_RTD_Datasheet.pdf)

### Circuit Diagram
[See Wiki](https://github.com/TheRealFalseReality/aquapi/wiki/Circuit) for more details on the circuit.  

## Software Used  
[**Home Assistant**](https://www.home-assistant.io/): Open source home automation that puts local control and privacy first.   
[**ESPHome**](https://esphome.io/): A system to control your ESP8266/ESP32 and RP2040 by simple yet powerful configuration files and control them remotely through Home Automation systems.

![made-for-esphome-white-on-black](https://github.com/TheRealFalseReality/aquapi/assets/106857076/c68b7da3-17c9-43bf-b8c7-f44acf63eb28)

## Setup AquaPi
### **[See Wiki](https://github.com/TheRealFalseReality/aquapi/wiki/Setup-AquaPi)** for Setup Guides that Include:

### [Home Assistant](https://github.com/TheRealFalseReality/aquapi/wiki/Setup-AquaPi#home-assistant)
Setting up Home Assistant and Connecting AquaPi to your Wifi.
 
### [Update Wirelessly](https://github.com/TheRealFalseReality/aquapi/wiki/Setup-AquaPi#update)
Updating the AquaPi.

### [Web Server](https://github.com/TheRealFalseReality/aquapi/wiki/Setup-AquaPi#update)
Connecting to the AquaPi without Home Assistant.

## Blueprints
**[See Wiki](https://github.com/TheRealFalseReality/aquapi/wiki/Blueprints)**  
These are scripts and automations I created to control other devices within Home Assistant.

## Install
**[See Wiki](https://github.com/TheRealFalseReality/aquapi/wiki/Install)** for guides when installing on a non-configured ESP32 device.

## Notable Substitutions
**[See Wiki](https://github.com/TheRealFalseReality/aquapi/wiki/Substitutions)** for more information on customizing your device.

## Useful Links:
<details>
<summary>See Links</summary>

[**HomeAssistant**](https://www.home-assistant.io/installation/)  
[**ESPHome**](https://esphome.io/)  
[**EZO-pH Circuit Datasheet**](https://files.atlas-scientific.com/pH_EZO_Datasheet.pdf)  
[**EZO-EC Circuit Datasheet**](https://files.atlas-scientific.com/EC_EZO_Datasheet.pdf)  
[**EZO-PMP Circuit Datasheet**](https://files.atlas-scientific.com/EZO_PMP_Datasheet.pdf)  
[**EZO-CO2 Circuit Datasheet**](https://files.atlas-scientific.com/EZO_CO2_Datasheet.pdf)  

</details>
