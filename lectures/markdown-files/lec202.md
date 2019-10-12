# Personal Notes made while studying for CS7NS3 - Next Generation Networks

## Lecture 2 - Overview of Wireless Networks

### Types of Wireless Networks

#### Nomadic

- A network that is considered to be semi-portable
- It provides coverage to users within range
- The Antenna are usually fixed
- User is changing their point of connection to the network
- Wireless local area networks (WLAN), Hot Spots, Wireless ISPs
- Tech: 802.11, Bluetooth

#### Mobile

- Cellular networks
- Should be a seamless browsing experience for a user on the go
- No physical or fixed connection between the transmitter and receiver

### OSI reference model

Follow this [link](https://www.cloudflare.com/img/learning/ddos/what-is-a-ddos-attack/osi-model-7-layers.svg) to view OSI model

#### Physical Layer

- Responsible for modulation, frequency selection and signal detection
- Handles communication impairments referenced in lecture one notes [here](https://github.com/ChrisLynch96/NextGenNetworks/blob/master/lectures/lec1.pdf)

#### DataLink Layer

- Responsible for mediating access to the wireless medium (Physical layer stuff)
- Handles problems that occur due to bit errors
- ensures a nice flow of information so neither the sender or receiver are overwhelmed
- mediates access to the network layer

#### Network Layer

- Addressing and routing is performed in this layer
- Handoff between different networks
- In charge of selecting the best logical path for data to be routed down
- Internet Protocol (IP) is in the Network Layer

#### Transport Layer

- Image above has required info for this layer with regards to course

#### Application Layer

- Deals with application specific exchange of messages
- Responsible for displaying received information to the user

### Frequencies

- The lower the frequency the lower the attenuation with distance and vice versa
- TV is in the lower range
- Cellular and PCS in the in the mid range
- WLANs, WPANs, fixed wireless occupy the higher ranges
- Regulators
  - International Tellecommunications Union
  - Federal Communications Commission (FCC)(US)
- Some degree of harmonization does occur when the ITU meets to discuss spectrum allocation

- Spectrum is inefficiently used
  - Licensed individuals not utilising allocation
  - Re-farming of TV brands
  - Dynamic Spectrum access: can operate in a licensed band as long as you don't interfere with the owner
