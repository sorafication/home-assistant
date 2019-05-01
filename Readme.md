My Configuration for Home Assistant, needs a little bit more work

# Brief instruction
 1) Install Image & Configure Network
 2) Install Addons
 3) Setup Automazation
 4) SSH Configuration
 5) ...


# Step 1: Image & Network

1) Download from: https://www.home-assistant.io/getting-started/
2) Flash to SDCard
3) create on SD ```\CONFIG\network\my-network``` file

Content: (more info: https://github.com/home-assistant/hassos/blob/dev/Documentation/network.md)
```
[connection]
id=hassos-network
uuid=72111c67-4a5d-4d5c-925e-f8ee26efb3c3
type=802-11-wireless

[802-11-wireless]
mode=infrastructure
ssid=$MY_SSID
# Uncomment below if your SSID is not broadcasted
#hidden=true

[802-11-wireless-security]
auth-alg=open
key-mgmt=wpa-psk
psk=$MY_WLAN_SECRET_KEY

[ipv4]
method=manual
address=$MY_IP/24,$MY_DEFAULT_GATEWAY
dns=8.8.8.8;8.8.4.4;
```


# Step 2: Initialization

1) Create Username & Password
2) Connect to Hue Bridge, Google Cast etc.
3) 

How to get a list of Songs play randomly?

        media_content_id: >
                  {{ [
                  "http://192.168.178.40:8123/local/MarioOddysey.mp3",
                  "http://192.168.178.40:8123/local/Pokemon.mp3",
                  "http://stream01.iloveradio.de/iloveradio6.mp3",
                  "http://stream01.iloveradio.de/iloveradio15.mp3",
                  "http://stream01.iloveradio.de/iloveradio4.mp3",
                  "http://stream01.iloveradio.de/iloveradio8.mp3",
                  ] | random }}
