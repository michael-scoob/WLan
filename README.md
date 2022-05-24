# WLan
Discription of how to setup ALFA1900 on Kali Linux

Components:   
**NOTE:** Private use only!

## Install Kali image on VMware  
...
## Driver install  

https://github.com/aircrack-ng/rtl8812au/blob/v5.6.4.2/README.md

## Start/Stop NetworkmManager  

```bash
systemctl start NetworkManager
systemctl stop NetworkManager
```
## WLAN Monitoring

```bash
# Switch WLAN adapter to monitor mode
ifconfig wlan0 down
iwconfig wlan0 mode monitor
ifconfig wlan0 up
```

```bash
```

```bash
```
