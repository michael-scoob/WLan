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

Befor you start to monitor wlan networks run followin cmd ...
```bash
airmon-ng check kill

# Output ...
Killing these processes:

    PID Name
 208065 wpa_supplicant
```
now you can start monitor mode ...

LINK:  
https://www.cellstream.com/reference-reading/tipsandtricks/410-3-ways-to-put-your-wi-fi-interface-in-monitor-mode-in-linux

```bash
# Option 1
sudo ip link set wlan0 down
sudo iw wlan0 set type monitor
sudo iw wlan0 set type managed
sudo ip link set wlan0 up

# Option 2 
airmon-ng start wlan0 
```
### Start monitoring
```bash
airodump-ng wlan0

# Output ...
CH  9 ][ Elapsed: 1 min ][ 2022-05-24 04:30 ][ WPA handshake: 38:43:7D:4D:34:68                                
                                                                                                                
 BSSID              PWR  Beacons    #Data, #/s  CH   MB   ENC CIPHER  AUTH ESSID                                
                                                                                                                
 33:2C:C4:49:9E:99   -1        0        0    0   3   -1                    <length:  0>
 ...

```
### Stop monitormode and change wlan intf back to manged mode 
```bash
# Option 1
sudo ip link set wlan0 down
sudo iw wlan0 set type managed
sudo ip link set wlan0 up

# Option 2 
airmon-ng stop wlan0 
```
# Graphic WLAN Analyser: sparrow-wifi
https://github.com/ghostop14/sparrow-wifi/blob/master/README.md



