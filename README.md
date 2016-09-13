# Raspberry Pi RFM69 Interface

This is a Raspberry Pi interface to the HopeRF RFM69 module, designed
for the [UKHASnet](https://ukhas.net) project.

It supports up to 4 channels with independent RFM69 transceivers, intended
for experimenting with sectored antennas and long-range backhaul links,
but can also be used with just a single RFM69 for more normal applications.

For code which works with this, check out my [rfm69
python library](https://github.com/russss/rfm69-python).

## BOM

To use just a single RFM69 channel, you will need:

* IC1: RFM69[H][W]
* J1: 40-pin socket (e.g. Farnell 7992033)
* P1: Edge-launch SMA socket

To use more than one RFM69, you'll additionally need:

* IC5: 3.3V 800mA regulator in SOT-223 package e.g. NCP1117 (Farnell 1652366)
* C1, C2: 10uF 0805 SMD capacitors
* IC6: 74HC139 Demultiplexer, TSSOP-16 (Farnell 2444981)
* Plus additional RFM69s and SMA sockets

To use one-wire sensors if you require a strong pull-up:

* R1: A 4k7 0805 SMD resistor

## Assembly

If you want to use a single RFM69, you'll need to bridge jumpers J1 and
J2. J1 connects the 3v3 bus to the RPi's (which will *just about* run
one RFM69 from my experience).

J2 bypasses the demultiplexer on the SPI chip select line and
connects it directly to the first RFM69.

## Pin Mappings

|Module | Interrupt (DIO0) | Reset  |
|-------|------------------|--------|
|1      | GPIO20           | GPIO21 |
|2      | GPIO02           | GPIO03 |
|3      | GPIO27           | GPIO22 |
|4      | GPIO19           | GPIO26 |

* 1-wire: GPIO4
* NSS Select: GPIO23 (bit 1), GPIO24 (bit 2)
