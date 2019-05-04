How to Configure a Raspberry PI Zero W as Bluetooth Gateway for example

# Prerequisites:
  1) Pi with  Hassio
  2) Pi Zero with Raspbian
  
  
# Step 1: Headless Pi Zero W Installation

  1) Download latest Image and flash it (https://www.raspberrypi.org/downloads/raspbian/)
  2) Keep SD mounted onwpa_supplicant.conf PC and create following files
  ```
  /ssh
  /wpa_supplicant.conf
  ```
  Important: Ensure that wpa_supplicant.conf has Linux (LF) characters
  
  Content of wpa_supplicant.conf
  
 ```
  country=DE 
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev 
update_config=1 
network={
     ssid="$WLAN_SSID"
     scan_ssid=1
     psk="$WLAN_PASSWORD"
     key_mgmt=WPA-PSK
}
  ```
  
  Now you can connect to ssh with 
  Username: ``pi``
  Password: ``raspberry``
  
  
  ### Configure Static IP
  edit ``vim /etc/dhcpcd.conf`` 
  
  Add:
  ```
wlan0 interface 
static ip_address=192.168.1.100/24 
static routers=192.168.1.1 
static domain_name_servers=192.168.1.1
  ```


# MQTT CONFIG
https://www.home-assistant.io/addons/mosquitto/
https://github.com/zewelor/bt-mqtt-gateway
