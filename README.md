USBH_MIDI
=========

USB-MIDI class driver for Arduino [USB Host Shield 2.0 Library][UHS2]

You can convert USB MIDI keyboard  to legacy serial MIDI.

Please check [device list][wiki]

How to use
----------
Please put into a USBH_MIDI directory to your Arduino libraries directory.

for single device
> File->Examples->USBH_MIDI->USB_MIDI_converter

for multiple device (with USB hub)
> File->Examples->USBH_MIDI->USB_MIDI_converter_multi

Note
> If you have Arduino Lenoardo, please change "Serial" to "Serial1"

API
---

uint8_t RcvData(uint16_t *bytes_rcvd, uint8_t *dataptr);
> Receive raw USB-MIDI Event Packets (4 bytes)

uint8_t RcvData(uint8_t *outBuf);
> Receive MIDI messages (3 bytes)  
return value is MIDI message length(0-3)

uint8_t SendData(uint8_t *dataptr, byte nCable=0);
> Send MIDI message. You can set CableNumber(default=0).

ChangeLog
---------

2013.08.28
* Fix MIDI Channel issue.

2013.08.18  
* RcvData() Return type is changed to uint8_t.
* Fix examples.

2012.06.22  
* Support MIDI out and loosen device check

2012.04.21  
* First release



License
-------
Copyright &copy; 2012 Yuuichi Akagawa

Licensed under the [GNU General Public License v2.0][GPL2]

[GPL2]: http://www.gnu.org/licenses/gpl2.html
[wiki]: https://github.com/YuuichiAkagawa/USBH_MIDI/wiki
[UHS2]: https://github.com/felis/USB_Host_Shield_2.0
