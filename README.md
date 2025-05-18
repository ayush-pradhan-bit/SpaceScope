# SpaceScope

SpaceScope is a proof-of-concept system designed during the Cassini Hackathon to capture vital signs—specifically heartbeat-related sound and temperature data—from remote or disconnected regions and transmit them via Kineis Nano-Satellites to the Verhaert Connect platform using AllThingsTalk integration.

# Overview
1. Captures heartbeat sound values using a Grove sound sensor.

2. Measures ambient temperature via a DHT20 sensor.

3. Sends compacted sensor data to Kineis KIM1 satellite modem every 60 seconds.

4. Transmits payloads to space, relayed down to Verhaert Connect through the AllThingsTalk platform.

5. Uses a low-power Arduino setup with basic interaction elements like a buzzer and optional button trigger.

# System Architecture


# Hardware Used

- Grove Base Shield + Arduino-compatible board
- Sound Sensor (A1)
- Grove DHT20 Temperature
- Kineis KIM1 Satellite Module
- Nano-satellite uplink (Kineis currently with 7 satellites in orbit)



 
