# BSD_on_OpenBlocksIX9
Confirm boot on OpenBlocksIX9 for NetBSD 9 and FreeBSD 12.1.

## For X11
In order for the Intel driver to work properly, the following must be added to the Device section in xorg.conf as follows

```
Section "Device"
        Identifier  "Card0"
        Driver      "intel"
        BusID       "PCI:0:2:0"
        Option      "AccelMethod"  "uxa"
EndSection
