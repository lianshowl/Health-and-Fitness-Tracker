# Health and Fitness Monitor

Group Members: Lian Showl, Simon Patel, Timothy Lytkine

##Background
For our final project, we built our own fitness monitoring device that is capable of
running the basic analytics on information given to it. There are two main components of
the system which are data collection and data processing. The sensors used were the
heart rate sensor, real time clock, one display device with a matrix display, 2x7 segment
LED, LCD screen, one environment sensor with the capabilities of a temperature
sensor, humidity sensor, and barometric pressure sensor.
The Arduino sends a sensor reading to a host program (written in C) running on a
UNIX-like system. The two programs communicate over the Arduino’s serial connection.
The host program stores a histogram-like structure of readings which can be easily
queried and outlier readings can be found.

One of the the goals of this project was to detect when the current heart rate is an
outlier. We accomplished this by using a histogram stored in memory on the host
machine. We know that people’s heart rates are different at different times of day.
Clearly, someone’s heart rate will be lower during the night when they are asleep than
during their daily 8AM gym trip. Therefore, a separate histogram was stored for different
parts of the day, in order to more accurately compare heart rate readings.
