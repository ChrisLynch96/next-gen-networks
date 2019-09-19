# Personal Notes made while studying for CS7NS3 - Next Generation Networks

## Lecture 1 - Wireless channel impairments and mitigation techniques

- Impairments: Phenomenon that reduce the signals strength/usefulness
- Mitigation: methods to proactively reduce impairment phenomenon

### Impairments

#### Path Loss

- Signal attenuates with distance

  - Attenuation: reduction in force, effect or value of something
  - Loss is roughly proportional to $\frac{1}{d^2}$

#### Shadowing

- The attenuation that occurs from obstacles being in the path of the signal from transmittor to receiver
- Modelled with a log-normal distribution

#### Multi-path

- Due to reflection and scattering multiple version of the signal may arrive at the receiver.
- Think if this as the signal splitting as it hits an uneven surface.
  - out of phase versions may cancel each other out.
- Can also cause a delay spread of the signal as the out of sync version arrive

#### Fading (wireless)

- The signal loss as it propagates throught a medium
- When referring to a wireless medium, fading is referencing Multi-Path signal loss i.e it's bouncing off of many different surfaces as the signal aims to reach the receiver.

#### Noise

- Unwanted signals added to the transmitted signal.
- Can come from both natural and man-made phenomenon.
- _Signal to noise Ration_ (SNR) is used as a measure of the quality of a channel.

### Mitigation

#### Diversity

- Combining independently received versions of the desired signal.
- Often done in the form of multiple antennas, multiple frequencies, repeated transmission and different polarizations

#### Directional Antennas

- Basically directing antennas to maximize gain in a certain direction.

#### Coding and Modulation

- Digital Modulation
  - Various schemes for digital modulation varying in power efficiency, spectral efficiency and robustness

#### Spread Spectrum

- distributed over a wide range of frequencies and collected back at the receiver
- Difficult to detect and interfere with

#### Frequency Hopping

- Transmitter and receiver hopping between pre-defined frequency bands.
- For security
- Fast and slow hopping

### Qs from lecture and answers

---

*Q* : what is the most detrimental wireless channel impairment for LAN?

*A* : Interference as access points are deployed very close to each other

---

*Q* : What about WAN

*A* : Path loss and noise due to the distance between stations.

---

*Q* : What about hilly regions

*A* : Shadowing, the transmitter and receiver are not in line of sight
