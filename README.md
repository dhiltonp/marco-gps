# Overview
Marco is a GPS Bike Computer, based around Arduino. This repository contains general notes for the project as well as code.

When paired with a speedometer and a magnetometer (perhaps with other sensors?), I hope to reduce GPS polling frequency via Inertial Navigations System (INS), ultimately allowing for a very low power device - <5mA on average should be achievable. <1mA would be nice, but is a stretch.

Development will be focused towards basic stats as well as creating a GPS track. Navigation may be added, but is a low priority.

Long-term, supporting a variety of external sensors is desired - heart rate, etc. This may include direct connections to wired speed or cadence sensors. I intend to use my dynamo hub as an initial speed sensor; supporting other types is desired but is not a priority.

# Roadmap

* Interface with Hardware
  * Correctly interface with sensor modules individually
  * Extend device libraries to provide necessary functionality
  * Merge hardware onto same physical platform
* Create UI
  * Add basic UI with time, distance, speed and bearing
  * Scroll through all time stats, activity stats and lap stats
* Discover limits
  * Log data to SD card
  * Add post-processing tools to convert to a GPX track
  * Score GPX track accuracy vs. reference tracks
  * Adjust polling rate and sensor selection
  * Verify performance via fuzzing for worst-case of data sheets

# Hardware

For prototyping, I am using devices from adafruit:

* [Arduino Zero](https://www.adafruit.com/products/2843)
* [GPS+SD Card shield](https://www.adafruit.com/products/1893)
* [Bluetooth LE shield](https://www.adafruit.com/products/2746)
* [Bosch BNO055 9DOF IMU with Sensor Fusion (Accel+Gyro+Mag)](https://www.adafruit.com/products/2472)
* [Freescale MPL3115A2 Altimeter](https://www.adafruit.com/products/1893)
* [Sharp Memory LCD](https://www.adafruit.com/products/1393)
* [Photo cell](https://www.adafruit.com/products/161)
* [Buzzer](https://www.adafruit.com/products/1536)
* [Spring Terminal Blocks](https://www.adafruit.com/products/1074)

I will add the actual layout later.

For potential production hardware, see [this spreadsheet](https://docs.google.com/spreadsheets/d/1vsMMK1ZfQU8QBTO4p9VmQdAtYGPAgfrVgpW_t-hXK8A/edit?usp=sharing)

[Wind speed sensors](https://en.wikipedia.org/wiki/Anemometer#Velocity_anemometers) would be good, but I haven't seen a great solution.

# Prior art (Open Source):

* http://www.avdweb.nl/solar-bike/electronics/solar-bike-computer.html
* http://www.piclist.com/techref/piclist/biketut/index.htm
* http://www.engbedded.com/veloace
* https://hackaday.io/page/428-brainstorming-an-open-bicycle-computer
* http://rockthebike.com/open-source/
* https://github.com/yock/arduino-bike-computer
* http://www.fringeneering.com/2011/07/open-source-cycling-computer.html