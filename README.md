# Raspberry Pi RFM69 Hat

This is a simple hat PCB for hooking a HopeRF RFM69 radio module up to a
Raspberry Pi+.

It has optional connections for two 1-wire sensors if you want to hook
some up.

For code which works with this, check out my [rfm69
python library](https://github.com/russss/rfm69-python).

## BOM

* One RFM69[H][W].
* One 40-pin socket (e.g. Farnell 7992033)
* One edge-launch SMA connector (or just solder a bit of wire to the
  centre pin).
* Optionally: a 4k7 resisitor and a 1-wire sensor or two.

## Pin Mappings

* RESET -> GPIO21
* DIO0 -> GPIO20
* DIO4 -> GPIO26
* 1-wire -> GPIO4
