My Configuration for Home Assistant, needs a little bit more work

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
