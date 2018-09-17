# ESP8266-WiFi-LED-System
A system to using ESP8266s to control addressable LEDs through a WiFi network.

# Setup(For a ESP8266 nodemcu)

## Requirements
-Python
-Pip
-WiFi Enabled Laptop of Cellphone (easier with laptop)

## Get the bin file
-Dowload this clone or download this repository.
-Navigate to the repositry in your comand line.

## Get Espressif Tool
-Go to https://github.com/espressif/esptool/ in your browser
-Follow the install isntructions

##Flash bin onto ESP8266
-esptool.py --port COM4 write_flash 0x00000 my_app_file.ino.bin
--Specifying the port is only necessary if you have multiple COMs in use.
--Don't miss the .bin the file will still compile, but it won't work correctly.
--There is a serial port connected on 9600 and you can monitor it to make sure it is connecting. It is fully set up when the monitor prints "MQTT connected". Then all commands will also show up in the monitor.

##Create AWS IOT Thing
-Navigate to "leds.mrcatnaps.com"
-Click "Login with Amazon" and login
-Copy the new Thing Name (right most column)
--If you are going to pair this with Alexa, Edit the Custom Invoke Name to the word you want to invoke with Alexa (bedroom), and click "Update"

##Setup ESP8266
-Connect to WiFi "MrCatNaps LED Setup"
-Navigate your browser to "196.168.4.1"
-Click Setup
-Fill out the information. WiFi SSID, Password, # of LEDS (max 800), RGB Order, thingname**
-Paste the Thing Name from the previous step in here.
-Click Connect/Disconnect (wifi will disconnect and you can reconnect to your normal network)

##Seting up Alexa (Optional)
-Navigate to "echo.amazon.com"
-Intall the home skill at https://www.amazon.com/Mr-CatNaps-LEDs/dp/B079PQJNTM
-Click the "Smart Home" tab on the left pane in the echo home menu.
-Click on "Devices"
-Click "Discover"
-Your devices should be found and you can use Alexa commands. "Alexa turn off bedroom." "Alexa set bedroom brightness 10."

#Congratulations you are set up!
-Navigate to "leds.mrcatnaps.com"
-Login again if you have too. There is cache, so you won't have to login everytime. 
-Click a scene or set a color!
-Enjoy

