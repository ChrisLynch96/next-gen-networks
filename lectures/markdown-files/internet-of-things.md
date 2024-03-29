# Internet of Things

Industrie 4.0 is the upcoming industrial revolution

Notice how its spelled Industrie -> that's because it originates fom Germany

## MTC

Massive variance of the requirements of MTC from massive MTC to critical MTC

### Massive IoT/MTC

Examples: monitoring and automation of buildings and infrastructure, smart agriculture, logistics, tracking and fleet management

Refers to services that typically span a very large number of devices

Typically a very small amount of data generated by the devices and and low latency is not a critical requirement.

Requirements of massive MTC:

1. architecturally simple devices that use a low-complexity transmission mode
2. devices that can run on battery power for many years
3. long transmission ranges for devices in remote locations
4. scalable networks that can connect either a large or a small number of M2M devices

Sometimes, a mobile network may be used to bridge connectivity to the device by means of capillary networks. Here, local connectivity is provided by means of a short-range radio access technology, for example Wi-Fi or Bluetooth. Wireless connectivity beyond the local area is then provided by the mobile network via a gateway node

### Critical IoT/MTC

Examples: traffic safety/control, control of critical infrastructure and wireless connectivity for industrial processes

Industries to benefit: Automotive, Energy utilities, Industrie 4.0

High reliability and low latency. Wide instantaneous bandwidths are useful in being able to meet capacity and latency requirements.

Low cost not as important.

### 5G in IoT/MTC

Looks to satisfy both massive and critical.

Will have 99.999% uptime and ultra low latency < 5ms RTT

Will have to be highly customizable. Network slicing. Move data storage much closer to where control is required for latency -> Edge/Fog computing

Having the same network cover such a wide range of applications is good. Reduces the need for any new application/service to require an entirely different network and avoids spectrum fragmentation.

In IoT, Reduced signaling is a big thing as it is a dominant part of the overall traffic in the network and consequently is a dominant part of battery consumption.

4g and 5g not ready for this yet

### LPWAN

What it is:

1. A technology that supports small messages with specific duty cycles
2. A technology that supports low power end nodes and hence a long battery life
3. A technology that is suited to accessing sensors in awkward spots
4. A technology that has a cost point that suits the end applications
5. A technology that supports the creation of public networks that serve multiple uses and users.

What it aims to achieve:

1. To support a vast number of cheap devices that transmit bursty, small, infrequent messages
2. To have a similar topology to mobile networks, with the aim of better range and penetration through the use if lower frequencies and more robust signals
3. To exceed the radio link budget performance of @G's GPRS by 20dB
4. To support between 50,000 and 100,000 devices per square kilometre in Non Line Of Sight urban areas
5. To achieve > ~15km range in LOS situations. Operating in the sub 1GHz frequencies so that the system can access things placed deep indoors.
6. To maintain cheap devices in the field on one battery fro over 10 years. The BOM must be very low.
7. To keep handshaking to a minimum for a cost and power usage perspective

The immaturity of the application means that the traffic patterns are not well known and so it is difficult to design MAC/network schemes that support emerging applications

### LoRa

What it is:

1. Operates in the 868MHz band, which has favourable propagation characteristics to travel long distances in LOS situations or for greater penetration in NON-LOS
2. Operates in unlicensed spectrum allowing anyone to deploy a base station to service their needs in different scenarios e.g smart agriculture
3. QoS issues as the rules are lax and primarily designed for short range communication.
4. Has a large link budget by using spread spectrum-based PHY
5. Uses simple ALOHA MAC for computation and power reasons. This can be detrimental and costly for QoS.
6. BiDirectional communication is initiated by the thing and not the base station.
7. 250bps to 50kbps
8. Up to 154dB link budget

Allows for different spreading factors which can be selected in an automatic adaptive fashion.

The network server controls a centralized Radio Access Network (RAN). It has a global view of the network

## Acronyms

* IOT: internet of things
* IIoT: Industrial Internet of Things
* M2M: Machine-to-Machine
* MTC: Machine-Type Communications
* SCADA: Supervisory Control And Data Acquisition
* RTT: Round Trip Time
* LPWAN: Low Powered Wide Area Networks
* BOM: Bill Of Materials
* LoRa: Long Range
* RAN: Radio Access Network
