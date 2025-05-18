# SpaceScope

SpaceScope is a proof-of-concept system designed during the Cassini Hackathon to capture vital signs—specifically heartbeat-related sound and temperature data—from remote or disconnected regions and transmit them via Kineis Nano-Satellites to the Verhaert Connect platform using AllThingsTalk integration.

# Overview
1. Captures heartbeat sound values using a Grove sound sensor.

2. Measures ambient temperature via a DHT20 sensor.

3. Sends compacted sensor data to Kineis KIM1 satellite modem every 60 seconds.

4. Transmits payloads to space, relayed down to Verhaert Connect through the AllThingsTalk platform.

5. Uses a low-power Arduino setup with basic interaction elements like a buzzer and optional button trigger.

# System Architecture

<pre> [Heartbeat Sound] + [Temperature Sensor] -> [Arduino + Grove Kit] -> [Kineis KIM1 Module] -> [Nano-Satellite Network] -> [Verhaert Connect (AllThingsTalk)] </pre>


# Hardware Used

- Grove Base Shield + Arduino-compatible board
- Sound Sensor (A1)
- Grove DHT20 Temperature
- Kineis KIM1 Satellite Module
- Nano-satellite uplink (Kineis currently with 7 satellites in orbit)

# Software Details

Libraries Required

- KIM_Arduino_Library (from Verhaert)
- Grove_Temperature_Sensir (From Seeed Studio)
- Wire.h, SoftwareSerial.h

Core Functionality 

- 60s Interval Transmission: Sends a payload every 60 seconds using Kineis AT Commands
- Payload Composition:
    - 2 bytes of temperature 
    - 21 bytes of sound samples (captured rapidly in a loop)
    - Encoded into a 23-byte hex string padded to meet KIM1 specs


 
