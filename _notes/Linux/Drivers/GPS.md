# GPS/Glonass
---

## how to install
```
sudo apt install gpsd
```
client install
```
sudo apt install gpsd-clients
```


## how to set up and use

-check to see if there is ttyACM0
```
ls /dev/tty*
```

-another way to check try:
```
sudo dmesg | grep tty  
```
should see ttyACM0
```
sudo gpsd -D 5 -N -n /dev/ttyACM0
GPSD_OPTIONS="/dev/ttyACM0"
```


## Internal link index

[[Alpha WiFi|Alpha WiFi install]]

## URLs
https://gpswebshop.com/blogs/tech-support-by-os-linux/how-to-connect-an-usb-gps-receiver-with-a-linux-computer