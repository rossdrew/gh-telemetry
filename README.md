# Greenhouse Telemetry

_Some code experimenting with greenhouse telemetry_

## Controller

Current using a Rasberry Pi 3 Model B v1.2

## Temp/Humidity

We are using the AM2302 wired as follows

```
VCC -> Pi Pin 1
GND -> Pi Pin 6
DATA -> Pi Pin 7
``` 

and the [Adafruit Python Drivers](https://github.com/adafruit/Adafruit_Python_DHT) which can be set up as follows

(1) Clone the drivers repo
```bash
git clone https://github.com/adafruit/Adafruit_Python_DHT.git
cd Adafruit_Python_DHT
```

(2) Make sure python is up to date
```bash
sudo apt-get upgrade
sudo apt-get install build-essential python-dev
```

(3) Install the Adafruit drivers
```bash
sudo python setup.py install
```

(4) Run the test to make sure it worked
```bash
cd examples
sudo ./AdafruitDHT.py 2302 4
```