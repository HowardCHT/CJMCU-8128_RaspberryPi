# CJMCU-8128_RaspberryPi

## About
For NTUT Special Projects Test

## Get start
```
$ git clone https://github.com/HowardCHT/CJMCU-8128_RaspberryPi.git
$ cd CJMCU-8128_RaspberryPi
$ python3 -m venv .venv
$ pip install -r requirements.txt
```

Set ..\lib\python3.7\site-packages\adafruit_bme280.py
```
_BME280_ADDRESS = const(0x76)
_BME280_CHIPID = const(0x58)
```

Set rpi-sensor.service
```
$ chmod 755 rpi-sensor.service
$ sudo ln -s /home/pi/Desktop/Env_parameter/rpi-sensor.service /etc/system
d/system/rpi-sensor.service
$ sudo systemctl daemon-reload
$ sudo systemctl enable rpi-sensor.service
$ sudo systemctl status rpi-sensor.service
```
Check service log
```
$ journalctl -u rpi-sensor.service -f
```
