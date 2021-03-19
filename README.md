# scratch3_tbsense2

Scratch 3 extension for Thunderboard Sense 2

This extension aims to make Silicon Labs' Thunderboard Sense 2 (BRD4166A) board work with Scratch 3. The extension was developed based on the Scratch 3 micro:bit extension source code. Currently, LED color (brightness) and LED state (on/off) as control and X/Y acceleration (tilt), thermo- and humidity sensor, and two buttons as sensing are supported.

This extension requires the corresponding [firmware](https://github.com/sza2/tbsense2scratch3) for Thunderboard Sense 2. Note: the release versions must match.

## Installation

I didn't really understand (and don't really want) how Scratch 3 source is structured (multiple repos, installing parts with `npm`, etc.) thus I just provide this extension as a bunch of source files need to add to a working Scratch 3 instance (or overwrite the existing ones) instead pull request to the authors.

First clone [scratch-gui](https://github.com/LLK/scratch-gui) and follow its installation guide, except the last step, `npm start` (actually it is no problem if you start it, the system even detect the changes in the source and restarts as needed without manual interaction).

If the above is done, copy the files in this repo to the corresponding directories of your Scratch 3 installation - this works at the time of writing this document, but may not work in the future. You may want to compare the actual Scratch 3 code/structure with this repo and apply changes on demand. When finished, start the Scratch 3 by issuing `npm start` in its root directory and open http://localhost:8601.

Additionally, you need to run [Scratch Link](https://en.scratch-wiki.info/wiki/Scratch_Link), the WebSocket <-> Bluetooth proxy to access Bluetooth devices from Scratch 3. Since my preference is Linux I used [scratch_link.py](https://github.com/kawasaki/pyscrlink) and not the official Scratch Link.

All installations are done in Linux (Debian 10) I don't know if it works with other versions/distros/platforms (basically it should as these are just Javascript and image files).

The repo contains two demo Scratch 3 applications [tbsense2scratch3demo.sb3](https://github.com/sza2/scratch3_tbsense2/blob/main/tbsense2scratch3demo.sb3) that exploits the tilt and button sensing and LED control capabilities of the Thunderboard Sense 2 and [tbsense2scratch3thermometer.sb3](https://github.com/sza2/scratch3_tbsense2/blob/main/tbsense2scratch3thermometer.sb3) that uses the onboard thermometer sensor.
