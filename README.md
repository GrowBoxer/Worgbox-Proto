# Worgbox
Growbox with Arduino based controller

##Introduction
Growbox named 'Worgbox'. What do I mean? 'Worg' and 'box'. 'Worg' in parallel universe sounds like 'Grow'. 
No need to explain you how we can travel there :]
Main idea I want to make a compact and controlled box for growing something small in compact area and possible stealthy.

##Construction
- Dimensions 260mm x 260mm x 470mm.
- Material is 6mm laser cutted plywood.

##Components

###Controller
- Arduino UNO (Arduino Pro Mini)

###Sensors
- DHT22 
- DS18B20

###Light
- 16x3W full spectrum LEDs

###Fans
- 2x 12cm FANs (3x optional)

###Additional
- ESP8266 WiFi Module (ESP-01)
- OLED 128x64 I2C display
- 2x DC SSR
- LED driver
- Precise clock module ds3231
- 3x buttons for change settings

##How It Work
Controller have 4 light modes: 24/0, 18/6 (default), 12/12 and 0/24 (hours of day/night). ON/OFF by SSR.
Default time when night starts: 18:00.
Default FANs speed: 90% when day, and 30% when night (range 30-95%). Regulated by PWM with SSR. At FAN SSR control PIN PWM frequency lower than standart.
With buttons you can change this modes and parameters.
OLED Display show main parameter, time also temperatures and humidity.
WiFi module have IP and rining web server. Http request answer is JSON (current parameters, sensors data, etc.).

##Files
- PlywoodLaserCut.dwg — 2d scheme of each plywood sheet for laser cutting in DWG format (AutoCAD).
- Worgbox.max — 3d model of box in 3dsmax format;
- wiring.xxx;
- pcblayout.xxx;
- worgbox.ino — arduino sketch;
- data.json — example of data recieved from controller;
- data.csv — example of data sended to thingspeak;

###TO DO Files
- check DWG for actual changes
- - need back door fan shift
- - need solid plywood base for light compartment door

###TO DO Construction
- using bigger holles for wires (up to 5 mm diameter)
- separate high voltage and low voltage compartments;

###TO DO Hardware
- kill the freezes and stop working of controller (need shield? no other cause);
- make PCB for working with Arduino Mini Pro;
- setup temeprature sensor to the LED radiators;
- read white wire data from the fans (for RPM analyze);

###TO DO Software
- analyze fans RPM;

###Ideas Components
- migrate totally to ESP8266
- different SSR relays for PWM control light and box fans (different RPM)

###Ideas Construction
- transparent acrylic window for revision of main area
- one-point lock for main door (now have 4-point locks)
- put screws deeper (into first plywood layer)
- replace membrane buttons to the touch
