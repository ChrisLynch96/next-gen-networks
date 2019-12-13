# Fixed Mobile Convergence

factors to increase mobile capacity

* Efficiency (MIMO, Smart scheduling, enhanced-CoMP) -> x3
* Spectrum (Carrier Aggregation, New Bands, Authorized Shared Access) -> x2
* Density (Advanced Macros, HetNet management, Flexible small cells) -> x167

Backhaul refers the intermediate layer between the core network and the access layer at the edge.

## Cell density issue

Backhauling a macro base station is economically feasible as each base station serves many users

As the density increases than the number of users being served is less and thus the economic viability is less.

Shared PON to be used between base stations homes etc.

## RAN

Until 4g the base stations were distributed meaning that each cell mast had everything required up to layer 3. This required a bulky coaxial cable that was costly, not wind resistant etc.

Now all wires are replaced by a fibre cable.

Now digital processing is being centralized

Connection between BBU and RRU is fibre through a protocol called  Common Public Radio Interface (CPRI)

All digital processing is done at the BBU and then the RF signal is sampled, digitized, and sent over to the RRU for processing.

Baseband unit is in the network and the RRU is on the mast

## BBU Hoteling

Utilising the advantages of a fibre connection between the BBU and the RRU.

Can place the BBU in a different location because the range that we can transfer data is drastically increased by fibre.

Can use a building to store multiple BBUs. The building is more secure, less prone to weather effects, less location constrained, easier for maintenance etc.

## BBU Pooling

Now that multiple antennas connections are coming to the one building why not use statistical multiplexing of the data and use a smaller number of BBUs. Not all cells will be running at peak rate all the time.

NFV: BBUs are now implemented in software running on off the shelf servers along with firewalls and routers etc. No need for dedicated hardware.

## Cloud RAN

The BBU is running as software on a server so now the idea can be expanded to Cloud computing, be it public or private cloud.

## Fronthaul

CPRI places the division line, between BBU and RRU, close to the Antenna on the LTE stack. For this reason it is called fronthaul.

To calculate the data rate of CPRI it is: R = Rs x Nq x Na x Nb x Rc x Rl

where:

* Rs is the sampling rate, and is 30.37MHz for a 10MHz wireless bandwidth (notice that there is oversampling)
* Nq is the number of bits used to digitize each samples and it’s typically 15 bits
* Na is the number of antennas used
* Nb is the number of 10MHz frequency bands used
* Rc is the overhead given by word control ratio (16/15)
* Rl is the overhead given by the line coding (10/8 or 66/64)

The rate is independent of the actual rate offered to the users. Always transmits the maximum rate of actual usage.

Fronthaul requires a transmission capacity 16 times higher than the equivalent backhaul rate.

Fronthaul must have a RTT of 3ms or less due to HARQ being used.

### Fronthaul over PON

true ptp in a high density network is unsustainable (prohibitively expensive).

* Virtual PTP:
  * Virtual ptp (assign an individual wavelength to a RRU). Uses more expensive transceivers but less fibre.
* Ptmp: TDM multiplexing between different base stations (or even residential users).
  * makes sense if rate at each RRU  is relatively low.
  * Can only be used with fixed bandwidth allocation at this moment as Dynamic Bandwidth Allocation introduces undesired latency to the solution.

### Fronthaul capacity issue

Reduce capacity required in the optical channel via signal compression.

Carried out by reducing the number of quantisation bits. Compression rate of up to 1:2 or even 1:3

typically lossy compression

Can also do:

Split the physical processing or midhauling:

* A bit more processing at the RRU can reduce the optical transmission rate considerably
* restores the proportionality with the user traffic and thus reintroduces the possibility of carrying out statistical multiplexing.

![](markdown-files/images/splits.png)

To get rid of limit on latency we need to choose a split option of 3 or lower (Need to have HARQ performed at the RRU)

eCPRI is the new standard that has identified the capacity and latency requirements for functional splits

## Acronyms

* RAN: Radio Access Network
* BBU: BaseBand Unit
* RRU: Remote Radio Unit
* CPRI: Common Public Radio Interface
* RF: Radio Frequency
* NFV: Network Function Virtualization
* eCPRI: evolved CPRI
