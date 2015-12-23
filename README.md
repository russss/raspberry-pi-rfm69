# Raspberry Pi RFM69 Hat

This is a simple hat for hooking a RFM69 radio module up to a
Raspberry Pi+.

It has optional connections for two 1-wire sensors if you want to hook
some up.

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
