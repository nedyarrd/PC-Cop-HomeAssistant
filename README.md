# PC-Cop-HomeAssistant

Main goal of that project is to create sensors for home heatpump. Project contains:
* board schematics with:
  * ESP32Dev Kit
  * ILI9341
  * PZEM004-T
  * 2x Dallas DS18b20  
* ESPHome yaml file

That project by using sensors gives data about Your heatpump:
* Temperatures
  * supply and return
* Electrical characteristcs
  * power (when heating or cooling)
  * current
  * consumed energy
  * voltage
  * power factor
* Calculates
  * COP - coefficient of performance
    * heating
    * cooling
    * daily
  * heating or cooling power
  * produced heating or cooling energy
  
Current limitations:
* I assume that water flow through heatpump is 20 litres per second
* pump in your heating system must have constant performance
* project assumes that heatpump is generating power only if electric power is greater than 100Watts
* assumes water density at 994

# How to change constants:
in lines: 113,128 there is an equation beginning with 0.02, that means 20 litres/sec
