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
