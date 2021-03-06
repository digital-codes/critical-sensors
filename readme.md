# Critical-Sensors Project
## Intro
Critical-Sensors creates a link between the exhibition space and its natural environment. Corresponding to the artistic project of Stéphane Verlet-Bottéro (Notes Towards a Permacircular Museum, https://critical-zones.zkm.de/#!/detail:notes-towards-a-permacirular-museum), different sensors were installed in the natural environment of the ZKM. They record environmental data, which are visualized on a website. Weekly pictures display changes over time. Further sensors are installed in the exhibition space and elsewhere. All sensor data are freely available for further analysis.

The project combines a number of components covering basically the full range of digital assets
 * Sensors - the real-world interface
 * MicroController - sensor readout and wireless transmission
 * Software - embedded (C), server (PHP,Python), browser (Javascript)
 * Database
 * Visualisation - the human interface

The corresponding hardware and software is documented in this repository, togethere with data snapshots. Live data can be obtained from the web service.

![Electronics](https://raw.githubusercontent.com/digital-codes/critical-sensor/master/assets/setup2text.png)




## Data Display
Fundamentals are explained in the [Website Readme](https://github.com/digital-codes/critical-sensor/blob/master/website/readme.md)

## Hardware components
### Sensor Unit
  ![Controller](https://raw.githubusercontent.com/digital-codes/critical-sensor/master/assets/controller-side.jpg)
  
 * M5Stack [ESP32 MicroController](https://docs.m5stack.com/#/en/core/gray)
 
  ![C-bottom](https://raw.githubusercontent.com/digital-codes/critical-sensor/master/assets/controller-bottom.jpg)
  
 * M5Stack [LoRa 868 Module](https://docs.m5stack.com/#/en/module/lora868)
 
  ![Lora](https://raw.githubusercontent.com/digital-codes/critical-sensor/master/assets/lora-bottom.jpg)

 * M5Stack [Light Sensor](https://docs.m5stack.com/#/en/unit/light)
 
  ![Light](https://raw.githubusercontent.com/digital-codes/critical-sensor/master/assets/lightSensor.jpg)

 * EplusE C02-Temerpeature-Humidity-Pressure Sensor [EE894](http://downloads.epluse.com/fileadmin/data/product/ee894/datasheet_EE894.pdf)
 
  ![EE894](https://raw.githubusercontent.com/digital-codes/critical-sensor/master/assets/ee894.jpg)

 * Solar [Power Bank](https://www.pearl.de/a-PX2957-1420.shtml) or similar
 
  ![Power](https://raw.githubusercontent.com/digital-codes/critical-sensor/master/assets/powerBank.jpg)

* Birdhouse style housing, wood or 3D printed

  ![Housing](https://raw.githubusercontent.com/digital-codes/critical-sensor/master/assets/birdhouse-3d.png)

 ### Gateway
   ![Gateway](https://raw.githubusercontent.com/digital-codes/critical-sensor/master/assets/gateway.jpg)

  * ESP32 based LoRa Module [TTGO](http://www.lilygo.cn/prod_view.aspx?TypeId=50003&Id=1134&FId=t3:50003:3) 
  * Cellular modem based upon [SIM800L](https://www.simcom.com/product/SIM800.html) 
  
## Software Components
 * Sensor Software, C++ Arduino based 
 * Gateway server, Python, update database with new sensor data 
 * Data server, PHP, serving data for website and users 
 * Website, HTML, Javascript 
   * [Live](https://critical-sensors.de/) 
 * Tools, Python for CO2 spiral video, download of reference data and scatterplot matrix 
 
 

 
 
