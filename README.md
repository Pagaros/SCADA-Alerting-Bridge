# SCADA-Alerting-Bridge

## Problem:
I have a SCADA system that operates in its own network without any external connections. The problem was that this meant I couldn't send alarm messages to the outside world to notify the on-call team. That meant I had to come up with something.

## Solution:
I send the alarms via an RS-232 interface to another server located in a different network, which runs a Python script that receives the alarms, formats them, and then sends them to our alarm distributor ([Divera](https://www.divera247.com/)) via a GET request.

Because modern computers no longer have an RS-232 interface, an external COM port is used. [Link](https://www.wut.de/e-58665-ww-dade-000.php)

To ensure that data can only be sent out and not received, only the transmit pin was soldered to one side of the RS-232 connection cable and only the receive pin to the other side.



ToDo:
- upload Graphic,
- upload Python script,
